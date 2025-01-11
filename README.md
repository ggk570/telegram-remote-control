# telegram-remote-control
A python program to control a linux or windows machine remotely using telegram bot

**Features:**
- Upload files to remote host
- Download files from remote host
- Execute shell commands

**Requirements:**
```
pip3 install python-telegram-bot
```

### Usage:
Create a telegram bot with the help of [BotFather](https://telegram.me/BotFather)

Paste your bot api token on **line 169** of [telegram-control.py](https://github.com/ggk570/telegram-remote-control/blob/main/telegram-control.py)
   
![auth_token](https://github.com/ggk570/telegram-remote-control/blob/main/Screenshots/api_token.png?raw=true)

Change the password on **line 20**, you can use this password to authenticate to bot
   
![password](https://github.com/ggk570/telegram-remote-control/blob/main/Screenshots/password.png?raw=true)

Now you can add a cronjob/startup script to execute the script automatically

To manually run the program use command:
   
```
python3 telegram-control.py
```

Now you can search your bot on telegram app then to authenticate to the bot use below command on telegram
   
```
/login <your_password>
```

To run a shell command on remote host, use command
   
```
/run <command>

Example:
/run whoami
/run ls -la "/home/user/personal files"
```

To download a file from remote host, use command:
   
```
/download <absolute_file_path>

Example:
/download /home/username/test_file.txt
```

To upload a file on the target, you first need to set a directory where the uploaded files can be saved then you can use the telegram app to upload the file, the script will save the file in specified directory, once the file is saved you will get success message on telegram (upload process takes time, so be patient).
    
```
/upload <absolute_path>

Example:
/upload /tmp
```

### Demonstration
**Target Machine**

![target_machine_command](https://github.com/ggk570/telegram-remote-control/blob/main/Screenshots/target_machine.jpeg?raw=true)


**Attack Machine**

[![demo](https://github.com/ggk570/telegram-remote-control/blob/main/Screenshots/video_demonstration_thumbnail.png?raw=true)](
https://github.com/ggk570/telegram-remote-control/raw/refs/heads/main/Screenshots/attack_machine.mp4)

