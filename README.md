# home
cozy place to hang out

# Edwin's Linux+Git Notes

Just a collection of useful things I'm writing down as I learn to use linux and git.

## How to install ssh credentials on WSL

* copy over ppk file to /home/.ssh/
* sudo apt-get install putty-tools 
* puttygen server1.ppk -O private-openssh -o server1.pem 
* chmod 400 server1.pem 
* eval `ssh-agent -s`
* ssh-add server1.pem

## Checking out the repo for the first time
* git lfs install
* pip install pre-commit
* git clone git@github.com:RespiraWorks/Ventilator.git

## Pre-Commit and Commit
* pre-commit run --from-ref $(git merge-base origin/master HEAD) --to-ref HEAD
* git commit -m "commit message"

## Rebase
* git rebase master
* git push -f
