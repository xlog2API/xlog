Newest douyin/tiktok encryption for validating devices...
Necessary for new devices being validated through newest apk version
Can be encrypted/decrypted.
mssdk 

![MSSDK_ENDPOINT](https://user-images.githubusercontent.com/111660587/187089624-ced03b4f-6717-45c1-b893-07263e0f9cb9.png)


Encryption in hex format...


![HEX](https://user-images.githubusercontent.com/111660587/187089684-158fd031-7736-4388-8424-de85b8e1c279.png)

we will be doing some analysis here with updates 

first decompile latest tiktok apk using jadx
after searching around for a bit we stumble upon hashmap values...
in function LIZIZ() mostly obfuscated funcs to prevent snooping.
![dbebada1bc4f3a49cff69206628a7da9](https://user-images.githubusercontent.com/111660587/187262250-bfa4db7d-a630-45d1-bca0-5833419d0681.png)

