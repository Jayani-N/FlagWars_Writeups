Challenge name: Mina's Birthday

Challenge type: OSINT

Description:
Mina’s friends threw her a secret birthday scavenger hunt — she posted silly pictures and little lies about being “so forgetful” — but if you pay attention, Mina left breadcrumbs across her profile. The challenge is simple to state and tricky to finish: piece together Mina’s birthday and her favourite colour from scattered clues on her profile and posts, then submit the flag in the format 

Flag Format: flagwars{DD_Month_color}.

user id: mina.memories_

Solution:
Step 1: Give a follow request to the account.

Step 2: After acception of the follow request you can see the notes in the instagram page.

Step 3: The notes state that "bGlsYWM=" which is a base- 64 code.

Step 4: On decoding in "https://gchq.github.io/CyberChef/" you get the plaintext as "lilac" which is mina's favourite colour.

Step 5: The name of the account is "mina30" which indicates her birthdate as 30.

Step 6: In the bio we have a binary number as 01101101 which is binary charecter of 'm' which denotes the month "march"

Step 7: The Bio has the information that "we three bears" and "my fav @03: me,juan,tina" where the "@03" indicates the month march.

Flag:
flagwars{30_march_lilac}

