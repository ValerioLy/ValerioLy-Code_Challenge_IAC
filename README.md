
il playbook è stato creato usando ubuntu wsl su windows 10 come master node e virtualbox come node1 e node2
il codice creato è interamente creato senza utilizzo di fonti esterne, non è stato riutilizzato codice online,
è il mio primo playbook che ho mai creato su ansible, prima di questo non conoscevo nulla di ansible


ABILITARE le variabili d'ambiente da wsl su windows per utilizzare vagrant con virtualbox
export PATH="${PATH}:/mnt/c/Program Files/Oracle/VirtualBox"
export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"

il file "Vagrantfile" consente di creare 2 vm centos in locale tramite vagrant usando come virtualizzatore virtualbox

usare "vagrant up" da wsl ubuntu per creare le 2 vm centos

ansible-playbook docker.yml per avviare il playbook (utilizzare sudo per scalare i privilegi da wsl)

Task Mancanti:
- manca da passare le variabili tra i play (token,ip interfaccia, curl servers)
- manca da predisporre il playbook con i roles
- usare task con molecule
- manca la parte di continous integration (iniziata associato github con Travis)