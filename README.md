# Projet-AD-OU

Ce projet montre comment j’ai mis en place un domaine Active Directory dans un environnement Windows Server, en utilisant à la fois PowerShell pour l’automatisation et l’interface graphique pour la vérification. L’objectif est de simuler une structure d’entreprise avec des OU, des utilisateurs, des groupes, et une VM cliente connectée au domaine.

1. Création des Unités d’Organisation (OU)
Pour organiser les utilisateurs par service, j’ai créé plusieurs OU dans le domaine ``mydomaine.local`` à l’aide de PowerShell :

``$List_OU = @("IT", "Finance", "HR", "Marketing", "Support")
foreach ($ou in $List_OU) {
    New-ADOrganizationalUnit -Name $ou -Path "DC=mydomaine,DC=local"
}``
