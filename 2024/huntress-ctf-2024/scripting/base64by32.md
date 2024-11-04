##### <- [Back to Huntress CTF 2024](../README.md)

---

# Base64by32 (Scripting)
Part of the Huntress CTF 2024

#### Description
`This is a dumb challenge. I'm sorry.`

### Attachments
`base64by32.zip`

### Solution
This being a `warmup` challenge, I was expecting it to be quite easy. Judging by the name of the chall, our first thoughts were immediately to take the provided chunk of encoded text and decode it with base64, 32 times. 

The script below was a quick remedy to automate churning through the decodes multiple times. Since I wanted to prep this script for future usage, instead of just using the while loop 32 times, I made it search for the flag prefix, therefore as long as it's assumed the end result will be in the proper flag format, the times it needs to iterate does not need to be assigned.

The `base64by32.zip` provided included only a plaintext file (no extension) which contained the initial base64 encoded blob of text.

```python
# Import packges
import base64

# Since the initial encoded string was very large in size, I opted to add it to a text file and import it that way. I could have just as easily made the file name be the one that is provided in the zip file. 
file_path = 'encoded.txt'

# Flag format 'prefix'
hunt = "flag{"

# Open the file in read mode
with open(file_path, 'r') as file:

    # Read the file and assign it
    code = file.read()

# Iterate through the loop until the 'hunt' text is found in the 'code' string
while hunt not in code:

    # Take the code, base64 decode it and assign it back to 'code'
    code = base64.b64decode(code).decode('utf-8')

# Print the resulting flag
print(f"Flag found: {code}")
```

#### FLAG
```
flag{8b3980f3d33f2ad2f531f5365d0e3970}
```
---

##### <- [Back to Huntress CTF 2024](../README.md)