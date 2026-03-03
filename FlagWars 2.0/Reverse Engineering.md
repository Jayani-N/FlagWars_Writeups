# 1. The Distorted Truth

## Desc:

    >`Author : EnCase`
    
    We found a small Linux binary that claims to validate a flag.

    It doesn’t seem to do much, just takes input and says “Wrong!”.

    There’s no server, no network, no tricks.

    Maybe the answer is hidden in how it checks, not what it prints.

## Soln:

    Open the binary in Ghidra (or IDA).

    Notice:

    Length check = 33

    memcmp against a target byte array

    Each byte is transformed before comparison.

    Identify the transformation:

    XOR 0x5A

    + 7

    ROTL 1

    Reverse the operations in reverse order:

    ROTR 1

    Subtract 7

    XOR 0x5A

    Apply these reverse operations to every byte in the target array.

    Convert resulting bytes to ASCII.


## Flag:

    flag{r3v3rs3_1s_fun_1nd33d!_1480}

# 2. Miscalculated

## Desc:

    >`Author : EnCase`
    
    Everything seems correct.

    Length matches.
    Characters match.

    Yet it still says no.

    Maybe the mistake isn’t yours.

## Soln:

    Open binary in Ghidra (or use strings).

    Find the secret string:
    hncizyctu}gcu{tgxgtug

    See the check logic:
    input[i] + 2 == secret[i]

    So subtract 2 from each character of the secret.


## Flag:

    flagwars{r3v3rse_3ngg_1s_s1gn1f1c4nt}
