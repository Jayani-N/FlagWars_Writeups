Challenge name: Kaukabe Defence Force

Challenge Type: WEB

Description :
Shinchan’s day off turned into a mystery — Shiro ran off chasing something shiny and now the little rascal refuses to admit he lost him. Your job is simple in words and tricky in practice: help Shinchan find Shiro. The clues are scattered across the site: a few well-hidden pages, a whisper in the source, and an image that’s keeping secrets beyond what you can see.

This challenge rewards careful reconnaissance, a little decoding, and the patience to follow a chain of small hints. It isn’t about brute force — it’s about noticing the things most players ignore. If you reach the right place and extract what’s hidden in the homeowner’s cover photo, you’ll learn where Shiro is hiding.

Flag format: flagwars{...}

URL : https://kasukabedefenceforce.netlify.app/

Solution:

    Step 1: Change the URL of https://kasukabedefenceforce.netlify.app/ into https://kasukabedefenceforce.netlify.app/robots.txt
    
    Step 2: Now You get the page as

<img width="1372" height="391" alt="image" src="https://github.com/user-attachments/assets/e5c6a16f-615f-418b-a069-097d2e93c97d" />

    Step 3: Now change the URL again to https://kasukabedefenceforce.netlify.app/sitemap.xml
    
    Step 4: You get the page as 

<img width="1274" height="416" alt="image" src="https://github.com/user-attachments/assets/799df2a0-3063-4366-bae5-b06654658393" />

    Step 5: Now change the URL to the given format {http://example.com/private/9f3a2c.html} such as https://kasukabedefenceforce.netlify.app/robots.txt/private/9f3a2c.html
    
    Step 6: You get the page as 
    
<img width="1295" height="982" alt="image" src="https://github.com/user-attachments/assets/f1bf546d-3993-40ec-a908-08ea81b1a295" />

    Step 7: Now download the given image and perform exiftool command on the image in kali or use and online exiftool such as https://www.metadata2go.com/ upload the image and view the metadata.
    
    Step 8: In the comment section you can see the flag --> flagwars{shinchan_spicy_kasukabe_dancers}

flag: 
flagwars{shinchan_spicy_kasukabe_dancers}
