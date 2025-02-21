# stamp-iot-kubespray

## 実行環境構築
```sh
$ git clone git@github.com:mktkhr/stamp-iot-kubespray.git
$ cd stamp-iot-kubespray

# 初回のみ
$ cp .env.sample .env

# venv activate
$ python3 -m venv venv
$ source venv/bin/activate

$ pip install -r requirements.txt

$ ansible-galaxy install -r requirements.yml

$ ANSIBLE_REMOTE_USER=<ユーザー名> ANSIBLE_PRIVATE_KEY_FILE=<SSHキーのパス> ansible-playbook -i inventory/hosts.yml playbook/k8s.yml
```