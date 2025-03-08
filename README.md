# 4640-w9-lab-start-w25

See lab instructions on D2L


make a new ssh key

```
ssh-keygen -t ed25519 -f ~/.ssh/lab9 -C "key for lab 9"
```
import to aws
```
./import_lab_key  ~/.ssh/lab9.pub
```

```


packer init .

packer fmt ansible-web.pkr.hcl

packer validate ansible-web.pkr.hcl

packer build ansible-web.pkr.hcl
```
