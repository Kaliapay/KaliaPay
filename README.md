# KaliaPay

Un module pour intégrer facilement KaliaPay dans votre application.

## Installation

Utilisez ces différents gestionnaires pour installer le module :

1. Utilisez npm

```bash

npm install mks-kaliapay

```
2. Utilisez yarn

```bash
$ yarn add mks-kaliapay
```

3. Utilisez pnpm:

```bash
$ pnpm add mks-kaliapay
```

### Utilisation du module

```javascript


// Utilisation du module kaliapay
const kaliapay = require('mks-kaliapay'); // Environnement serveur ou node.js
import * as kaliapay from 'mks-kaliapay';

// Vous devez nécéssairement renseigner ces informations ci-après
const tid = 'entrer votre-token-d\'authentification';  
const apikey = 'entrer votre-clé-api';
const service = 'entrer votre-service-id';

kaliapay.setTid(tid);
kaliapay.setApiKey(apikey);
kaliapay.setService(service);

// Exemple d'utilisation de la fonction Signin pour la connexion

const user = 'entrer votre-email';
const password = 'entrer votre-mot-de-passe';
kaliapay.Signin(user, password);

// Exemple d'utilisation de la fonction initialize pour initaliser un paiement
const amount = 100;
const custom_data = "entrer votre-custom_data";
kaliapay.initialize(amount, custom_data);

// Exemple d'utilisation de la fonction getPaymentDetails pour voir les détails d'un paiement

const reference = 'entrer votre-référence';  // Définissez la référence, vous pourrez l'avoir lors de la requête d'un paiement 
kaliapay.getPaymentDetails(reference);

```

#### API

Explication des termes

`Signin(user, password)`

Cette fonction permet de se connecter à KaliaPay. Elle prend deux paramètres :

`user`: L'identifiant de l'utilisateur (email).
`password`: Le mot de passe de l'utilisateur.

`initialize(amount, custom_data)`

Cette fonction permet d'initialiser un paiement. Elle prend deux paramètres :

`amount`: Le montant du paiement.
`custom_data`: Des données personnalisées associées au paiement.

`getPaymentDetails(reference)`

Cette fonction permet d'obtenir les détails d'un paiement. Elle prend un paramètre :

`reference`: La référence du paiement.

`setTid(value)`

Cette fonction permet de définir le token d'authentification (tid).

`setApiKey(value)`

Cette fonction permet de définir la clé API (apikey).

`setService(value)`

Cette fonction permet de définir l'identifiant du service (service).
