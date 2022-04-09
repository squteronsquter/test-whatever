# Sample rsync commands 


## rsync remote with local


## all websites:

```
rsync -azP -e "ssh -i /path/to/.ssh/authorized_keys_name" username@192.168.56.100:/usr/share/nginx/ ~/Desktop/local/folder

```
## just one website

```
rsync -azP -e "ssh -i /path/to/.ssh/authorized_keys_name" username@192.168.56.100:/usr/share/nginx/your_website_folder_name/public_folder_name ~/Desktop/local/folder_name

```
## rsync local with remote


```
rsync -azP -e "ssh -i /path/to/.ssh/authorized_keys_name" /Users/gray/local_development_folder/where_your_code_is/* username@192.168.56.100:/usr/share/nginx/your_website_folder_name/public_folder_name/ 

```

## general command local to remote

```
rsync ~/source/directory/* username@192.168.56.100:~/destination

```

## rsync folder on a remote machine eg. to keep a backup folder

```
rsync /source/directory/* /destination/folder_name


rsync -vazP /usr/share/nginx/* /home/backups/all_websites

```


## You can also put some of these commands into a cron job to run regularily



___happy rsyncing___
