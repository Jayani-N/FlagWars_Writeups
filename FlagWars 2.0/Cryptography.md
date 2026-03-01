# 1. Collide Me If You Can

## Desc:

    >`Author : st3g0`
    
    A legacy authentication system still uses **MD5** to verify file integrity.
    
    The system verifies files by checking:
    MD5(uploaded_file) == stored_MD5
    
    Your job?
    
    Create a **different file with the same MD5 hash** as verified.bin (attached in the website)
    When you upload a colliding file, the system reveals the flag.
    Upload the file here-> https://collide-1.onrender.com


## Soln:

    The system verifies files by checking:
    MD5(uploaded_file) == stored_MD5
    
    Create a **different file with the same MD5 hash** as verified.bin (attached in the website)
    When you upload a colliding file, the system reveals the flag.

    Example working file:  https://drive.google.com/file/d/1vrACSjwukaDxyJ5tQ2Xcw1ydZk01UQXd/view?usp=sharing

## Flag:

    flagwars{md5_collision_master}





# 2. Calm Down

## Desc:

    > `Author : st3g0`
    
    Someone intercepted a suspicious encoded message. 
    https://drive.google.com/drive/folders/1n0P4ml0EwUt1Sptp-ueUrQkiWd9b7e9u?usp=sharing
    
    Attached to it was a crumpled note that just said:
     
    "baby calm down, calm down - **the key** is how many times he says 'calm down' in the chorus. (it's not 4. it's not 2. calm down and count.)"
    
    The message looks like gibberish — or does it? **The first half of the flag is buried inside**.
    
    But that's only half the story. The sender also left behind an official song credits PDF. Nothing suspicious about it. Just a normal credits sheet. Totally normal.
    
    ...**look at who's featuring**. carefully.


## Soln:

    STEP 1 — Caesar Cipher (challenge.txt)
    Ciphertext received:
    fdop grzq, fdop grzq
    edeb, edeb, edeb...
    wkh iluvw kdoi ri zkdw brx vhhn lv klgghq khuh:
    iodjzduv{fdop_grzq_
    
    Caesar shift = 3
    (Rema says "calm down" 3 times in the chorus)
    
    Decrypted:
    igrs juct, igrs juct
    hghe, hghe, hghe...
    znk loxyz ngrl ul cngz eua ykkq oy nojjkt nkxk:
    lrgmcgxy{igrs_juct_
    
    First half of flag: flagwars{calm_down_
    
    STEP 2 — PDF Initials (song_credits.pdf)
    Read FIRST LETTER of each artist in "ADDITIONAL FEATURING ARTISTS":
    
      Ivan Turner-Smith     → I
      Tems                  → T
      Sia Konstantinidis    → S
      Juice WRLD Estate     → J
      Usher Raymond         → U
      Summer Walker         → S
      Ty Dolla $ign         → T
      Chris Nolan-Beats     → C
      Raye                  → R
      Young Jonn            → Y
      Patoranking           → P
      Tekno Miles           → T
      Omah Lay              → O
    
    Initials: i t s j u s t c r y p t o
    With underscores + closing brace: its_just_crypto}
    
    Second half of flag: its_just_crypto}
    
    COMBINE
    flagwars{calm_down_ + its_just_crypto} = flagwars{calm_down_its_just_crypto}


## Flag:

    flagwars{calm_down_its_just_crypto}
