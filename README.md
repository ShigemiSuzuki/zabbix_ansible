## zabbix_ansible
ansibleでRaspberryPi 4Bにzabbixを構築する
1. RaspberryPi をインストールする
2. ネットワーク設定をする
3. 初期アカウントの pi のパスワードを設定し、sshを有効にする
4. RaspberryPiの設定で、起動時にCLIにし、更に自動ログオンをオフにする
5. ansibleサーバから証明書認証によってロクイン出来るようにする  
     $ ssh-keygen  
     $ ssh-copy-id pi@xxx.xxx.xxx.xxx (RaspberryPiのIP)  
6. ansibleサーバで  
     $ ansible-playbook -i inventory/inventory.ini site.yml  
7. 基本構築完了
