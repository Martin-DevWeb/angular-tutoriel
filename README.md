# Partie 1 : Initiation

- Les boucles dans le fichier HTML (`ngFor, ngIf`) ont l'air vraiment pratique ! J'aime déjà.
- En fait, tout à l'air extremement dynamique, c'est magnifique. Les crochets, accolades, etc sont partout dans le HTML.
- La facilité avec laquelle on crée un nouveau component, easy peasy lemon sqeezy !
- La balise personnalisé avec le nom de l'enfant me rend perplexe mais plutôt enthousiaste pour la suite et la lecture globale du code.
- Un peu compliqué au premier abord pour passer les données d'un parent à un enfant et inversement mais le réflexe doit se prendre au fur et à mesure.

# Partie 2 : Routing

- Le `routerLink` semble plutôt facile à utiliser et assez clair.
- Par contre pour la visualisation des détails, c'est un peu le bazar. Il faudra revoir `OnInit, gnOnInit`, j'ai pas tout saisi.

# Partie 3 : Data

- La partie service est claire, c'est une instace de classe accessible sur l'ensemble de l'application (via des dépendances).
- La creation du panier avec une liste de produit que l'on `push` et que l'on peut clear avec une liste vide était bien compréhensible.
- L'affichage des items dans le panier c'est fait sans problème.
- `HttpClient` semble un peu plus compliqué mais abordable (à ne pas oublier afin d'utiliser des APIs).
- La méthode `get()` récupère les données de l'API.
- Se renseigner sur RxJS.
- Problème sur :
  `export class ShippingComponent implements OnInit {
  constructor(private cartService: CartService) {}

  shippingCosts!: Observable<{ type: string; price: number }[]>;

  ngOnInit(): void {
  this.shippingCosts = this.cartService.getShippingPrices();
  }
  }`

  OK c'était un oubli sur le get(), je n'avais pas appelé le `.json`, merci Jérémy !

# Partie 4 : Formulaire

- La construction du modèle de formulaire est assez claire. Les méthode inhérentes comme `group()` ou `reset()` le sont aussi.
- Il ne faut pas oublier de faire référence au `formControlName` pour lier l'input au constructeur du groupe de formulaire.
