# Projet-AD-OU

Ce projet montre comment j’ai mis en place un domaine Active Directory dans un environnement Windows Server, en utilisant à la fois PowerShell pour l’automatisation et l’interface graphique pour la vérification. L’objectif est de simuler une structure d’entreprise avec des OU, des utilisateurs, des groupes, et une VM cliente connectée au domaine.

1. Création des Unités d’Organisation (OU)
Pour organiser les utilisateurs par service, j’ai créé plusieurs OU dans le domaine ``mydomaine.local`` à l’aide de PowerShell :


<img width="697" height="124" alt="image" src="https://github.com/user-attachments/assets/0c0d5037-d264-4c4a-abe2-d3dd44429d88" />
<img width="1273" height="955" alt="image" src="https://github.com/user-attachments/assets/fce2992a-7d76-4cf2-972c-eefc84701b8e" />



2. Création des utilisateurs dans l’OU IT
J’ai automatisé la création de plusieurs utilisateurs dans l’OU IT avec PowerShell :


<img width="922" height="357" alt="image" src="https://github.com/user-attachments/assets/7d81d981-d874-455f-8120-da56ccb89a3a" />
<img width="1273" height="952" alt="image" src="https://github.com/user-attachments/assets/3376d436-0fb1-499a-92bb-dbbb27488ca0" />


3. Création d’un groupe de sécurité
J’ai créé un groupe nommé ``G_IT_Admins`` dans l’OU IT via l’interface graphique pour gérer les droits d’accès :


<img width="538" height="466" alt="image" src="https://github.com/user-attachments/assets/b0bee2b1-be7b-4cd7-a609-6d28dbf96cbf" />


Ensuite, j’ai ajouté les utilisateurs du service IT à ce groupe via l’onglet "Membre de" :


<img width="1273" height="955" alt="image" src="https://github.com/user-attachments/assets/0d277ee1-cd57-43c1-8ac5-4e2d9ff1fd0f" />
<img width="1269" height="955" alt="image" src="https://github.com/user-attachments/assets/9d1ca329-2280-4d7b-b04a-38a4808d1be7" />


4. Connexion d’une VM cliente au domaine
J’ai configuré une machine virtuelle Windows 10 comme poste client, puis je l’ai jointe au domaine ``mydomaine.local`` . Ensuite, j’ai testé la connexion avec un utilisateur du service IT (``jmartin``).


<img width="1918" height="961" alt="image" src="https://github.com/user-attachments/assets/5e6a9a15-344e-46dc-afac-4cdc3a4f5bc7" />
<img width="1917" height="955" alt="image" src="https://github.com/user-attachments/assets/926361d6-e739-40ce-84fe-77828803a191" />


Résultat
• 	Domaine AD fonctionnel avec structure logique.
• 	Utilisateurs créés et organisés par service.
• 	Groupe de sécurité opérationnel.
• 	Poste client connecté et authentifié avec succès


