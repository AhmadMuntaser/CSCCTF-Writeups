![image](https://user-images.githubusercontent.com/103259604/211188511-9d4c0056-9bba-4c85-9b00-b33ccd15f4c0.png)



After opening this .pcap file , first thing to do with any wireshar file is to check the Protocol Hierarchy Statistics

![image](https://user-images.githubusercontent.com/103259604/211188588-754b5801-bb53-41c4-8351-8509fef4df53.png)

we found that there is 84.2% of this capture file are on tcp protocol

So, filter on tcp and the follow the first tcp stream


![image](https://user-images.githubusercontent.com/103259604/211188612-34e1af6f-f5ee-49bc-ae42-99f58880358c.png)




in the first TCP stream we found this wierd nc -l -p 4444 > new_wallpaper_XD.jpg , which means its a shell from tha attacker


![image](https://user-images.githubusercontent.com/103259604/211188691-2d9f2ba9-eb00-4032-9f34-c40dc70e8acc.png)

and echo "I hacked you and replaced your wallpaper hahaha XD!" > pwned.txt command


if you follow to the next stream you will find a PNG Header at the beging of the file 

![image](https://user-images.githubusercontent.com/103259604/211188730-4971ad90-c870-446a-b02d-e56ca12f5156.png)

so what i need to do is to download it on my machine
so, convert the represntation of showing the data to RAW

![image](https://user-images.githubusercontent.com/103259604/211188762-83890daa-2bfa-4453-82d4-c2f9de19d3a6.png)

![image](https://user-images.githubusercontent.com/103259604/211188783-bc9d9f2c-7da8-469e-90a8-427cc0d7b605.png)

and then copy this RAW data and go to any online converter , to convert hex value to file

![image](https://user-images.githubusercontent.com/103259604/211188827-9daa0833-22ce-4590-a5ca-5d2aa1274f1f.png)

then click convert to download the image on your machine 
and here is your flag in that image
![image](https://user-images.githubusercontent.com/103259604/211188857-6e99207e-0f38-4721-af66-a462300cc5a4.png)







