# HoneyShield — site officiel

Site vitrine public pour HoneyShield, une initiative de cyberdéception et de R&D en cybersécurité à Lomé (Togo).

**Site prévu :** https://honeyshield.tech  
**Contact :** contact@honeyshield.tech  
**Fondateur :** founder@honeyshield.tech

## Contenu et exactitude

- Vitrine responsive, avec une version française et une version anglaise.
- Présentation d'un prototype HoneyShield associé à la JPOPE 2026.
- Feuille de route de R&D : honeypots, télémétrie, analyse IA et intégration SOC.
- Console interactive : **uniquement une simulation**, sans collecte réelle et sans backend.
- Aucun client ou financement non vérifié n'est revendiqué sur le site.

## Publication avec GitHub Pages

1. Ouvrir [Settings → Pages](https://github.com/hackus-mans/honeyshield-site/settings/pages).
2. Dans **Build and deployment**, choisir **Deploy from a branch**, branche **main**, dossier **/(root)**, puis **Save**.
3. Dans **Custom domain**, saisir `honeyshield.tech` puis enregistrer. Le dépôt contient déjà le fichier `CNAME`.
4. Chez le **fournisseur DNS effectivement autoritaire**, configurer les A de la racine `@` :

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

5. Facultatif : `www` en CNAME vers `hackus-mans.github.io`.
6. Une fois le certificat disponible, activer **Enforce HTTPS**.

**Sécurité :** vérifier la propriété du domaine dans les paramètres GitHub Pages pour limiter les risques de domain takeover.

**Ne pas toucher** aux MX, TXT SPF/DKIM/DMARC, ni à la vérification TXT de Google Postmaster. Ces enregistrements servent à la messagerie Titan et à son authentification.

### Vérification DNS sur Kali

```bash
dig NS honeyshield.tech +short
dig honeyshield.tech A +short
dig honeyshield.tech MX +short
dig honeyshield.tech TXT +short
```

Il faut utiliser le panneau correspondant aux **nameservers autoritaires**. Le domaine acheté chez .TECH ne signifie pas nécessairement que .TECH héberge actuellement la zone DNS.

## Modifier le site

Le site est volontairement statique et indépendant de services payants. L'accueil, le CSS et le JavaScript sont dans `index.html`. Modifier le fichier, faire un commit vers `main`, puis attendre la publication GitHub Pages.

> Le site n'est pas une preuve d'immatriculation de la société et n'implique pas à lui seul une éligibilité AWS Activate. Les affirmations commerciales doivent rester vérifiables.
