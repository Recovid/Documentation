# Contexte

Avec le pic épidémique, les hôpitaux risquent de manquer de respirateurs (machines de Ventilation Assistée Controlée). Nous souhaitons proposer une solution open-source pour fabriquer des machines de VAC d’urgence.

L’idée est de partir des respirateurs manuels et de produire une solution pour les mécaniser avec un bras mécanique et de l’électronique. Nous sommes collectif citoyen rassemblant des acteurs de différents milieux économiques et académiques Auvergne Rhône Alpes. Le service de réanimation du CHU Grenoble nous aide à valider le prototype.

Les premiers prototypes devraient être prêts vers le début de la semaine prochaine, pour des tests sur poumon artificiel débutant immédiatement après. L’utilisation en hôpital pourrait commencer vers la fin de la semaine du 30 mars.
Ce projet est une course contre la montre, et nous avons besoin d’aide.

# Mission

Develop an open source VAC with all contributions being under BSD/MIT/CC license allowing other to copy, replicate, derive similar VACs. We try selecting components that are either readily available in hospitals or in FabLabs, to make it as easy as possible to replicate the design. The design is driven by requirements provided by emergency professionals, and aim to make the usage of the device easy and familiar for them.

We hope that if our design is successful, it will be replicated by others.

# Equipes

Ci dessous les pseudos Discords des contributeurs au projet.

## Experts

* Urgentiste CHU (je ne met pas son nom pour limiter des solicitations)
* ``cyril FROMENTIN`` - a travaillé sur un VAC dans le passé
* ``ErikHuneker`` - réglementation dispositifs médicaux

## Coordination

* ``a.farrugia`` (Adrien) - instigateur du projet, pousse un peu tout le monde
* ``stan.borkowski`` - coordination technique, design meca
* ``jerome`` - relation avec les institutions, dev IHM
* ``rstephane`` - communication sur le web et community designer.

## Mecanical design and motors

### Prototype Inria
* ``sylefeb`` (Sylavain) - modélisation paramétrique
* ``Rix`` (Eric) - modélisation, motage, tests mécaniques, test du moteur NEMA 23
* ``stan.borkowski``

### proto Alprobotic
``Benoît Alprobotic`` - motorisation, premiers test du ballon, proto chez Alprobotic

### Equipe MinMax Medical
``Christophe D`` et son équipe vont regarder à partir du 27.03 s'ils proposent une meca+motorisation alternative.

## Pressure sensors

* ``samuel.heidmann`` - sourcing et interface pour le capteur différenciel et absolu
* ``ludovic lm`` - vanne réglables low-tech

## Vannes PEP

### Equipe MinMax Medical
``Christophe D`` et son équipe cherchent une solution 

### Equipe Low-tech / DIY
``ludovic lm`` - vanne PEP sans commande low-cost, source de pression pour la commande de la PEP commandable avec une pompe d'air pour aquarium

## FiO2
MinMax Medical vont essayer de sourcer le capteur.

## Firmware Arduino
[https://github.com/Recovid/Controller](https://github.com/Recovid/Controller)

``manO`` (Manoel) et son équipe commencent implémenter des fonctions de base du VAC

## IHM
[https://github.com/Recovid/ihm](https://github.com/Recovid/ihm)

``Germain`` et ``jerome`` dévellopent l'interface d'utilisateur en Python sur RPi.

# Related projects

* [Well documented, nicely designed mecanisation](https://e-vent.mit.edu)
* [Minimalist VAC, MUR project](https://www.mur-project.org)
* [A paper from MIT](https://web.mit.edu/2.75/projects/DMD_2010_Al_Husseini.pdf), it is the starting point for our implementation.
* An alternative, more complex, [bag squeezing design](https://techcrunch.com/2020/03/19/open-source-project-spins-up-3d-printed-ventilator-validation-prototype-in-just-one-week/)
* [3D printable respirator developped in Nantes, France](https://github.com/covid-response-projects)
* [Low-cost, open source ventilator with Arduino](https://blog.arduino.cc/2020/03/17/designing-a-low-cost-open-source-ventilator-with-arduino/)
* [7 open hardware projects working to solve COVID-19](https://opensource.com/article/20/3/open-hardware-covid19)


# Potentially usefull documentation

* [User manuals of various ventilators](https://fr.ifixit.com/Device/Ventilator?fbclid=IwAR2QkkLaEYnkGO83MzNBpAX4AoMacKGG9ShRHLeXB89XToLnUCslMgtQvB8)

