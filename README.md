# Projet-AD-OU

Ce projet montre comment j’ai commencé à structurer un domaine Active Directory existant dans un environnement Windows Server. L’objectif est de rester sur des choses simples : créer des Unités d’Organisation (OU), des utilisateurs, des groupes de sécurité, et tester la connexion d’un poste client au domaine. J’ai utilisé PowerShell pour aller plus vite, et l’interface graphique pour vérifier et illustrer chaque étape.

**1. Création des Unités d’Organisation (OU)**
Pour organiser les utilisateurs par service, j’ai créé plusieurs OU dans le domaine ``mydomaine.local`` à l’aide de PowerShell :


<img width="805" height="67" alt="image" src="https://github.com/user-attachments/assets/5c07658a-a5f5-49d0-8cd5-5d6e4247b013" />
<img width="1273" height="955" alt="image" src="https://github.com/user-attachments/assets/5f67447d-6853-4504-b3a2-c7ec93638407" />


**2. Création des utilisateurs dans l’OU IT**
J’ai automatisé la création de plusieurs utilisateurs dans l’OU IT avec PowerShell :


<img width="922" height="357" alt="image" src="https://github.com/user-attachments/assets/5e30fb91-1375-47d3-a319-b993cb7b7d5b" />
<img width="1273" height="952" alt="image" src="https://github.com/user-attachments/assets/9fe48b42-2fd0-4d2d-ac52-03013d64b7c6" />


**3. Création d’un groupe de sécurité**
J’ai créé un groupe nommé ``G_IT_Admins`` dans l’OU IT via l’interface graphique pour gérer les droits d’accès :


<img width="538" height="466" alt="image" src="https://github.com/user-attachments/assets/ee7183ca-ccad-4035-a64b-1dcac12f3ab7" />


Ensuite, j’ai ajouté les utilisateurs du service IT à ce groupe via l’onglet "Membre de" :


<img width="1269" height="955" alt="image" src="https://github.com/user-attachments/assets/b54edb41-a963-48b0-a42e-8ff38113d2e7" />


**4. Connexion d’une VM cliente au domaine**
J’ai configuré une machine virtuelle Windows 10 comme poste client, puis je l’ai jointe au domaine ``mydomaine.local`` . Ensuite, j’ai testé la connexion avec un utilisateur du service IT (``jmartin``).


<img width="1918" height="961" alt="image" src="https://github.com/user-attachments/assets/5e6a9a15-344e-46dc-afac-4cdc3a4f5bc7" />
<img width="1917" height="955" alt="image" src="https://github.com/user-attachments/assets/926361d6-e739-40ce-84fe-77828803a191" />


**Résultat**
• 	Domaine AD fonctionnel avec structure logique.
• 	Utilisateurs créés et organisés par service.
• 	Groupe de sécurité opérationnel.
• 	Poste client connecté et authentifié avec succès


