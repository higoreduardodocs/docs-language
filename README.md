# Linux

### :radioactive: Instalações

    - WSL:
      ```
      wsl --update
      wsl --set-default-version 2
      wsl --install
      ```

    - Node:
      ```
      curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
      sudo apt install Node.js
      sudo apt purge nodejs
      sudo apt autoremove
      sudo apt install nodejs
      ```

<details>
<summary>:keyboard: Descrição</summary>

**:mailbox_with_no_mail: Comandos**

    - Move/Rename Folder: `sudo mv <name-folder/> <target-folder/>`
    - Copy: `cp <name-folder/file-name> <target-folder/>`
    - File:
      ```
      nano <file-name>
      touch <file-name>
      open <file-name>
      cat <file-name>
      less <file-name>
      rm -rf <folder-name|file-name>
      ls -ltra
      ls -la
      ```
    - Enviroment:
      ```
      printenv
      export ENV_VAR=value
      sudo su
      vi /root/.env
      vi /root/.profile [set -o allexport; source /root/.env; set o+ allexport;]
      ```
    - Path: `echo $PATH`
    - Get Ip: `nslookup <url>`
    - Encriptografia:
      ```
      md5 <file-name>
      shasum <file-name>
      shasum -a 256 <file-name>
      shasum -a 512 <file-name>
      ```
    - OpenSSL:
      ```
      openssl
      openssl genrsa
      openssl genrsa -aes256
      openssl genrsa -aes256 -out private.pem
      openssl rsa -in private.pem -outform PEM -pubout -out public.pem
      openssl genrsa -des3
      openssl genrsa 4096
      ```

<details>
