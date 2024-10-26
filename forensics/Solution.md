# Corrupted Hard Drive

![image](https://github.com/user-attachments/assets/47162803-d1a3-4b61-a2cd-1a715d507989)

## Analyzing part.

This is the challenge that we need to answer various of question to get the flag. I will do each Question.

### Walkthrough

Q1. What is the starting address of the LBA address? Format (0xXXXXX)

Firstly, LBA in partition is determined by the offset from the beggining of the disk to the first sector of the partition.

When analyze the disk, I found that the partition starts at sector 128 => Starting Address = 0x10000 => Answer

Q2. What is the tampered OEM ID? Format (0xXXXXXXXXXXXXXXXX)

In this challenge, we have to find OEM ID. OEM ID is a series of characters identifying the file system, such as NTFS, exFAT, etc.

It often located at offset 3.

![image](https://github.com/user-attachments/assets/e10f19e2-55e7-41f5-ae75-c0d17c39a679)

This is an example of how to find OEM ID. By that, I use hxd to open disk file and find the byte at offset 3.

![image](https://github.com/user-attachments/assets/7b605c03-9aef-49d3-95cb-171e328d3930)

Answer: 0x4E54460020202020

Q3. After Fixing the disk, my friend downloaded a file from Google, what is the exact time when he clicked to download that file?

I actually think they must renamed to what time the file downloaded, but anyway, When open Autopsy and go to the web downloads function in Autopsy

![image](https://github.com/user-attachments/assets/8167defc-aab0-45cf-9417-a6a3ef81c4a1)

After that, we know that the file is Blue_Team_Notes.pdf and it's in MustRead folder. Go to it

![image](https://github.com/user-attachments/assets/dd71b458-aa3f-49a3-822c-8d4ab69d0297)

We will take the Created Time then convert it to UTC timezone => 2024-10-22 21:51:13

Q4.  How much time did that file take to for download (in seconds)??

At this question, I know that when we download, it will create a file called .crdownload or something. We can parse 2 both **$LogFile** and **$UsnJrnl** to find that. At this challenge, I use **$Logfile**

After open, I found that there is different in time so it might be the answer

![image](https://github.com/user-attachments/assets/722254d7-a5fb-4667-8dcb-041137cd73d0)

(Actually I'm tired to find the collumn so I bruteforce the time) => Answer: 126

Q5. The first directory he moved this file to?

At this challenge,







