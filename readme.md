# ForgeFolio - Documentation - Hébergement de portfolio BTS SIO

Documentation technique du projet **ForgeFolio**, une infrastructure web destinée à héberger les portfolios des étudiants en BTS SIO (Initialement conçus pour le BTS SIO du lycée Paul-Louis-Courier).

---

Le projet apporte un cadre reproductible pour publier des portfolios étudiants, alors que les notions d'infrastructure et d'exploitation sont peu présentes dans le parcours de développement (BTS SIO SLAM). La documentation décrit les choix d'architecture, la configuration du VPS et d'Apache, les mesures de sécurité, ainsi que les procédures de déploiement et de maintenance.

Le site est généré avec [MkDocs](https://www.mkdocs.org/) et le thème
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). Les
modifications poussées sur `main` sont publiées automatiquement par GitHub Actions.

**Documentation en ligne :** [forgefolio-docs.loutik.fr](https://forgefolio-docs.loutik.fr)

> Une migration vers [Zensical](https://zensical.org/docs/get-started/) est prévue.

---

## Structure du projet

```text
.
├── .github/
│   └── workflows/
├── docs/
│   ├── assets/
│   ├── index.md
│   └── cahier-des-charges.md
├── templates/
└── mkdocs.yaml
````

  - **`.github/workflows/`** : Contient le pipeline CI/CD (`publish.yaml`) chargeant la génération et le déploiement automatique du site lors d'un *push* sur la branche `main`.
  - **`docs/`** : Répertoire source contenant les pages de la documentation au format Markdown (`.md`) ainsi que les médias dans le sous-dossier `assets/`.
  - **`mkdocs.yaml`** : Fichier de configuration principal définissant la navigation, le thème visuel et les extensions du site.
  - **`templates/`** : Répertoire contenant les modèles de documents réutilisables pour structurer la documentation du projet.

---

## Comment utiliser le projet en local

1.  **Cloner le dépôt et y accéder**

```bash
git clone git@github.com:FireToak/forgefolio-docs.git
cd forgefolio-docs
```

  * **`git clone <url>`** : Télécharge une copie complète du dépôt distant sur ton poste de travail local.
  * **`cd <dossier>`** : (*Change Directory*) Modifie ton répertoire de travail actuel pour entrer dans le dossier du projet.

2.  **Installer les dépendances**

```bash
pip install mkdocs-material
```

  * **`pip install ...`** : Utilise le gestionnaire de paquets de Python pour télécharger et installer la bibliothèque `mkdocs-material`, requise pour compiler le site avec l'interface visuelle choisie.

3.  **Lancer le serveur de développement**

```bash
mkdocs serve
```

  * **`mkdocs serve`** : Démarre un mini-serveur web local (généralement accessible sur `http://127.0.0.1:8000`). Cette commande surveille tes fichiers et recharge automatiquement la page web dans ton navigateur dès que tu sauvegardes une modification dans un fichier Markdown. Idéal pour tester le rendu avant publication.

---

## Mainteneurs

**Louis MEDO** | [Linkedin](https://www.linkedin.com/in/louismedo/) | [Portfolio](https://louis.loutik.fr/) | [GitHub](https://github.com/FireToak)

---

<div align="center"\>
<br>
<small\><i\>Dernière mise à jour : 28 août 2026</i\></small\>
</div\>