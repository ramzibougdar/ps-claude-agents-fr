# Agents Claude pour PrestaShop 🇫🇷

Agents [Claude Code](https://docs.anthropic.com/claude-code) spécialisés pour automatiser le développement et la gestion de projets **PrestaShop 8 et 9**, rédigés en français.

## Les agents

| Agent | Rôle |
|---|---|
| [`prestashop-expert`](prestashop-expert.md) | Développeur PrestaShop 8/9 expert : modules, hooks, overrides, thèmes, controllers Symfony, services et injection de dépendances. Analyse le projet (version de PrestaShop, thème actif, modules custom, configuration Symfony) avant de proposer quoi que ce soit, et garantit la compatibilité PS8/PS9. |
| [`code-auditor`](code-auditor.md) | Audit et revue de code d'un module PrestaShop : qualité, failles de sécurité, standards PrestaShop, compatibilité Symfony. Liste tous les problèmes, puis ne corrige que ce que vous validez, un par un ou d'un coup. |
| [`code-auditor-expert`](code-auditor-expert.md) | Même audit, avec en plus une matrice de compatibilité qui déduit les versions de Symfony et de PHP à partir de la version de PrestaShop détectée (de 1.7 à 9.1+). |
| [`seo-expert`](seo-expert.md) | Audit SEO, visibilité dans les IA (GEO/AEO), accessibilité RGAA 4.1.2 et Core Web Vitals : balises meta, URLs, maillage interne, données structurées schema.org, conformité juridique. Génère un rapport HTML (`audit-seo.html`) dans le projet. |

## Installation

Copiez les fichiers `.md` des agents voulus :

- dans le dossier `.claude/agents/` d'un projet PrestaShop, pour ce projet seulement ;
- ou dans `~/.claude/agents/`, pour les utiliser dans tous vos projets.

```bash
git clone https://github.com/ramzibougdar/ps-claude-agents-fr.git
mkdir -p ~/.claude/agents
cp ps-claude-agents-fr/*.md ~/.claude/agents/
rm ~/.claude/agents/README.md
```

## Utilisation

Dans Claude Code, à la racine de votre boutique PrestaShop, demandez simplement la tâche : Claude choisit l'agent adapté, ou vous pouvez le nommer.

```text
> Audite le module mon_module
> Utilise prestashop-expert pour créer un hook sur la validation de commande
> Lance un audit SEO et accessibilité du site
```

Les agents d'audit ne modifient jamais un fichier sans votre accord explicite.

## Auteur

**Ramzi Bougdar** — développeur d'applications IA et expert e-commerce PrestaShop & Shopify.
CV : [ramzibougdar.github.io](https://ramzibougdar.github.io/) · [LinkedIn](https://www.linkedin.com/in/ramzibougdar/)
