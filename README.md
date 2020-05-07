# ssh-laravel-gcloud

1.Create Compute Engine Instance
2.Generate ssh-keygen -t rsa  -C "username on SSH terminal"
  -prompt for the file name " Will be save at home folder"
  -local ssh file on terminal "cat file.pub"
  -copy then proceed to 3.
3.after being generated add on Compute Engine SSH click enable

on visual studio code ssh config 

Host Connection Name
    HostName Ip.Address.com
    User userNameCanbeFoundSShTermanilCloud
    IdentityFile ~/.ssh/file(private not public)
    
Now Connect
    
