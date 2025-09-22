# Projet-AD-OU

Ce projet montre comment j’ai mis en place un domaine Active Directory dans un environnement Windows Server, en utilisant à la fois PowerShell pour l’automatisation et l’interface graphique pour la vérification. L’objectif est de simuler une structure d’entreprise avec des OU, des utilisateurs, des groupes, et une VM cliente connectée au domaine.

1. Création des Unités d’Organisation (OU)
Pour organiser les utilisateurs par service, j’ai créé plusieurs OU dans le domaine ``mydomaine.local`` à l’aide de PowerShell :


<img width="697" height="124" alt="image" src="https://github.com/user-attachments/assets/0c0d5037-d264-4c4a-abe2-d3dd44429d88" />


2. Création des utilisateurs dans l’OU IT
J’ai automatisé la création de plusieurs utilisateurs dans l’OU IT avec PowerShell :


<img width="922" height="357" alt="image" src="https://github.com/user-attachments/assets/fcadd9df-4fd3-48ce-b716-7d75d5e25bb6" />



3. Création d’un groupe de sécurité
J’ai créé un groupe nommé ``G_IT_Admins`` dans l’OU IT via l’interface graphique pour gérer les droits d’accès :


<img width="1273" height="955" alt="image" src="https://github.com/user-attachments/assets/a027b9dc-c9f4-41b9-86b5-969072545e84" />


Ensuite, j’ai ajouté les utilisateurs du service IT à ce groupe via l’onglet "Membre de" :


