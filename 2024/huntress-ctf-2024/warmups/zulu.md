##### <- [Back to Huntress CTF 2024](../README.md)

---

# Zulu (Warmups)
Part of the Huntress CTF 2024

### Description
`Did you know that zulu is part of the phonetic alphabet?`

### Attachments

`zulu`

### Solution

This chall comes with a file, so let's download that file in our VM. After downloading it, I open up a terminal, navigate to my `~/Downloads` directory and run `file zulu`

![alt text](img/zulu-01.png)

My VM shows the icon of a compressed object (like a .zip, for example) but it just won't decompress. I searched for `compress'd data 16 bits` and the results talked about a `.z` file. Since the name of the chall is `Zulu`, that kind of makes sense. 

Trying to `uncompress` the file as is, just won't work for me, so I first `mv` the file so I can add the `.z` extension to it.

![alt text](img/zulu-02.png)

Ok, let's try to `uncompress` it again.

![alt text](img/zulu-03.png)

Let's look to see what the output was

![alt text](img/zulu-04.png)

Looks like we have a 'zulu' file again (without an extension). Let's `cat` that file and see what we have.

![alt text](img/zulu-05.png)

And there is the flag!

#### FLAG
```
flag{74235a9216ee609538022e6689b4de5c}
```
---

##### <- [Back to Huntress CTF 2024](../README.md)