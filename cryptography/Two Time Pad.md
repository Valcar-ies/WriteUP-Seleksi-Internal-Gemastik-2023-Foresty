# Two Time Pad
>One Time Pad? No, this is Two Time Pad.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/08982101-4e98-4864-b5e7-3f674883a4e9)

In this crypto challenge, we are given a .txt file and a python script
seems to be the source code to encrypt the flag

This is the content from encrypted message

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/cf9296e3-3d68-4680-9ea7-895c8a42ee61)

Based on the title & description of the problem, I assume the concept of crypto
namely One TimePad. So, i immediately use online tools
```console
https://toolbox.lotusfa.com/crib_drag/
```

Based on the source code provided, the concept is quite similar to
XOR, even though we don't know the KEY, but still can
get the flag because we are given the encrypted flag, and plaintext MSG
which is also used in the encryption process

So let's just use:

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/ecb35242-a848-473a-8f68-8e032b6c27f8)

#### Flags successfully obtained:
```console
ForestyCTF{ecebe_crib_fl4ggg_11d28a}
```

##### Solved by : valcaries
