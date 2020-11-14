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

Faire apparaître les fonctions lambda dans Cloud9
- xxx
