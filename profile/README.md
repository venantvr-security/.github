# venantvr.security

Boîte à outils offensive et défensive de cybersécurité : scanners de vulnérabilités, reconnaissance réseau, analyse statique de code, recherche en sécurité et outils IoT.

## Repos

### Analyse statique de code

**`Python.PHP.Sec.Scan`** <sup>public</sup>
*Python / tree-sitter* — Scanner de sécurité PHP par analyse statique : taint tracking forward, AST tree-sitter, 16 types de vulnérabilités (SQLi, XSS, RCE, SSRF...), rapports SARIF/HTML/terminal, 89 tests.

**`TypeScript.PHP.Sec.Scan`** <sup>public</sup>
*TypeScript / VS Code API* — Extension VS Code de détection de vulnérabilités PHP : taint tracking intégré à l'éditeur, diagnostics en temps réel, quick fixes, configuration via rules.yaml.

**`Python.Sqli.Detection`** <sup>privé</sup>
*Python* — Scanner d'injections SQL (basé sur DSSS) : fuzzing de paramètres QueryString, payloads d'injection, détection par diff de réponses HTTP (texte, code, titre, HTML).

**`Python.QueryStringsFromPhp`** <sup>privé</sup>
*Python* — Extracteur de query strings et chaînes SQL depuis du code source PHP pour alimenter d'autres outils de scan.

### Analyse de trafic et fichiers

**`Python.Har.Scanner`** <sup>privé</sup>
*Python / haralyzer* — Analyseur de fichiers HAR (HTTP Archive) : parsing du trafic capturé, extraction de métriques de performance, filtrage par domaine.

**`Python.HAR.ZAP`** <sup>public</sup>
*Python / Flask* — Plateforme DAST orchestrant OWASP ZAP via Docker : attaques Red Team (rejeu non authentifié, mass assignment, race conditions), détection IDOR multi-session, analyse passive des en-têtes, import OpenAPI, intégration CI/CD.

**`Python.AccessForbiddenFiles`** <sup>privé</sup>
*Python* — Scanner de fichiers à accès restreint : vérification que les règles .htaccess interdisent l'accès direct aux ressources sensibles (`.env`, `.git`, backups...) via requêtes GET/POST.

**`Python.Traversal.Vulnerabilities`** <sup>public</sup>
*Python* — Scanner de vulnérabilités path traversal (fork dotdotslash) : tests automatisés de séquences `../` sur des endpoints cibles, testé sur DVWA, bWAPP et VulnHub.

### Reconnaissance et réseau

**`Python.Nmap.Batch`** <sup>public</sup>
*Python / Flask* — Plateforme de scan réseau multi-outils (Nmap, Masscan, Netcat, Hping3, Curl, Scapy) avec stratégies d'évasion de pare-feu, intégration TOR, dashboard web temps réel via SSE, exécution parallèle adaptative.

**`Python.Dome.SubDomains`** <sup>public</sup>
*Python* — Énumération de sous-domaines (fork Dome) : mode passif OSINT (moteurs de recherche, APIs) indétectable + mode actif bruteforce DNS, multi-threadé, scan de ports optionnel.

**`Python.Osint.Blackbird`** <sup>public</sup>
*Python / aiohttp* — Outil OSINT de recherche de noms d'utilisateur sur 574+ plateformes (fork Blackbird), requêtes asynchrones, interface web intégrée (port 9797), export JSON.

**`Python.Arping`** <sup>public</sup>
*Python / Scapy* — Découverte de machines sur un sous-réseau via paquets ARP broadcast, affichage des correspondances IP/MAC.

**`Python.Apache.Logs`** <sup>privé</sup>
*Python / scikit-learn* — Analyseur de logs Apache : détection d'attaques par regex (SQLi, XSS, RCE, LFI) + clustering machine learning (K-Means, DBSCAN, hiérarchique, spectral) pour identifier les comportements anormaux.

**`Python.Network.Connections`** <sup>public</sup>
*Python / Scapy* — Surveillance réseau en temps réel : détection continue des machines connectées via requêtes ARP, affichage coloré des nouvelles connexions (IP + MAC).

### Recherche et démonstrations de sécurité

**`Python.Ransomware`** <sup>public</sup>
*Python / cryptography* — Projet éducatif : démonstration de chiffrement RSA/Fernet, changement de fond d'écran, note de rançon, mécanisme de déchiffrement par échange de clés.

**`Python.Session.Hijacking`** <sup>public</sup>
*Python / Flask* — Démonstration de détournement de session HTTP : injection de cookie volé via JavaScript côté client, accès non autorisé à une page protégée.

**`Python.CSRF.Demo`** <sup>privé</sup>
*Python / Flask* — Démonstration CSRF avec deux serveurs (banque + attaquant) : exploitation des cookies de session, tokens anti-CSRF, analyse de fichiers HAR.

**`Python.CORS.Handler`** <sup>privé</sup>
*Python / Flask* — Lab de test de configurations CORS : endpoints avec différentes mauvaises configurations, frontend d'exploitation JavaScript, proxy DNS.

**`Python.Network.Pivot`** <sup>privé</sup>
*Python / Docker* — Lab de pivot réseau conteneurisé : 3 machines (attaquant + DMZ + réseau interne), scripts de rebond sans Metasploit, sous-réseaux segmentés.

**`Python.Usb.Test`** <sup>privé</sup>
*Python / PyUSB* — Communication Python/Android via USB : exploration des bibliothèques usb4a, PyUSB, ADB et UsbManager Java.

### Anonymisation et TOR

**`Python.Tor.Proxy`** <sup>privé</sup>
*Python / GTK / Stem* — Proxy TOR avec interface système (system tray GTK) : rotation automatique d'IP via Stem, règles iptables pour forcer le trafic Tor, vérification d'anonymat.

**`Javascript.TOR.Workflow`** <sup>privé</sup>
*JavaScript* — Visualisations interactives de protocoles de sécurité : circuit TOR, négociation de clés, HTTPS/TLS, VPN IPSec, SSH, WebRTC, Zero Trust, DNS-over-HTTPS, blockchain PoW/PoS.

### Hardware et IoT

**`Raspberry.Hack`** <sup>privé</sup>
*C* — Analyse pédagogique d'un worm réel capturé ciblant Raspberry Pi : 4 phases documentées (persistance, C2 IRC Undernet, propagation SSH, minage crypto), code source décompilé.

**`Raspberry.IpBlocker`** <sup>public</sup>
*Python* — Génération de règles iptables pour bloquer des plages d'IP géolocalisées : agrégation de zones d'adresses, fusion des plages chevauchantes, filtrage par pays.

**`Python.PiZero.WiFi`** <sup>privé</sup>
*Python / Scapy / Flask* — Plateforme WiFi pour Raspberry Pi Zero : sniffing de paquets (PyShark + Scapy), déauthentification, localisation de chipsets, dashboard web Flask, alertes Telegram, persistance SQLite.

### Divers

**`Php.WordPress.Cypher`** <sup>privé</sup>
*PHP / OpenSSL* — Chiffrement de paramètres QueryString dans WordPress en AES-256-CBC via OpenSSL, masquage de paramètres sensibles dans les URLs.

## Stack

- **Python** pour la majorité des outils (scanners, OSINT, réseau, analyse)
- **Tree-sitter** pour l'analyse statique de code PHP
- **Scapy** pour la manipulation de paquets réseau bas niveau
- **Flask** pour les dashboards web temps réel
- **Docker** pour les labs de sécurité conteneurisés
- **scikit-learn** pour la détection d'anomalies par machine learning
- **OWASP ZAP**, **Nmap**, **Masscan** comme outils intégrés
