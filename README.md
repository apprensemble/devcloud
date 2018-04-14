# devcloud

Construire un cloud de dev basé sur openstack + dcos

## Pourquoi?

Pour le fun! Openstack c'est la virtualisation à portée de main :
* stockage
* réseau
* machine(CPU)

Le tout gérable grace à un ensemble d'outils cohérent ainsi qu'une interface sympa : horizon. C'est opensource, utilisé en production et activement développé.

DC/OS est quand à lui un Système d'exploitation de datacenter. Semble idéale pour simplifier la gestion de nos applications dans le datacenter virtuel.

A-ton besoin de cela pour développer à la maison? Sincerement non. Mais en entreprise je pense que ce serait top. Alors l'utilisation à la maison est pour moi un POC. J'ai envie de voir ce que c'est d'utiliser ces outils au quotidien.

## OK... Mais que va t-on en faire?

En ce moment je m'interesse à l'iot et le packaging d'OS. Coté IOT j'ai besoin de collecter, analyser et stocker des données. Coté packaging d'OS...Je vais y reflechir...Pourquoi pas un environnement de dev ou de tests à la demande... On verra.

## ressources

### vagrant - devstack

https://github.com/openstack-dev/devstack

### vagrant - dcos

https://github.com/dcos/dcos-vagrant

### une vm dans un container :)

Je me suis dis que mettre une vm dans un container pouvait être sympa car une vm dans une vm je doute un peu des perf... Et bien d'autres l'ont fait même pas besoin de se prendre la tête :

https://stackoverflow.com/questions/48422001/how-to-launch-qemu-kvm-from-inside-a-docker-container --> https://github.com/naeemkhan12/dockerfiles/blob/master/kvm/Dockerfile

La même chose est possible avec virtualbox :

https://stackoverflow.com/questions/25741904/is-it-possible-to-run-virtualbox-inside-a-docker-container

## troubleshooting

### J'ai installé DCOS via vagrant et j'ai eu qq pb.

* stack too deep après un vagrant up : https://github.com/hashicorp/vagrant/issues/9595

* impossible d'acceder aux noeuds avec un dcos ssh car je ne connais pas le mdp core : https://github.com/dcos/dcos-cli/issues/679

### J'ai installé devstack via vagrant et j'ai eu qq pb.

* impossible de trouver le package puppet apres le premier vagrant up : j'ai ajouté ```sudo apt-get update``` au moment du provisionning.



