# Variables et console.log()

_Cette série de cours demande un minimum de base en programmation, prenez votre temps_

> Sur ce second épisode de la série, nous allons directement nous plonger dans du code en commençant par les fondamentaux (Les bases de tout langages)

## Types de valeurs et console.log()

Dans la plupart des langages, il est possible d'envoyer un message dans notre **console de commande (terminal)**. Par exemple si on écrit :

```js
console.log(26)
```

Le nombre 26 sera directement afficher dans notre **terminal** au lancement du programme.

> Vous ne voyez pas de terminal ? Pour l'ouvrir: faîtes la combinaison de touche `CTRL gauche + ù` ou cliquez sur `view > terminal` dans la barre d'outil de VSC tout en haut

> Comment lancer un programme avec nodejs ? Il suffit de taper la commande `node nomdemonfichier.js` dans votre **terminal**. Nodejs executera ensuite le fichier indiqué

Dans ce premier exemple, nous avons envoyer un nombre. On aimerait maintenant essayer d'envoyer du texte, non ? Oui, vous ne pouvez pas mettre votre texte en brut dans le code... Sinon javascript ne va pas comprendre si c'est du code ou non, il faut donc lui indiquer que c'est du texte et il existe des **balises** pour ça:

```js
console.log('Ceci est bien du texte')
```

Mais on va faire face à nouveau soucis, imaginons que nous voulons mettre un guillemet dans notre texte ("), cela va interférer avec nos balises qui indiquent que c'est du texte. Par chance, il existe d'autres balises et un moyen pour dire au code d'ignorer notre guillemet :

```js
console.log("J'- j'a- j'ai dit \"pouet\" !") // \ nous permet de dire au code d'ignorer le caractère qui suit
console.log('J\'ai di "pouet" !') // Vous pouvez aussi utiliser ' comme balise
console.log(`J'ai dit "pouet" !`) // Vous pouvez aussi utiliser ` comme balise
```

> Oui, vous pouvez mettre des commentaires dans votre code avec `// commentaire` ou `/* commentaire */` ! C'est quoi un commentaire ? C'est des notes ou indications pour les humains, votre code ignorera cette partie

Maintenant vous allez dire, mais la balise ` est géniale ! elle permet de pas s'embêter avec les " et '. Oui je suis d'accord avec vous, et elle permet même de mettre du code directement dans du texte :

```js
console.log(`1 + 1 = ${1 + 1} !`) // Output : 1 + 1 = 2 !
/* Alors que sans la balise ` */
console.log('1 + 1 = ' + (1 + 1) + '!') // Output : 1 + 1 = 2 !
/* Ca devient desuite plus compliqué ! */
```

Mais c'est génial diriez vous ! Je vais l'utiliser partout ! _Inspire..._ **NON**, il y a un piège. Cette balise propose plus de chose que les autres, ce qui veut aussi dire qu'elle est plus lente ! Si vous comparé un code avec qui n'utilise que cette balise et un autre code qui utilise les balises selons ses besoins, celui qui fait la plus attention à ses balises (donc le second) sera plus rapide et propre !

> Nous avons déjà vu 2 types de valeurs avec les quelques exemples si dessus:
>
> - Les chaines de caractères (texte) que l'on nomme string en **anglais**
> - Les nombres que l'on nomme number en **anglais**
>
> Comment voir le type d'une valeur ?
>
> ```js
> console.log(typeof "J'adore les furets") // Output : string
> console.log(typeof 1 + 7 * 78) // Output : number
> ```
>
> En plaçant `typeof` devant votre valeur, vous obtiendrez le type de sa valeur  
> Il existe bien d'autres types de valeur que nous verront au fur et à mesure

## Les variables

Les variables sont des boites qui contiennent une valeur... Ca sera peut être plus parlant avec un exemple :

```js
const boite = 'valeur'
const number = 4.8

const key = 'value' // La valeur de key est "value" qui est un string
```

Nous indiquons avec le symbole `=` que la boite contient un string, maintenant :

```js
const key = 'value'

console.log(key) // Output : value
console.log(typeof key) // Output : string
```

Vous pouvez donc directement récupérer les valeurs d'une variable en appelant leur nom

> Vous pouvez aussi définir une variable avec `let` au lieu de `const`. Ce que ça change ? Ca vous permet de modifier la valeur de votre variable, ce qui n'est pas possible avec const :
>
> ```js
> const key = 'value'
> key = 'other value' // Output : Error
>
> let key = 'value'
> key = 'other value'
> console.log(key) // Output : other value
> ```

Il est aussi possible de faire des opérations simples avec des variables :

```js
let a = 4
let b = 6.5
const str = 'Ce ceci est du texte : '

console.log(a + b) // Output : 10.5

a++ // On incrémente de 1 la valeur de a, c'est à dire qu'on ajoute 1
console.log(a) // Output : 5
a-- // On désincrémente de 1 la valeur de a, on retire 1

b = a / 2 + b // On redéfini b = 4 / 2 + 6.5
console.log(b) // Output : 8.5

console.log(str + a) // Output : Ce ceci est du texte : 4
```
