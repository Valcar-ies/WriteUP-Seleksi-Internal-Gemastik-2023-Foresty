# Signature
>Someone gave me a file, but I can't open it. Help me to open the file
Telah diberikan

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/7079926a-053e-4f0d-957e-5c650901420a)

A corrupt file has been given, thus making the file inaccessible
opened.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/8dc5d92e-14e8-4578-a218-64291350106f)

In order to patch, it is necessary to identify this file type, but in
At first I had quite a hard time because I rarely played forensics for
some time.

But when checking all file headers of image types
(PNG,JPEG/JFIF,JPG)

I found there is a signature of JFIF in the last 2 chunks.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/4efdea60-d5a4-4bc7-aa22-44f3fcd32465)

Reference : 
```console
https://www.file-recovery.com/jpg-signature-format.htm
```

Knowing this, we can patch the signature file header to
FF D8 FF E0 00 10 4A 46 49 46 00 01 01

Here is a comparison of the two, for the left
is before it was changed and to the right after it was changed

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/249db911-ce87-431d-876a-0dfa25be0737)

Then save, and the image can be opened:

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/dd4dd04c-3b00-4206-b5cf-309cf38a53a2)

#### Flags successfully obtained:
```console
ForestyCTF{ezzzz123!!!}
```

##### Solved by : valcaries
