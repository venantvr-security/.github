# venantvr.security

Outils offensifs et défensifs de cybersécurité : scanners de vulnérabilités, reconnaissance réseau, analyse de code, recherche en sécurité.

## Repos

### Scanners et analyse de code

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.PHP.Sec.Scan` | Python | Scanner de sécurité PHP par analyse statique (taint tracking, tree-sitter, 16 types de vulns) |
| `TypeScript.PHP.Sec.Scan` | TypeScript | Scanner de sécurité PHP (version TypeScript) |
| `Python.Sqli.Detection` | Python | Détection d'injections SQL |
| `Python.Har.Scanner` | Python | Analyseur de fichiers HAR pour la sécurité |
| `Python.HAR.ZAP` | Python | Scanner HAR avec intégration OWASP ZAP |
| `Python.QueryStringsFromPhp` | Python | Extraction de query strings depuis du code PHP |
| `Python.AccessForbiddenFiles` | Python | Scanner de fichiers à accès interdit |
| `Python.Traversal.Vulnerabilities` | Python | Scanner de vulnérabilités path traversal |

### Reconnaissance et réseau

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Dome.SubDomains` | Python | Énumération de sous-domaines |
| `Python.Osint.Blackbird` | Python | Outil OSINT basé sur Blackbird |
| `Python.Nmap.Batch` | Python | Automatisation de scans Nmap en batch |
| `Python.Arping` | Python | Scanner réseau ARP ping |
| `Python.Apache.Logs` | Python | Analyseur de logs Apache orientée sécurité |
| `Python.Network.Connections` | Python | Monitoring de connexions réseau |

### Recherche en sécurité

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Ransomware` | Python | Recherche et analyse de ransomware |
| `Python.CSRF.Demo` | HTML | Démonstration de vulnérabilités CSRF |
| `Python.Session.Hijacking` | Python | Illustration de session hijacking |
| `Python.CORS.Handler` | Python | Tests de configurations CORS |
| `Python.Network.Pivot` | Python | Outils de pivot réseau |
| `Python.Usb.Test` | Python | Outils de test de sécurité USB |
| `Python.Tor.Proxy` | Python | Outils TOR |
| `Javascript.TOR.Workflow` | JavaScript | Automatisation de workflows TOR |

### Hardware et IoT

| Repo | Stack | Description |
|------|-------|-------------|
| `Raspberry.Hack` | C | Outils de hacking Raspberry Pi |
| `Raspberry.IpBlocker` | Python | Blocage d'IP sur Raspberry Pi |
| `Python.PiZero.WiFi` | Python | Outils WiFi pour Raspberry Pi Zero |

### Divers

| Repo | Stack | Description |
|------|-------|-------------|
| `Php.WordPress.Cypher` | PHP | Utilitaires de chiffrement WordPress |

## Stack

- **Python** pour la majorité des outils (scanners, OSINT, réseau)
- **C** pour le hardware embarqué (Raspberry Pi)
- **Tree-sitter** pour l'analyse statique de code PHP
- **OWASP ZAP** pour l'analyse dynamique
- **Nmap** pour la reconnaissance réseau
