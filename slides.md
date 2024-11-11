---
theme: seriph
title: "Docsible : Automatisation de la Documentation Ansible"
info: Une solution de documentation automatisée pour DevOps
class: text-center
transition: slide-up
exportFilename: docsible-pdf-export
favicon: 
background: /background.jpg
info: false
download: true
drawings:
  persist: true
transition: none
---

# **Docsible**

*Automatisez la documentation de vos rôles Ansible pour des processus DevOps optimisés et sans effort manuel.*

---
transition: slide-up
---

# Contexte et objectif
<v-click>

- <span v-mark.orange="1">Le défi</span> : Gérer un grand nombre de rôles Ansible en évolution constante, augmentant la complexité de la documentation.
</v-click>
<v-click>

- <span v-mark.orange="2">Délais serrés</span> : Maintenir une documentation à jour dans un environnement où les versions et les configurations changent rapidement.
</v-click>
<v-click>

- <span v-mark.orange="3">Documentation manuelle</span> : Un processus fastidieux, sujet aux erreurs et difficilement scalable avec les besoins croissants de conformité et de standardisation.
</v-click>


## Pourquoi Docsible ?
<v-click>

- <span v-mark.orange="4">Évolution rapide</span> des environnements Ansible, rendant la documentation difficile à suivre.
</v-click>
<v-click>

- Besoin d’une documentation <span v-mark.orange="5">à jour en continu</span> pour faciliter la collaboration et l’intégration.
</v-click>
<v-click>

- Automatisation pour <span v-mark.orange="6">gagner du temps</span> en éliminant les tâches répétitives et manuelles.
</v-click>
<v-click>

- <span v-mark.orange="7">**Alignement avec le code**</span> : Une documentation toujours synchronisée avec le code source, réduisant les risques d’incohérence et d'erreurs de configuration.
</v-click>
---
transition: slide-up
level: 2
---

# Docsible : Une solution clé pour le DevOps
<v-click>

- Outil <span v-mark.orange="1">open-source</span> conçu pour automatiser la génération de documentation directement depuis les rôles et collections Ansible.
</v-click>
<v-click>

- <span v-mark.orange="2">Gain de temps</span> : Plus de documentation manuelle, tout est généré automatiquement avec chaque changement de code.
</v-click>
<v-click>

- Documentation <span v-mark.orange="3">intégrée au pipeline CI/CD</span>, toujours à jour, et prête à être consultée par les équipes DevOps et d’intégration.
</v-click>

---
transition: fade-out
---

# Fonctionnement de Docsible
<v-click>

1. <span v-mark.orange="1">Analyse des rôles et tâches Ansible</span> : Extraction des informations clés du code.
</v-click>
<v-click>

2. <span v-mark.orange="2">Extraction des métadonnées</span> : Collecte des descriptions, variables, et autres détails pour une documentation complète.
</v-click>
<v-click>

3. <span v-mark.orange="3">Génération automatique de README</span> : Format structuré et lisible, toujours aligné avec l’état actuel du code.
</v-click>
<v-click>

4. <span v-mark.orange="4">Visualisation</span> : Création de diagrammes pour illustrer les flux de tâches, offrant une vue d’ensemble rapide et compréhensible des workflows.
</v-click>

---
---

```mermaid
flowchart TD
    A[Commandes utilisateur : docsible] --> B{Analyse des répertoires}
    B -->|Dossier des rôles| C{Lecture des fichiers YAML}
    B -->|Dossier des collections| D{Lecture des fichiers Collection}
    
    C --> E[Extraction des tâches : tasks/main.yml]
    C --> F[Extraction des variables : vars/main.yml]
    C --> G[Extraction des handlers : handlers/main.yml]
    C --> H[Extraction des métadonnées : meta/main.yml]
    
    D --> H[Extraction des métadonnées : meta/main.yml]
    D --> I[Extraction des modules : plugins/modules]
    D --> J[Extraction des rôles : roles/]
    D --> K[Extraction des playbooks : playbooks/]
    
    E --> L[Compilation des informations des tâches]
    F --> L
    G --> L
    H --> L
    I --> L
    J --> L
    K --> L
    
    L --> M[Génération du fichier README.md avec toutes les informations]
```

---
transition: slide-left
---

# Demo github

- Rôle : [docsible/thermo-core](https://github.com/docsible/thermo-core)

---
transition: slide-left
---

# Merci de votre attention !

<v-click>Des questions ?</v-click>