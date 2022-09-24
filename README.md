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


## Question 7

>  Filter so that wireshark only picks up packets coming from your ip!

## Question 8

> Browse the flow of packets in the given .pcap file, look for useful information in the form of a conversation between two students regarding cheating in practicum activities. The conversation is reported to use a network protocol with a high level of reliability in its data exchange so you need to apply a filter with that protocol.


## Question 9

> There are reports of file exchanges made by the two students in the conversations obtained, look for the file in question! To facilitate reporting to superiors, name the file found in the format [group_name].des3 and save the output file with the name “flag.txt”


## Question 10

> Find the secret password (flag) of the above-mentioned underground organization!


