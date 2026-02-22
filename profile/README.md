# venantvr.security

Outils offensifs et defensifs de cybersecurite : scanners de vulnerabilites, reconnaissance reseau, analyse de code, recherche en securite.

## Repos

### Scanners et analyse de code

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.PHP.Sec.Scan` | Python | Scanner de securite PHP par analyse statique (taint tracking, tree-sitter, 16 types de vulns) |
| `TypeScript.PHP.Sec.Scan` | TypeScript | Scanner de securite PHP (version TypeScript) |
| `Python.Sqli.Detection` | Python | Detection d'injections SQL |
| `Python.Har.Scanner` | Python | Analyseur de fichiers HAR pour la securite |
| `Python.HAR.ZAP` | Python | Scanner HAR avec integration OWASP ZAP |
| `Python.QueryStringsFromPhp` | Python | Extraction de query strings depuis du code PHP |
| `Python.AccessForbiddenFiles` | Python | Scanner de fichiers a acces interdit |
| `Python.Traversal.Vulnerabilities` | Python | Scanner de vulnerabilites path traversal |

### Reconnaissance et reseau

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Dome.SubDomains` | Python | Enumeration de sous-domaines |
| `Python.Osint.Blackbird` | Python | Outil OSINT base sur Blackbird |
| `Python.Nmap.Batch` | Python | Automatisation de scans Nmap en batch |
| `Python.Arping` | Python | Scanner reseau ARP ping |
| `Python.Apache.Logs` | Python | Analyseur de logs Apache orientee securite |
| `Python.Network.Connections` | Python | Monitoring de connexions reseau |

### Recherche en securite

| Repo | Stack | Description |
|------|-------|-------------|
| `Python.Ransomware` | Python | Recherche et analyse de ransomware |
| `Python.CSRF.Demo` | HTML | Demonstration de vulnerabilites CSRF |
| `Python.Session.Hijacking` | Python | Illustration de session hijacking |
| `Python.CORS.Handler` | Python | Tests de configurations CORS |
| `Python.Network.Pivot` | Python | Outils de pivot reseau |
| `Python.Usb.Test` | Python | Outils de test de securite USB |
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

- **Python** pour la majorite des outils (scanners, OSINT, reseau)
- **C** pour le hardware embarque (Raspberry Pi)
- **Tree-sitter** pour l'analyse statique de code PHP
- **OWASP ZAP** pour l'analyse dynamique
- **Nmap** pour la reconnaissance reseau
