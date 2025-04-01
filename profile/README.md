# DEPSEC Project – Public Access

> **Dependency Security & Evaluation Control**  
> Plateforme de gestion des vulnérabilités à partir des SBOMs pour projets de développement.

---

## Objectif

DEPSEC fournit un ensemble d'API REST modulaires pour :
- Importer des SBOMs
- Évaluer automatiquement les vulnérabilités
- Générer des rapports
- Gérer les projets liés à la sécurité logicielle

---

## Achitecture en microservices

Le projet est divisé en plusieurs services indépendants :

| Nom | Description | Lien |
|-----|-------------|------|
| `AuthAPI` | Authentification par JWT | [🔗 Voir le dépôt](https://github.com/DEPSEC-Project/AuthAPI) |
| `SBOMs` | Analyse des SBOMs et détection des vulnérabilités | [🔗 Voir le dépôt](https://github.com/DEPSEC-Project/SBOMs) |
| `Gestion_Rapport` | Transformation de rapports JSON (Trivy) en Markdown | [🔗 Voir le dépôt](https://github.com/DEPSEC-Project/Gestion_Rapport) |
| `API_Project_Management` | Gestion centralisée de projets et suivi des risques | [🔗 Voir le dépôt](https://github.com/DEPSEC-Project/API_Project_Management) |
| `DB-Management` | Modélisation & gestion centralisée des bases | [🔗 Voir le dépôt](https://github.com/DEPSEC-Project/DB-Management) |

---

## Déploiement

Le projet est pensé pour fonctionner dans 3 environnements :
- **Développement** (`5433`, `5001`)
- **Testing** (`5434`, `5002`)
- **Production** (`5435`, `5000`)

Via des stacks Docker Compose indépendantes et orchestrées via Portainer ou CI GitHub.

---

## 📦 Registre d’images

Toutes les images Docker sont publiées sur GitHub Container Registry :

➡️ [ghcr.io/depsec-project](https://ghcr.io/depsec-project)

---

_© 2025 - DEPSEC Project_  
