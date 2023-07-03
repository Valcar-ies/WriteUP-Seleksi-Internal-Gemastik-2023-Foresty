# Attack Traffic
>Oh no, my web app has been hacked by someone and I think my secret
password has been leaked.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/47f59c18-ad80-45c3-80de-e06cec55fc7a)

Given a capture file that records the website traffic logs that have been
hacked.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/c8c066a1-d40d-4745-af91-475fa9a83d0d)

Because data is too much, do filtering by looking for http only
or related to login traffic or opening attempts
password.

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/40845d13-f82f-4615-bd9e-03f4df846421)
![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/6487bd80-293e-43df-b57e-bb6f0ccf9a76)

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

![gambar](https://github.com/Valcar-ies/WriteUP-Seleksi-Internal-Gemastik-2023-Foresty/assets/84186470/7f5258f5-5c54-4f8a-bf66-586a36a36226)

#### Flags successfully obtained:
```console
ForestyCTF{Ohh_no_my_web_has_been_hacked_4a2fac}
```

##### Solved by : viva03
