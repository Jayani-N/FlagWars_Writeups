# 1. Echoes of an Old Website

## Desc:


    > `Author : st3g0`
    
    A small personal site once existed at the domain:
    https://myport-rho-two.vercel.app/
    
    It went offline two years ago.
    But the internet never forgets.
    
    Someone told us the site accidentally exposed a secret in one of its early versions.
    
    **Flag format**: flagwars{...}
    
    No brute-force, no exploitation.
    Just… look into history.
    
    Good luck, archivist.


## Soln:

    Search for the exact link in the web archive to see the saved snapshots
    
    In one of the snapshot->by viewing the source code->you'll get an internal token leaked which is actually b64 encoded (ZmxhZ3dhcnN7eTB1X2ZvdW5kX3RoM19lY2gwX2luX3RoM19hcmNoMXYzfQ==) ->decode it->get the flag


## Flag:

    flagwars{y0u_found_th3_ech0_in_th3_arch1v3}



# 2. Footprints in the Noise

## Desc:

> `Author : st3g0`

    A mysterious traveler leaves no public profile behind…  
    Except for one image we recovered from their device.
    https://drive.google.com/file/d/1vL0aOfEIs9ZtGkVK5Ccrkn-KxONiSirb/view?usp=sharing
    
    Somewhere inside this photo lies a clue to their identity.
    
    Once you find it, track their online presence.
    
    When you discover all three accounts, combine the fragments to form the flag.


## Soln:

1. Given a image which clearly is a picture of sherlock-> hints at using sherlock command to find the username across different platforms.
2. To find the username first-> check the metadata of the image (using exiftool or any online metadata viewer)-> it has "cyberwanderer_00x" in author tag
3. Use either google dorking to find different platforms existing for that username or sherlock command in kali
4. P1-> Instagram bio-> P1: flagwars{osint
5. P2-> github status in profile-> p2: _sher
6. P3-> twitter acc (x.com)-> go to profile->replies section->find the comment-> p3:lock_master}

   ![writeup](https://github.com/user-attachments/assets/c80f3e14-8706-4e04-a969-d6538f27c3af)
   <img width="510" height="668" alt="image" src="https://github.com/user-attachments/assets/7808fbfa-9dfc-4cb4-98c6-c05d8d9401a2" />
   <img width="597" height="685" alt="image" src="https://github.com/user-attachments/assets/c94297b8-8058-4c6c-b886-0bed281a3ef6" />



## Flag:

    flagwars{osint_sherlock_master}




# 3. The City That Doesn’t Exist


## Desc:

    > `Author : st3g0`
    
    **Flag Format**: flagwars{lat_lon}
    
    NOTE:  round it to 4 decimal places
    
    Find the image here:
    https://drive.google.com/file/d/1HycVh0p0qjfH5p-nsAmZjXEClnUFqQHK/view?usp=sharing



## Soln:

    Use google image search to find the place and its coordinates

    <img width="1645" height="786" alt="image" src="https://github.com/user-attachments/assets/e80364fd-e893-47d4-a2a1-661690e8ddaa" />



## Flag:

    flagwars{18.3232_-64.7662}




