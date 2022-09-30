# Le reactJS
- React est une bibliothèque JavaScript open-source 📚
- Elle est utilisée pour gérer la couche d'affichage des applications web et mobiles 🖥️📱
- L'objectif principal de React est d'être rapide, évolutif et simple.
- React se base sur un modèle MVC (Modèle Vue Controller) 
- React possede une communauté de développeurs importante ce qui permet une facilité dans la résolution des problèmes ou l'ajout de dépendance 📦


## Pré-requis

1. Un ide sachant reconnaitre reactJS (Visual studio code par exemple) 

2. Assurez-vous de disposer d’une version installée de Node.js (https://nodejs.org/fr/) suffisamment récente.

## Votre premier projet

Maintenant que l'installation de Node.js a été effectué vous allez pouvoir créer votre premier projet 

```
npx create-react-app mon-app
cd mon-app
npm start
```

🎊 Voila votre premier projet de créé ! 🎊

`Que s'est-il passé  lors de la commande "npx create-react-app mon-app" et qu'est ce que "create-react-app" ?`

`Si l'on éjecte "create-react-app" de notre projet que se passe-t-il ?`

`Un fichier nommé "package.json" se trouve à la racine de votre projet à quoi sert-il et que contient ce fichier précisément ? `

### Mon premier composant

`Qu'est ce qu'un composant ?`

`A quoi sert le fichier App.js , App.css et App.test.js ?`

`Comment notre application choisis d'afficher le contenu de App.js lors de son lancement ?`

Dans le fichier App.js remplacer son contenue par : 

```
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
      <h1>Ceci est un titre dans la function App</h1>
      </header>
    </div>
  );
}

export default App;
```

Ensuite, nous allons créer un composant qui nous affichera un texte sous le `<h1></h1>` de notre page.

Pour faire cela au-dessus de notre composant App() , nous allons créer un composant nommé Information qui aura la forme :

```
export function Information() {
  return <h2>je suis un sous-titre de la function Information</h2>
 }
 ```
 
 `Il faut maintenant l'insérer dans notre page à vous de jouer !!`
 
---

Nous avons donc créer un composant nommé Information() celui-ci a pour objectif d'afficher un texte dans notre page, mais il se trouve dans le même fichier que notre fonction "App". 

`Vous devez le sortir de App.js et l'insérer dans un fichier nommé Information.js et vérifier que tous fonctionne correctement.`

Il est préférable de découper son code sous forme de composant, donc avoir un fichier avec un composant permet de maintenir le projet de manière plus efficace et d'avoir une lecture de celui-ci plus efficace.

Nous avons donc deux fichiers un qui contient la composant App()  et un autre qui contient Information(), la prochaine étape est de pouvoir modifier le texte de la fonction d'information. 
Pour cela, il existe ce qu'on appelle des "props", les props servent a passer en paramètre des informations a un composant.

Pour faire cela, il suffit de rajouter a un composant une variable props dans ses paramètres donc par exemple : 

```
export exemple(props){}

```

ensuite, il faut définir quels types de props, nous voulons lui passer en paramètre. 
Dans notre exemple, nous voulons lui passer un texte soit : 

```
<Exemple texte=""/>
```

Cela nous permet donc de récupérer le paramètre texte dans notre composant :

```
export exemple(props){
  return <p>{props.texte}</p>
}
```

Dans notre composant information, nous voulons lui passer en paramètre la date actuelle sous forme dd/MM/yyyy.

Il faut donc créer une function dans le composant App() qui passe la date en paramètre de `<information/>`.

---

Nous avons vu comment passer une information d'un composant parent à son enfant, mais il est aussi possible de passer de l'information d'un enfant à son parent. 
Pour cela, il faut comprendre le hook "useState".

`A quoi sert le hook "useState" et comment l'utiliser` 

Une fois que nous avons compris comment fonctionne "useState", nous allons créer un composant qui contient un `<input/>` qui retournera un chiffre qui  sera envoyé au composant principal.

`Vous devez maintenant faire en sorte de récupéré l'information du input dans "function App() {}" et de l'afficher dans la page`

## Besoin d'aide ? Attention à internet

Sur internet, vous trouverez beaucoup de solutions pour créer un composant. Mais attention, un grand nombre de ces solutions nous proposes des composant écrits en Class et non en function. 


`Transformer notre function App() en class `


`Quelle est la différence entre l'écriture d'un composant en class et en function ? `


## Pour le cours suivant 

Nous avons vu précédemment `useState` qui est un hook, il existe une multitude de hook.
Pour le prochain cours, vous allez devoir écrire un morceau de code qui mettra en pratique le hook qui vous sera attribué et vous présenterez celui-ci en début du prochain cours.



