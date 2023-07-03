# Crackme
>Could you crack the pin for me? ;)

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/9f2f7504-049e-4da3-8579-604d1f434cfd)

Given a 64 bit binary file - not stripped

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/589b0f5d-8598-4fb0-b3b2-adf334747ecd)

Immediately, we do static analysis by decompiling
on binary files.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/374f3e77-3a65-4b3f-8bd2-7839d938c4c7)

Based on the if statement in the main function, it seems we just need to
enter the hardcoded pin in the source code, namely 151235. Then automatically
automatically the looping process will be executed x

```console
NOTES:
The looping process contains the XOR algorithm
```
and the flag will be displayed

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/1c7ddad8-e53c-4dfd-b5ee-fe529e7431d4)

Flags successfully obtained:
```console
ForestyCTF{debug_debug_n_debug_for_the_key_a53dfa}
```
