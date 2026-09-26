# Correspondance images ↔ rapport

Référence utile si tu veux légender précisément chaque capture ailleurs (LinkedIn, présentation, etc.).

## architecture/
| Fichier | Contenu |
|---|---|
| architecture-avant.png | Réseau AVANT (comptes locaux, HTTP/FTP en clair, WiFi WPA2-PSK) |
| architecture-apres.png | Réseau APRÈS (AD + PKI, HTTPS, LDAPS, WPA3-Enterprise) |

## screenshots/ad/ — VM1 (AD DS) + VM5 (client)
| Fichier | Contenu |
|---|---|
| 01-vm1-ip-config-general.png | Fenêtre propriétés réseau VM1 |
| 02-vm1-ip-config-ipv4.png | Propriétés IPv4 remplies sur VM1 |
| 03-vm1-nom-dc-ad.png | Nom "DC-AD" dans les propriétés système |
| 04-vm1-addc-installation-success.png | Installation AD DS : Success True |
| 05-vm1-connexion-administrator.png | Connexion TECHSECURE\Administrator après redémarrage |
| 06-vm1-get-addomain.png | Résultat Get-ADDomain (techsecure.local) |
| 07-vm1-ous-dsa-msc.png | OUs IT, RH, Finance, Computers dans dsa.msc |
| 08-vm1-utilisateurs-ous.png | Utilisateurs créés dans leurs OUs |
| 09-vm1-grp-vpn-membres.png | Groupe GRP_VPN (Ali, Sana, Karim) |
| 10-vm5-jonction-domaine.png | VM5 jointe au domaine techsecure.local |
| 11-vm5-connexion-bensalah.png | Connexion avec TECHSECURE\a.bensalah |

## screenshots/pki/ — VM2 (AD CS) + VM5 (magasin de certificats)
| Fichier | Contenu |
|---|---|
| 01-vm2-jonction-domaine.png | VM2 jointe au domaine |
| 02-vm2-adcs-installation-success.png | Installation AD CS : Success True |
| 03-vm2-rootca-config.png | Configuration de la Root CA |
| 04-vm2-certsrv-rootca-demarree.png | certsrv.msc : TechSecure-RootCA démarrée |
| 05-vm2-certificat-web-emis.png | Certificat web.techsecure.local émis par la CA |
| 06-vm2-template-cert-802-1x-certtmpl.png | Template Cert-Client-802.1X dans certtmpl.msc |
| 07-vm2-template-certificate-templates.png | Template visible dans Certificate Templates (certsrv.msc) |
| 08-vm1-gpo-autoenrollment-enabled.png | Paramètre Auto-Enrollment "Enabled" (GPO) |
| 09-vm1-gpupdate-force.png | Mise à jour de la stratégie réussie |
| 10-vm5-certlm-rootca-confiance.png | certlm.msc : TechSecure-RootCA dans les autorités de confiance |

## screenshots/radius/ — VM3 (NPS/RADIUS)
| Fichier | Contenu |
|---|---|
| 01-vm3-nps-installe-enregistre-ad.png | NPS installé et enregistré dans AD |
| 02-vm3-client-radius-ap-wifi.png | Client RADIUS AP-WiFi (192.168.10.50) configuré |
| 03-vm3-network-policy-eap-tls.png | Network Policy EAP-TLS (condition GRP_VPN) |

## screenshots/apache/ — VM4 (Apache HTTPS)
| Fichier | Contenu |
|---|---|
| 01-vm4-ip-statique.png | IP statique 192.168.10.40 sur VM4 |
| 02-vm4-apache-openssl-install-1.png | Installation Apache2 + OpenSSL (1/2) |
| 03-vm4-apache-openssl-install-2.png | Installation Apache2 + OpenSSL (2/2) |
| 04-vm4-csr-genere-terminal.png | CSR généré dans le terminal Ubuntu |
| 05-vm4-apache-https-running.png | Apache2 actif (running) avec HTTPS |
| 06-vm4-firefox-avertissement-ca-privee.png | Avertissement Firefox : CA privée non reconnue |
| 07-vm4-certificat-details-firefox.png | Détails du certificat X.509 (Firefox) |
| 08-vm4-connexion-https-validee.png | Connexion HTTPS validée |

## screenshots/kali/ — VM6 (tests de sécurité)
| Fichier | Contenu |
|---|---|
| 01 à 04-nmap-scan-reseau-*.png | Scan nmap du réseau 192.168.10.0/24 |
| 05, 06-responder-0-hash-ntlm-*.png | Responder actif : 0 hash NTLM capturé |
| 07 à 09-openssl-certificat-apache-*.png | openssl : certificat Apache signé par TechSecure-RootCA |
| 10 à 12-certificat-x509-complet-*.png | Détail complet du certificat X.509 (Subject, Issuer, SHA-256) |
| 13, 14-ldapsearch-annuaire-ad-*.png | ldapsearch : requête LDAP vers l'annuaire AD |


