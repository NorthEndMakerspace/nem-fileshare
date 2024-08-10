# Set it up

Run this in the project base directory.

```bash
sudo apt install -y git

# Clone/update the repo
if [[ ! -d nem-fileshare ]]; then
  git clone https://github.com/mikeymakesit/nem-fileshare.git
  cd nem-fileshare
else
  cd nem-fileshare
  git pull
fi

python3 -m venv .venv
. .venv/bin/activate
pip install -U pip
pip install -U ansible
ansible-playbook -i ansible/inventory.yaml ansible/configure.yaml
deactivate
```
