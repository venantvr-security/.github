# venantvr.security

Boîte à outils offensive et défensive de cybersécurité : scanners de vulnérabilités, reconnaissance réseau, analyse statique de code, recherche en sécurité et outils IoT.

## Repos

### Analyse statique de code

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.PHP.Sec.Scan` | Python | Scanner de sécurité PHP par analyse statique : taint tracking forward, AST tree-sitter, 16 types de vulnérabilités (SQLi, XSS, RCE, SSRF...), rapports SARIF/HTML/terminal, 89 tests |
| `TypeScript.PHP.Sec.Scan` | TypeScript | Extension VS Code de détection de vulnérabilités PHP : taint tracking intégré à l'éditeur, diagnostics en temps réel, commande de scan workspace |
| `Python.Sqli.Detection` | Python | Scanner d'injections SQL (basé sur DSSS) : tests booléens blind, tampering de paramètres, détection par diff de réponses HTTP (texte, code, titre, HTML) |
| `Python.QueryStringsFromPhp` | Python | Extracteur de query strings depuis du code source PHP pour alimenter d'autres outils de scan |

### Analyse de trafic et fichiers

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Har.Scanner` | Python | Analyseur de fichiers HAR (HTTP Archive) pour détecter des patterns de sécurité dans le trafic réseau capturé |
| `Python.HAR.ZAP` | Python | Scanner HAR avec intégration OWASP ZAP : corrélation entre captures HAR et résultats de scan dynamique |
| `Python.AccessForbiddenFiles` | Python | Scanner de fichiers à accès restreint : détection de ressources sensibles exposées (`.env`, `.git`, backups...) |
| `Python.Traversal.Vulnerabilities` | Python | Scanner de vulnérabilités path traversal : tests automatisés de séquences `../` sur des endpoints cibles |

### Reconnaissance et réseau

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Nmap.Batch` | Python / Flask | Automatisation de scans réseau en batch avec dashboard web temps réel : Nmap, Masscan, Netcat, Hping3, Curl. Multi-threadé, configuration TOML, SSE pour le streaming |
| `Python.Dome.SubDomains` | Python | Énumération de sous-domaines par bruteforce DNS, résolution récursive et requêtes API tierces |
| `Python.Osint.Blackbird` | Python | Outil OSINT de recherche de noms d'utilisateur sur 500+ plateformes (basé sur Blackbird), requêtes asynchrones aiohttp |
| `Python.Arping` | Python / Scapy | Scanner réseau ARP : découverte de machines sur un sous-réseau via paquets ARP broadcast (Scapy) |
| `Python.Apache.Logs` | Python | Analyseur de logs Apache orienté sécurité : clustering K-Means et DBSCAN pour détecter les patterns d'attaque |
| `Python.Network.Connections` | Python | Monitoring en temps réel des connexions réseau actives sur une machine |

### Recherche et démonstrations de sécurité

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Ransomware` | Python | Recherche et analyse de mécanismes de ransomware (contexte éducatif) |
| `Python.Session.Hijacking` | Python | Démonstration de détournement de session HTTP : interception, rejeu de cookies, contre-mesures |
| `Python.CSRF.Demo` | HTML/Python | Démonstration de vulnérabilités CSRF : formulaires malveillants, tokens anti-CSRF, validation Referer |
| `Python.CORS.Handler` | Python / Flask | Lab de test de configurations CORS : serveur configurable, vérification de politiques cross-origin |
| `Python.Network.Pivot` | Python / Docker | Lab de pivot réseau conteneurisé : 3 machines (attacker + 2 victims), backdoor, Twisted web server |
| `Python.Usb.Test` | Python | Outils de test de sécurité USB : détection de périphériques, analyse de comportement |

### Anonymisation et TOR

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Tor.Proxy` | Python / GTK | Proxy TOR avec interface système (system tray GTK) : rotation automatique d'IP via stem, changement de circuit, vérification d'anonymat |
| `Javascript.TOR.Workflow` | JavaScript | Visualisations interactives des workflows TOR : routing en oignon, négociation de clés, comparaison HTTPS, transactions blockchain |

### Hardware et IoT

| Repo | Stack | Description |
|------|-------|-------------|
| `Raspberry.Hack` | C | Outils de test de sécurité embarquée sur Raspberry Pi : persistence via rc.local, scripts de reconnaissance |
| `Raspberry.IpBlocker` | Python | Blocage automatique d'IP malveillantes sur Raspberry Pi |
| `Python.PiZero.WiFi` | Python / Scapy | Boîte à outils WiFi pour Raspberry Pi Zero : sniffing de paquets (pyshark + Scapy), déauthentification, géolocalisation, dashboard Flask, alertes Telegram |

### Divers

| Repo | Stack | Description |
|------|-------|-------------|
| `Php.WordPress.Cypher` | PHP | Utilitaires de chiffrement et hachage pour WordPress |

## Stack

- **Python** pour la majorité des outils (scanners, OSINT, réseau, analyse)
- **Rust** / **C** pour le hardware embarqué et la performance
- **Tree-sitter** pour l'analyse statique de code PHP
- **Scapy** pour la manipulation de paquets réseau bas niveau
- **Flask** pour les dashboards web temps réel
- **Docker** pour les labs de sécurité conteneurisés
- **OWASP ZAP**, **Nmap**, **Masscan** comme outils intégrés
