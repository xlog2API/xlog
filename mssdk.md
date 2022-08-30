we will be doing some analysis here with updates

Newest douyin/tiktok encryption for validating devices...
Necessary for new devices being validated through newest apk version
Can be encrypted/decrypted.
mssdk 

![MSSDK_ENDPOINT](https://user-images.githubusercontent.com/111660587/187089624-ced03b4f-6717-45c1-b893-07263e0f9cb9.png)


Encryption in hex format...


![HEX](https://user-images.githubusercontent.com/111660587/187089684-158fd031-7736-4388-8424-de85b8e1c279.png)
 

we can inject straight into some dynamic library / shared object

first decompile latest tiktok apk using jadx

after searching around for a bit we stumble upon hashmap values...
in function LIZIZ() mostly obfuscated funcs to prevent snooping.

![dbebada1bc4f3a49cff69206628a7da9](https://user-images.githubusercontent.com/111660587/187262250-bfa4db7d-a630-45d1-bca0-5833419d0681.png)

#investigating web mssdk encryption we see that the response is base64 encoded 

#we will investigate in depth both encryptions should be the same 

![mssdk web](https://user-images.githubusercontent.com/111660587/187497024-570d0c51-bfdd-4951-97a1-5c64aeb02164.png)

After going through many requests in web we sift through some js files and we have found obfuscated functions 

or follow this link and inspect source 
https://sf16-secsdk.ttwstatic.com/obj/rc-web-sdk-gcs/webmssdk/1.0.0.412/webmssdk.js


After looking at each function we can see this from this file in formatted version...


Time to go through each obfuscated function one by one this can be the confusing/tricky part but it can be done through this file...
![mssdk obfuscation](https://user-images.githubusercontent.com/111660587/187560756-0143d37a-a15d-489a-97f1-13808f9f545f.png)


we take a look at some functions in this file... and found 
![js file mssdk](https://user-images.githubusercontent.com/111660587/187560875-52e37b7e-ddd8-4aa5-9efb-c308bec9cdb6.png)


Try and follow the obfuscated function...no more updates for now....




