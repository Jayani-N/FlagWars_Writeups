# 1. I’m tryna put you in the worst mood, ah…

## Desc:

    > `Author : st3g0`
    
    **🎵 “I’m tryna put you in the worst mood, ah…”**
    
    A short audio clip from *Starboy* mysteriously glitches at one moment.  
    Participants report hearing NOTHING strange—  
    but secret analysis reveals otherwise.
    
    AUDIO FILE: https://drive.google.com/file/d/1Wcwq7kJzFk8Tsg9Dw5RIDnTaMvOdk-Yc/view?usp=sharing
    
    **Flag Format**: flagwars{...}


## Soln:

    Open the file in audacity or any audio spectogram visualizer and get the flag


## Flag:

    flagwars{daft_punk_mad_starboy}




# 2. One In A Hundred


## Desc:

    > `Author : st3g0`
    
    A glitchy matrix animation has been circulating.
    Nothing looks wrong. It's just a GIF.
    
    Download here: https://drive.google.com/file/d/1q99TwUxVJlFuymCEq8N76xF2k0xCn_m8/view?usp=sharing
    
     But somewhere inside, something was hidden —
     not visually, not audibly.
     **Structurally**.
    
     One frame carries something the others don't.
     Find it.
    
    **Flag format**: flagwars{...}


## Soln:

    STEP 1 — Recognise it's a GIF with frames
      file matrix_glitch.gif
      → confirms it's a GIF image
    
    STEP 2 — Split into frames
      Option A: Python
        from PIL import Image
        gif = Image.open('matrix_glitch.gif')
        for i in range(100):
            gif.seek(i)
            gif.copy().convert('RGB').save(f'frame_{i:03d}.png')
    
      Option B: ffmpeg (if installed)
        ffmpeg -i matrix_glitch.gif frame_%03d.png
    
      Option C: Online tool
        https://ezgif.com/split
    
    STEP 3 — Inspect each PNG frame for hidden chunks
      Option A: Python (fastest — scans all frames at once)
    
        import struct
        for i in range(100):
            with open(f'frame_{i:03d}.png','rb') as f:
                data = f.read()
            pos = 8
            while pos < len(data):
                length = struct.unpack('>I', data[pos:pos+4])[0]
                ctype  = data[pos+4:pos+8].decode('latin-1')
                if ctype == 'tEXt':
                    chunk_data = data[pos+8:pos+8+length]
                    null_idx   = chunk_data.index(0)
                    keyword    = chunk_data[:null_idx].decode()
                    value      = chunk_data[null_idx+1:].decode()
                    print(f'Frame {i}: tEXt [{keyword}] = {value}')
                pos += 4 + 4 + length + 4
    
      Option B: pngcheck (one file at a time)
        pngcheck -c frame_065.png
    
      Option C: exiftool (limited but works)
        exiftool frame_065.png
    
    STEP 4 — Find frame 65
      Frame 065 contains a tEXt chunk:
        keyword : flag
        value   : flagwars{fr4m3_65_png_chunk_hunt}


## Flag:

    flagwars{fr4m3_65_png_chunk_hunt}

# 4. Active Surveillance

## Desc:

    >`Author : EnCase`
    
    We’ve been monitoring him for weeks.

    Calls. Messages. Movements.

    Tonight, at 21:43, he placed a short phone call to an unknown number.

    The conversation itself wasn’t important — mostly small talk.

    But something in the background caught our attention.

    A faint announcement.
    Distorted. Muffled. Almost drowned out.

    He never mentioned where he was.
    He didn’t have to.

    We believe that background audio reveals his location at the time of the call.

    Identify where he was when this call was made.

    Flag format: flagwars{origin-destination-time}

    For example:

    flagwars{jammu-punjab-11:11}

    https://drive.google.com/file/d/1hGy3U9Mz23FSrsffsxCQ6kxUA7DVpNms/view?usp=drive_link

## Soln:

    Reverse the video and google translate from malayalam.

## Flag:

    flagwars{mangalapuram-chennai-19:35}
