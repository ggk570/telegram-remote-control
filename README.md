# telegram-remote-control
A python program to control a linux or windows machine remotely using telegram bot

**Features:**
- Upload files to remote host
- Download files from remote host
- Execute shell commands

### Usage:
1. Create a telegram bot with the help of [BotFather](https://telegram.me/BotFather)
2. Paste your bot api token on **line 169** of [telegram-control.py](https://github.com/ggk570/telegram-remote-control/blob/main/telegram-control.py)
   
![auth_token](https://github.com/ggk570/telegram-remote-control/blob/main/Screenshots/api_token.png?raw=true)

4. Change the password on **line 20**, you can use this password to authenticate to bot
   
![password](https://github.com/ggk570/telegram-remote-control/blob/main/Screenshots/password.png?raw=true)

6. Now you can add a cronjob/startup script to execute the script automatically
7. To manually run the program use command:
```bash
python3 telegram-control.py
```
5. Now you can search your bot on telegram app then to authenticate to the bot use below command on telegram
```
/login <your_password>
```
6. To run a shell command on remote host, use command
```
/run <command>

Example:
/run whoami
/run ls -la "/home/user/personal files"
```
7. To download a file from remote host, use command:
```
/download <absolute_file_path>

Example:
/download /home/username/test_file.txt
```
8. To upload a file on the target, you first need to set a directory where the uploaded files can be saved then you can use the telegram app to upload the file, the script will save the file in specified directory, once the file is saved you will get success message on telegram (upload process takes time, so be patient).
```
/upload <absolute_path>

Example:
/upload /tmp
```

