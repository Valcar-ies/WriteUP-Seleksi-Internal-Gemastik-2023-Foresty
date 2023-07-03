# Crackme
>Could you crack the pin for me? ;)

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/3318d5fb-c91a-496c-9c48-28049eaaf542)

Given a 64 bit binary file - not stripped

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/7c3877d9-5cac-47a4-9acf-7a82caba2949)

Immediately, we do static analysis by decompiling
on binary files.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/8c8fa33f-9fb6-45ae-943c-0ddba74bfb54)

Based on the if statement in the main function, it seems we just need to
enter the hardcoded pin in the source code, namely 151235. Then automatically
automatically the looping process will be executed x

```console
NOTES:
The looping process contains the XOR algorithm
```
and the flag will be displayed

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/5b45783b-577b-4264-a3e0-064dd192da4b)

#### Flags successfully obtained:
```console
ForestyCTF{debug_debug_n_debug_for_the_key_a53dfa}
```

##### Solved by : valcaries
