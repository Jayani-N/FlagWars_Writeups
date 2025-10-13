Challenge name: Willy Wonka

Challenge Type: CRYPTOGRAPHY

Description :Deep within the crumbling halls of the Wonka Chocolate Factory, a dusty ledger is found locked inside a glass vault.
On the first page, written in purple ink, is a riddle:

“The candy that never melts hides the key to my sweetest secret.
Only those who can unwrap the old seal shall taste the forbidden formula.”

Rumor has it that Willy Wonka left behind one final recipe "The Everlasting Gobstopper 2.0", a candy that can replicate infinite flavors from memory. But to prevent it from falling into the wrong hands, he encrypted it once using modern magic.

Now, you the newest intruder in the chocolate factory must decipher the vault and uncover the lost formula.

Solution:

Step 1: Parse the public key to get n and e
Step 2: Open rsa.pub in a text editor and copy the whole PEM text (the -----BEGIN PUBLIC KEY-----… block), or the n/e values if they are already plain.

Step 3: Paste that PEM into an online PEM/RSAPub parser (it shows Modulus (n) and Exponent (e)). Use the PEM parser / RSA tools page. 
8gwifi.org

Result: note down the modulus n (a big integer) and exponent e (often 65537).

2) Factor the modulus n (find p and q)

Step 4: Paste the decimal (or hex) value of n into FactorDB (search box) or use a factoring site (Alpertron ECM) if FactorDB doesn’t already have factors. FactorDB will show p and q if known; Alpertron can try to factor it for you. 
factordb.com
+1

Step 5: If FactorDB already lists factors: copy p and q.
If not, run the Alpertron/ECM factor tool and wait for it to finish factoring.

3) Compute the private key (or directly decrypt) and decrypt the ciphertext

Step 6: Now that you have p, q, and e, go to an online RSA tool that accepts p, q, e (or that computes the private exponent d) and lets you decrypt a ciphertext (dCode or similar RSA calculator). Paste p, q, e, and your ciphertext from rsa.txt (select correct input encoding: hex or base64 — check the file contents). 
dcode.fr
+1

Alternative Methods:

Steps on that site:

Step 1: Enter p and q (and e if requested). The tool will compute d.

Step 2: Paste the ciphertext (rsa.txt) into the ciphertext box. Choose the right input format (hex or base64).

Step 3: Click Decrypt → the site returns the plaintext bytes / ASCII.

Notes on ciphertext format

Step 4: If rsa.txt looks like random hex characters (0-9a-f), tell the decryptor it’s hex.

Step 5: If it’s A–Z a–z + / = characters, it’s base64.

If it’s binary, you may need to open it in a hex editor and copy hex.

flag: 
flagwars{chocolate_factory_secrets}

