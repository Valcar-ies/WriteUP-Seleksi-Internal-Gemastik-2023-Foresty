# Two Time Pad
>One Time Pad? No, this is Two Time Pad.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/14752b25-2704-476b-9331-0e2b83c2b3e1)

In this crypto challenge, we are given a .txt file and a python script
seems to be the source code to encrypt the flag

This is the content from encrypted message

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/d3c25159-1306-468e-bc16-65a40ba770c5)

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

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/83f3d276-8a0c-4514-840d-2e08c65633f5)

#### Flags successfully obtained:
```console
ForestyCTF{ecebe_crib_fl4ggg_11d28a}
```
