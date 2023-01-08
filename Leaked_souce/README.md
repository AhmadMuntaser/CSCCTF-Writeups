![image](https://user-images.githubusercontent.com/103259604/211189475-ef012d61-6fee-4aad-92a3-9a153c80b93a.png)


download the souce files , you will find a fake flag
![image](https://user-images.githubusercontent.com/103259604/211189522-a000a2dd-8f28-40bf-a00b-9f58ff41371b.png)


there is a Hint for this challenge that says "Check hidden files in the source"

so , i found .git folder was hidden in the source files

![image](https://user-images.githubusercontent.com/103259604/211189555-b346caba-5129-4e58-adc4-a463f3bbc4ea.png)

enter the command git show to view expanded details on Git objects such as blobs, trees, tags, and commits.

![image](https://user-images.githubusercontent.com/103259604/211189589-ace7efa2-ced2-417e-a0ab-537cc7949be8.png)

here is our secret that we will need it later on



in the source file we can found a database file with username for Rick & Morty

![image](https://user-images.githubusercontent.com/103259604/211189674-03de5351-d423-466a-807e-fa73dbe59ad0.png)

the idea on this challenge is based on Json Web Tokens (JWT)


JWT is a proposed Internet standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims.
The tokens are signed either using a private secret or a public/private key. and its used for authentication.


so lets try to login by Morty user and intercept the request using Burp suit


![image](https://user-images.githubusercontent.com/103259604/211190303-2d8b47d4-f3b8-4069-afe8-ab6251b80862.png)


thats the JWT for morty user, but i need to login as Rick user
but i dont have his password
So , what we can do is going to https://jwt.io/ and paste Morty JWT on this website

![image](https://user-images.githubusercontent.com/103259604/211190446-a8aa1b6b-ef5b-4244-91fa-30d23c0df900.png)


![image](https://user-images.githubusercontent.com/103259604/211190534-b3cbc9ba-dca3-4c21-bd80-36d996695816.png)
Here we need to modify morty user to Rick
and we need to put our secret key tha we found from the souce code "sUp3r_JWT_k3y_ADMIN" as shown in this screenshot

![image](https://user-images.githubusercontent.com/103259604/211190600-945cb52b-619f-4165-85e3-6ff0451fb5a0.png)




then you need to copy this decoded JWT and put it back in the request cookie on burp as show

![image](https://user-images.githubusercontent.com/103259604/211190714-babd7297-b3f3-4e92-9f5b-6dc415b08287.png)


and here is your flag
