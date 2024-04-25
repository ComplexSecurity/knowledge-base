**FTP (File Transfer Protocol)** is a standard network protocol used for the transfer of files from one host to another over a [[Transmission Control Protocol|TCP]]-based network, such as the Internet.

FTP works by opening two connections that link the computers trying to communicate with each other. One connection is designated for the commands and replies that get sent between the two clients, and the other channel handles the transfer of data. 

During an FTP transmission, there are four commands used by the computers, servers, or proxy servers that are communicating. These are “**send**,” “**get**,” “**change directory**,” and “**transfer**.”

While transferring files, FTP uses three different modes: **block**, **stream**, and **compressed**. The stream mode enables FTP to manage information in a string of data without any boundaries between them. The block mode separates the data into blocks, and in the compress mode, FTP uses an algorithm called the Lempel-Ziv to compress the data.

