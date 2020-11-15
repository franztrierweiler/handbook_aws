# handbook_aws
Trucs et astuces pour AWS
Gérer ses utilisateurs:
- Créer des groupes.
- Administators: Stratégie = AdministratorAccess (évite de tout créer avec le compte racine AWS).
- Developers: Stratégie = AWSCloud9Users

Création d'une instance Cloud9
- Ne pas la créer depuis le compte racine.
- Créer l'instance Cloud9 sur une machine ec2.
- Créer d'abord l'instance eC2 (une nano 0,5 GB RAM peut suffire), avec connexion SSH (indépendant de Cloud9).
- Créer l'instance Cloud9 en choisissant connexion via SSH.
- Ajouter la clé publique créée par Cloud9 à la machine ec2 dans le fichier authorized_keys de l'utilisateur ubuntu.
- Installer les éléments demandés par Cloud9: nodejs, Python 2.7
- Autoriser l'installation de Cloud9
- L'utilisateur par défaut sur ec2 est Ubuntu -- franzdev y est rattaché
- Les autres utilisateurs ont leur propre user Linux sur la machine, créer le .ssh correspondant dans le profil pour pouvoir créer l'environnement Cloud9 correspondant. Comme chaque user Cloud9 accède à la machine en ssh, il n'est pas nécessaire de préciser le mot de passe ==> Attention, après création l'environnement Cloud9 a disparu, il semble nécessaire d'avoir une VM ec2 par utilisateur.
- Attention: lorsque l'instance ec2 est utilisée en tant qu'entité Cloud9 "non directe" (3ème chois), l'instance ec2 ne s'arrête pas toute seule au bout de X minutes d'inactivité), il faut l'arrêter et la redémarrer le cas échéant ===> pour un usage par des intervenants extérieurs il vaut mieux utiliser le mode direct.

Faire apparaître les fonctions lambda dans Cloud9
- TBD
