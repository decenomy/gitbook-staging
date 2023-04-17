---
description: >-
  Proper File Installation and User ID Creation for Secure Environment
  Deployment.
---

# Environment basis

The installation of files provided by this script has been carried out in a proper manner, with due consideration given to the best security practices.

As a result, the files will not be deployed at the root level, as is common with similar tools. Instead, every instance of coin installation will create its own user ID on the Linux system files, with the coin name serving as the identifier for the deployment location of the coin blockchain respective files.

Please take into consideration the exact file locations, using the coin sapphire as an example.

| Description                       | Directory                | Example ( when need )          |
| --------------------------------- | ------------------------ | ------------------------------ |
| $HOME directory                   | /home/users/             | -                              |
| Directory of user ID              | /home/users/userID/      | /home/users/sapphire/          |
| Wallet files location for user id | /home/users/userID/.coin | /home/users/sapphire/.sapphire |
| Daemon location                   | /usr/local/bin/          | -                              |
| Service files directory           | /etc/systemd/system/     | -                              |

In case of need for terminal access to the mention directories and files please follow the next steps:

| Description           | Command     | Example       |
| --------------------- | ----------- | ------------- |
| To enter in userID    | su - userID | su - sapphire |
| To logout from userID | exit        | exit          |

