# Signature
>Someone gave me a file, but I can't open it. Help me to open the file
Telah diberikan

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/dd790fdc-020e-4fe2-98ab-49ccbb9140d3)

A corrupt file has been given, thus making the file inaccessible
opened.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/87a02476-2189-4536-8d45-3975ddf49e8c)

In order to patch, it is necessary to identify this file type, but in
At first I had quite a hard time because I rarely played forensics for
some time.

But when checking all file headers of image types
(PNG,JPEG/JFIF,JPG)

I found there is a signature of JFIF in the last 2 chunks.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/f38bb040-5c33-495b-aedf-dc3890d13a41)

Reference : 
```console
https://www.file-recovery.com/jpg-signature-format.htm
```

Knowing this, we can patch the signature file header to
FF D8 FF E0 00 10 4A 46 49 46 00 01 01

Here is a comparison of the two, for the left
is before it was changed and to the right after it was changed

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/9fd85220-dd2f-4940-9091-423767f96d84)

Then save, and the image can be opened:

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/81953c2e-6463-4711-a94c-8f12b2b932c0)

#### Flags successfully obtained:
```console
ForestyCTF{ezzzz123!!!}
```

##### Solved by : valcaries
