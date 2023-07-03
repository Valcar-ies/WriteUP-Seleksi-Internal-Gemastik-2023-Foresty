# Ransomware
>Could you help me to recover my encrypted files from this ransomware?

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/c8d1de6d-a6aa-4868-9a1b-b0f7d2065a8b)

Hints given:

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/f6079c05-b5cb-4c43-8c93-890adbdb4675)

Given 2 files, one zip file and one .pyc file.
When the zip file is unzipped, you get 3 image files that appear to be encrypted.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/0be5f57b-b20a-4b7e-839b-20e1a1c92db7)

My assumption is, all images are encrypted using .pyc files.
To get the python source code, I decompile it
using a tool called pycdc which I installed via:
```console
https://github.com/zrax/pycdc
```

Then, here are the results:

```py
# Source Generated with Decompyle++
# File: ransomware.pyc (Python 2.7)

Warning: Stack history is not empty!
from Crypto.Cipher import AES
from Crypto.Util.Padding import pad, unpad
from Crypto.Random import get_random_bytes
from zlib import compress, decompress
import os

def encrypt_file(filename):
    with open(filename, 'rb') as f:
        data = f.read()
    aes_key = get_random_bytes(16)
    aes_obj = AES.new(aes_key, AES.MODE_CBC)
    enc_dat = aes_obj.encrypt(pad(compress(data), AES.block_size))
    with open(filename + '.encrypted', 'wb') as f:
        f.write(aes_key + aes_obj.iv + enc_dat)
    os.remove(filename)

if __name__ == '__main__':
    path = 'target'
    for file_name in os.listdir(path):
        encrypt_file(os.path.join(path, file_name))
```

Based on the source code obtained, it seems the image is "correct"
encrypted using this script, that's why I did
reversing in scripts,
here are the results:

```py
from Crypto.Cipher import AES
from Crypto.Util.Padding import unpad
from zlib import decompress
import os

def decrypt_file(filename):
    with open(filename, 'rb') as f:
        data = f.read()

    aes_key = data[:16]
    iv = data[16:32]
    enc_data = data[32:]

    aes_obj = AES.new(aes_key, AES.MODE_CBC, iv)
    dec_data = aes_obj.decrypt(enc_data)
    dec_data = decompress(unpad(dec_data, AES.block_size))

    decrypted_filename = os.path.splitext(filename)[0]
    with open(decrypted_filename, 'wb') as f:
        f.write(dec_data)

if __name__ == '__main__':
    encrypted_file1 = 'flag1.png.encrypted'
    encrypted_file2 = 'flag2.png.encrypted'
    encrypted_file3 = 'flag3.png.encrypted'
    decrypt_file(encrypted_file1)
    decrypt_file(encrypted_file2)
    decrypt_file(encrypted_file3)
```

Then the following results are obtained, fragments of encrypted image files
will be decrypted:

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/da2fb046-6c2f-47cb-b37b-368f85879b44)

So if i opened one by one and put together it will
form the flag:

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/89d34437-d35d-4773-8e5e-e8c56e4d92dc)
![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/f23c5ab9-4604-4246-9793-74ef1d5268d2)
![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/616d07ff-3186-45b0-bb6f-efc2f4bf0ffa)

Combine the three images above into flags according to the order
on the file name.

#### Flags successfully obtained:
```console
ForestyCTF{the_real_ransomware_never_store_the_key_hardcoded_on_encrypted_file_12da1f}
```

##### Solved by : valcaries

