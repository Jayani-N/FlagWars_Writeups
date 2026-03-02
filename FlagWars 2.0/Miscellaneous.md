# 1. Discord Server

## Desc:

    >`Author : EnCase`
    
    Hidden secrets lie across the server… 🗝️

    Your mission: explore, search carefully, and uncover all the pieces of the ultimate flag.

    Only those who find every part will be able to assemble the legendary code.

    Are you ready to begin the hunt? ⚡

## Soln:

    Join the Discord Server and get your CTF Player role. 
    First part: in the description of #announcements channel 
    Second part: in the #discord-challenge channel
    Third part: in the bottom left corner of the picture posted in the #starbucks channel
    Fourth part: in the filename of the picture in the #motivation channel.
    Fifth part: in the bio of the user - EnCase

## Flag:

    flagwars{welcome_to_the_s3cre77ttt_server}

# 2. The Conversation That Never Happened

## Desc:

    >`Author : EnCase`
    
    A shared AI transcript was circulated briefly before being pulled.

    According to the sender, nothing was deleted.

    According to everyone else, it was never accessible.

    Only one of them is wrong.

    *9 to 5* jobs are stressful!

    Link: https://chatgpt.com/share/699d9a89-80b8-8012-8fd0-5b5262f24bc9

## Soln:

    Change the last digit of the URL from 9 to 5. And then use ROT47 on the encrypted text in that chat.

## Flag:

    flagwars{y0u_f0und_ma_s3cr3t!}   

# 1. Brobot

## Desc:

    >`Author : EnCase`
    
    You are given access to a Telegram bot that claims to be very helpful.

    It even offers help — though not always the same kind of help every time.

    Sometimes the bot prefers things explained *verbosely*.

    Sometimes it refuses to act unless you’re being *fully* clear.

    And sometimes it hears you… but won’t actually *execute* anything unless you really mean it.

    The bot talks a lot, but don’t trust everything it says.

    What matters is how it behaves — especially after you ask for help again.

    If you learn how to communicate with it properly, it might eventually reveal something it wasn’t supposed to.

    Hint: start interacting with the bot using /help
## Soln:
    First use /help to find out what all commmands can be used. 

    Then /check2 verbose

    Then /help again. You see some more commands now

    Then /diag full

    Then /help again. You see even more commands

    Then /mem_read

    Then /io_status

    Then /ctrl_seq execute

    Then you get the flag 
    
## Flag:

    flag{br0_b07_15_4_sm4r7_b0t_2233}

# 4. Secret Emoji Log

## Desc:

    >`Author : EnCase`
    
    🔥🍋🍎🔫⌚🍎🌧🐍{🥚🎬😲🧃🧊_🎯🥚🚕😲🎯🥚_🔥☂💅}

## Soln:

    First letter of each emoji

## Flag:

    flagwars{emoji_decode_fun}
