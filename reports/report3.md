# CSE 15L Lab Report 3
## I am reporting on Group Choice Option 2
## Table of Contents
- [Public Key](#public-key)
- [Private Key](#private-key)
- [Using `git` commands from `ieng6`](#using-git-commands-from-ieng6)
- [Commit link](#commit-link)
## Public Key
Here is my public SSH key in GitHub:<br>
![public SSH key in GitHub](lr3-github-public-key.png)
By connecting my public SSH key on GitHub, I can commit changes to my repositories via `git push`. Since I am the only person with commit access on my repositories, GitHub needs to check if I have the proper permissions to push to my repositories, which they do by checking the public `ssh` key I provided against my public and private `ssh` keys in my `.ssh` folder. Since the two match, I am authenticated as [Akhil841](https://github.com/Akhil841) and thus the pushed changes are accepted and the repository is modified.<br>
Here it is on my `ieng6` account, in the directory:
![public SSH key on ieng6](lr3-github-public-key-dir.png)<br>
It's the file named `id_rsa_github.pub`.<br><br>
Here are the contents of my public key:
![public SSH key on ieng6 contents](lr3-github-public-key-contents.png)<br>
The `$` indicates that there is more text past the edge of the window, but it would be cumbersome to get the entire thing into one image.
## Private Key
Here is my private SSH key on my `ieng6` account:<br>
![public SSH key on ieng6](lr3-github-public-key-dir.png)<br>
It's the file named `id_rsa_github`.<br>
From what I understand, when authenticating myself, my private key is hashed and the hash is compared with both the public key on my computer and the public key I stored on GitHub. If the two match/check out, the commits and pushes I make towards my repositories go through. The reason that we have both a public and a private key is anyone can see the public key, so the private key is necessary to indicate that its holder has rights over the repositories they want to edit. Since it's hard to find collissions for the hash used by `SSH`, `SHA-256`, it would be difficult for someone to reverse-engineer a private key from a public key to impersonate myself.
## Using `git` commands from `ieng6`
I added [this](https://github.com/Akhil841/cse-15l-lab-reports/blob/master/reports/lr3-commited-from-ieng6.md) file to the repository from `ieng6`.<br>
You can access it as a webpage [here!](lr3-commited-from-ieng6.md)<br>
I first commited the file locally:
![local commit of markdown file](lr3-github-commit-file.png)<br>
I then pushed it to the repository:<br>
![pushing to repo](lr3-github-push-file.png)<br>
If I did not have the public and private `SSH` keys to match the public key I provided to GitHub, the system would instead have asked me for my username and password, followed by an error message saying that GitHub no longer supports authentication via username and password since August 2020 and I thus need to have an SSH key connected to GitHub.
## Commit link
You can find the link to this commit [here](https://github.com/Akhil841/cse-15l-lab-reports/commit/88298462d93364c533b1e27c5fdb49d2922c5a0c).
