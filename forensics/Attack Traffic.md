# Attack Traffic
>Oh no, my web app has been hacked by someone and I think my secret
password has been leaked.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/b2cdb199-b961-48e5-9955-3c97facc74c7)

Given a capture file that records the website traffic logs that have been
hacked.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/793a7f62-cafc-4ef2-94e0-65893002ef9b)

Because data is too much, do filtering by looking for http only
or related to login traffic or opening attempts
password.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/168b0015-d0fa-4ac3-b849-15dc5500c3fb)
![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/187eae66-b2dc-4a11-aa47-9d53110623c3)

By checking the http logs, we found the info that contains
many password characters, then on wireshark you can see there is info
(password, 1, 1) which means the value of the search attempt is the character value first. Because there is a lot of info (password, 1, 1), then choose info
(password, 1, 1) the last one which means the password is correct.
Info info(password, 1, 1) = 70 denotes the first character of the flag
is a character with an ascii number of 70. Then enter it in
ascii to text online converter. To find the flag, do that
up to a password value of 48.

If you have found all the ascii numbers, enter them in
online converter to convert to plaintext. Then get flags
as follows.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/7f6997eb-c7aa-4279-a7ec-a69de68d537e)

#### Flags successfully obtained:
```console
ForestyCTF{Ohh_no_my_web_has_been_hacked_4a2fac}
```
