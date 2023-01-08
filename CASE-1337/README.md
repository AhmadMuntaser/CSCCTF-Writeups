# CSCCTF-Writeups



Hello guy Here's my Writeups for the Forensics challenges:


![case-1337](https://user-images.githubusercontent.com/103259604/211186860-b5f5327b-fb19-4d32-b566-ca67c1e579e0.png)



in this cahllenge you have to investigate a disk image that is given in the challenge
i used Autopsy Tool do my investigation ana analyze this image



![image](https://user-images.githubusercontent.com/103259604/211187230-7d2bb7ee-d343-43ba-9d81-31549392a4b8.png)

after searching for any information we found a flag.db file wich means a database folder


![image](https://user-images.githubusercontent.com/103259604/211187244-17660da6-4161-4733-bb1e-bc52e3a4401c.png)

Right-click on the file then ==> Extact files(s) to download this flag.db on your Desktop



we found another intersting file under the /home/akashi/CASE-1337/shadystuff directory 
and i do extarct flag.zip to my desktop 

![flag](https://user-images.githubusercontent.com/103259604/211187547-c2955e57-a82f-4c28-aa21-27bdff85cf88.png)

if we opend this file we will found flag.db file inside it , but we can't open it ,it needs a password
we tried to brute force the password uzing fcarckzip tool on my kali linux machine , but it seems its not brute forceable

![image](https://user-images.githubusercontent.com/103259604/211187748-a22e81b3-bca7-429c-ab6f-b3b6202c9409.png)

So i keep loking for any new information tha could help me to find the key


![image](https://user-images.githubusercontent.com/103259604/211187807-d41877a5-1ceb-4f9c-915a-581a280e08f4.png)

in the /home/akashi/CASE-1337 directory we found this wierd message.mp3 , so i extact it , and after listening to this message , it tells me that his database file password is in /etc/8ea00242ac.txt 

![image](https://user-images.githubusercontent.com/103259604/211187825-866a3025-a880-4b5d-adde-abcae6d10872.png)



so here is the password 

![image](https://user-images.githubusercontent.com/103259604/211187887-5d667c2b-189e-44b6-b421-4fa5827d8789.png)
 copy this password and paste it on the flag.db file
 
 ![image](https://user-images.githubusercontent.com/103259604/211187919-6055e646-8a84-4915-b4cc-aef1d5a8a819.png)



we found that its an sqlite3 database
![image](https://user-images.githubusercontent.com/103259604/211187935-98baca60-6b5c-4c27-813d-be5106232b47.png)




one more step to get the flag, you can open your terminal ,cmd, or powershell, and go to the directory that this flag.db is located on your own machin
then type the following command
sqlite3 flag.db and follow my steps in the following screenshot

![image](https://user-images.githubusercontent.com/103259604/211188059-f8d9d4bc-a8c9-449e-9330-5b62297e3541.png)

and here is your Flag.














