# Picture This (150 points)

## Description:
A dusty zip was found stuffed with snapshots from a childhood afternoon — small, silly frames of two friends forever frozen in mischief. One of them is a red herring; the rest whisper fragments of something more. Each picture keeps a quiet note, and together they tell a secret. Gather the pieces, put them in the right order, and the whole story will reveal itself.

## Solution:
Open the zip file and move into the childhood folder. You can find 5 images. Run exiftool on each image in Kali Linux and find the flag split into parts and each part present in the comment section of the metadata. 
Alternatively you can also run an online exiftool through the images. For this, go to https://exif.tools/ and upload each image one by one.

![alt text](image.png)

We get, _ doraemon_guides _

![alt text](image-1.png)

We get, flagwars{when_timeless_

![alt text](image-2.png)

We get, nobita_home}

![alt text](image-3.png)

We get, gadgets_whisper_

<img width="742" height="353" alt="Screenshot 2025-10-12 163139" src="https://github.com/user-attachments/assets/8865fa71-3f8f-4c60-ba6a-c5f3a1fceb6a" />

We get, daring_solaces

Now assemble them in the right order to get the full final flag.

## Flag:
flagwars  {when_timeless_gadgets_whisper_daring_solaces_doraemon_guides_nobita_home}
