# Context

Avec le pic épidémique, les hôpitaux risquent de manquer de respirateurs (machines de Ventilation Assistée Controlée). Nous souhaitons proposer une solution open-source pour fabriquer des machines de VAC d’urgence.

L’idée est de partir des respirateurs manuels et de produire une solution pour les mécaniser avec un bras mécanique et de l’électronique. Nous sommes collectif citoyen rassemblant des acteurs de différents milieux économiques et académiques Auvergne Rhône Alpes. Le service de réanimation du CHU Grenoble nous aide à valider le prototype.

Les premiers prototypes devraient être prêts vers le debut de la semaine prochaine, pour des tests sur poumon artificiel débutant immédiatement après. L’utilisation en hôpital pourrait commencer vers la fin de la semaine du 30 mars.
Ce projet est une course contre la montre, et nous avons besoin d’aide.

# Misson

Develop an open source VAC with all contributions being under BSD/MIT/CC license allowing other to copy, replicate, derive similar VACs.
We try selecting components that are either readily available in hospitals or in FabLabs, to make it as easy as possible to replicate the design.
The desing is driven by requirements provided by emergency professionals, and aim to make the usg of the device easy and familiar for them.
We hope that if our desing is successful it will be replicated by others.

# Equipes

## Experts

* Urgentiste CHU (je ne met pas son nom pour limiter des solicitations)
* Cyril Fromentin - a travaillé sur un VAC dans le passé

## Coordination

* Adrien Farrugia - instigateur du projet, electron libre, pousse un peu tout le monde
* Stan Borkowski - coordination technique, design meca
* Jerome Maisonnasse - relation avec les institutions, dev IHM

## Mecanical desing and motor

### proto Inria
* knimp (Sylavain) - modelisation parametrique
* Rix (Eric) - modelisation, motage, tests mecaniques, test du moteur NEMA 23
* Stan

### proto Alprobotic
Benoit - motorisation, premiers test du ballon, proto chez Alprobotic

### Equipe MinMax Medical
Christophe D et son equipe vont regarder à partir du 27.03 s'ils proposent une meca+motorisation alternative.

## Pressure sensors

* Samuel Heidmann - sourcing et interface pour le capteur differenciel et absolu
* Ludovic LM - vanne reblables low-cost

## Vannes PEP

### Equipe MinMax Medical
Christophe D et son equipe cherchent une solution 

### Equipe Low-cost / DIY
Ludovic LM - vanne PEP sans commande low-cost, source de pression pour la commande de la PEP commandable avec une pompe d'air pour aquarium

## FiO2
MinMax Medical vont essayer de sourcer le capteur.

## Firmware Arduino
[https://github.com/Recovid/Controller](https://github.com/Recovid/Controller)
manO (Manoel) et son equipe commencent implementer des focntions de base du VAC

## IHM
[https://github.com/Recovid/ihm](https://github.com/Recovid/ihm)
Germain et Jerome developent l'interface d'utilisateur en Python sur RPi.


# Schema general

Three variants are considered, but currently we focus on the one closest to the requirement of medical staff.

## Recovid-MD - close to a medical device grade ventilator
This is our current target.

![recovid-MD](/images/principe.001.png)

## Recovid-simple

![recovid-simple](/images/principe.002.png)

## Recovid-DIY

It is not clear if this type of device is of any use in a Hospital.
No sensors, so no clinically usable data.
![recovid-giy](/images/ventilation_low_tech_v3.svg)


## Scrap-made presure valves (APL, PEEP)

material: aquarium tube 4mm internal / 6mm external
Section not enough enough I would have to double the diameter
2 or 4 non-return valve:
https://www.botanic.com/produit/366004/clapet-anti-retour-pour-pompe-a-air.html
pipe 4/6mm :
https://www.botanic.com/produit/365979/tuyau-pour-pompe-a-air-4-6mm-silicone-2-5m.html
possibility of using diffusers in a volume of water to filter the exhaled air:
https://www.botanic.com/produit/365998/diffuseur-aquarium-ceramique-50mm.html
ISSUE:
* the rectangular volumes prevent the water used for pressure control from leaving the system I still don't know how to make them.
* the system is not adjustable in pressure ... except to put several PEP control system in parallel with small valves: not terrible


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

