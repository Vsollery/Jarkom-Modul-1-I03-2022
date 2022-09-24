# Jarkom Modul-1-I03-2022

Computational Networking Module 1 Practicum Report

* Selomita Zhafirah 5025201120
* Venia Sollery Aliyya Hasna 5025201161
* Erlangga Wahyu Utomo 5025201118

## Question 1

> Mention the web server used on "monta.if.its.ac.id"!

Firstly, we will open wireshark and use filter "http.host == "monta.if.its.ac.id"

![Number1](/screenshots/no%201a.jpeg)

Then, right click on the Hypertext Transfer Protocol and follow TCP stream

![Number1](/screenshots/no%201b.jpeg)

It will show server : **nginx/1.10.3**

## Question 2

> Ishaq was confused looking for TA topics for this semester, then he came to the monta website and found the topic details on the website “monta.if.its.ac.id”, what TA title did Ishaq open?

## Question 3

>  Filter so that wireshark only shows packets going to port 80!


## Question 4

> Filter so that wireshark only picks up packets coming from port 21!

For this question we can use `tcp.srcport == 21` to pick up packets from port 21

![Number4](/screenshots/no%204.jpg)


## Question 5

> Filter so that wireshark only picks up packets coming from port 443!

Using the command `tcp.srcport == 442` to filter out packets coming from port 443. src is where the packets comes from.

![Number5](/screenshots/no%205.png.jpg)


## Question 6

> Filter so that wireshark only shows packets going to lipi.go.id !

ip going to lipi.go.id

<img width="866" alt="image" src="https://user-images.githubusercontent.com/87944227/192083671-627d34a6-6afd-48b0-a351-537d3486c706.png">


## Question 7

>  Filter so that wireshark only picks up packets coming from your ip!

IPv4 address : 192.168.1.24, Using ip.src_host ==  192.168.1.24 to  picks up packets coming from your ip

<img width="904" alt="image" src="https://user-images.githubusercontent.com/87944227/192083651-176679a8-a451-498f-b89d-de66385d1afb.png">

<img width="898" alt="image" src="https://user-images.githubusercontent.com/87944227/192083694-22c90d59-6310-49c5-b15b-a95d0647caec.png">


## Question 8

> Browse the flow of packets in the given .pcap file, look for useful information in the form of a conversation between two students regarding cheating in practicum activities. The conversation is reported to use a network protocol with a high level of reliability in its data exchange so you need to apply a filter with that protocol.

First thing we do is right click and follow TCP stream PSH.

<img width="1121" alt="image" src="https://user-images.githubusercontent.com/87944227/192083097-682d2475-95a8-466e-bb6d-2eedb63fcc1b.png">

Here is the TCP Stream

<img width="1122" alt="image" src="https://user-images.githubusercontent.com/87944227/192083151-d7978235-8a18-4c5e-9c69-5b72ca62eee9.png">

In the picture above there are conversation between two students, and when clicking the entire conversation we get the ip and port. 

<img width="1125" alt="image" src="https://user-images.githubusercontent.com/87944227/192083167-79ca3ce6-aaa4-4a88-8120-c42c4d90bf0d.png">

In conclusion, the filter that can be use is (ip.src == 127.0.0.1 ||  ip.dst == 127.0.0.1) 

<img width="984" alt="image" src="https://user-images.githubusercontent.com/87944227/192083196-258849fd-3508-4f6d-b62d-1d3bb8a2c750.png">

## Question 9

> There are reports of file exchanges made by the two students in the conversations obtained, look for the file in question! To facilitate reporting to superiors, name the file found in the format [group_name].des3 and save the output file with the name “flag.txt”

We can see in the conversation from stream 12 that we need to decrypt a file using openssl.

<img width="800" alt="image" src="https://user-images.githubusercontent.com/87944227/192083227-f3b656fa-8164-428e-97a9-64cb0acdb380.png">

Using stream tcp.stream eq 29 we can get the encrypted file. 

<img width="796" alt="image" src="https://user-images.githubusercontent.com/87944227/192083240-38cba664-74cd-4020-9bfa-ebf764f95584.png">

we will save that file to be decrypted. 

<img width="797" alt="image" src="https://user-images.githubusercontent.com/87944227/192083251-1f1fa40a-099d-4551-97e3-e3c780b56bc9.png">

In the screenshot above we are decrypting the daved file with the password nakano.

<img width="506" alt="image" src="https://user-images.githubusercontent.com/87944227/192083281-8f1bcb85-529e-42e6-a7e0-d7a75ea8124e.png">

Results of the encrypted file. 


## Question 10

> Find the secret password (flag) of the above-mentioned underground organization!

The secret password is : nakano

