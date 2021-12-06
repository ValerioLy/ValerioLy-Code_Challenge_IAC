
#il playbook è stato creato usando ubuntu wsl su windows 10 come master e virtualbox come node1 e node2

#ABILITARE le variabili d'ambiente da wsl su windows per utilizzare vagrant con virtualbox
export PATH="${PATH}:/mnt/c/Program Files/Oracle/VirtualBox"
export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"

il file "Vagrantfile" consente di creare 2 vm centos in locale tramite vagrant usando come virtualizzatore virtualbox

usare "vagrant up" da wsl ubuntu per creare le 2 vm centos

ansible-playbook docker.yml per avviare il playbook