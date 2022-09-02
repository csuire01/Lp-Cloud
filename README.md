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

`Que c'est-il passer lors de la commande "npx create-react-app mon-app" et qu'est ce que "create-react-app" ?`

`Si l'on ejecte "create-react-app" notre application que ce passe-t-il ?`

`Un fichier nommé "package.json" se trouve à la racine de votre projet a quoi sert-il et que contient se fichier précisement ? `

### Mon premier composant

`A quoi sert le fichier App.js , App.css et App.test.js ?`

`Comment notre application choisis d'afficher le contenue de App.js lors de son lancement ?`

Dans le fichier App.js remplacer son contenue par : 

```
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
      <h1>Bonjour je suis entrain de modifier cette page</h1>
      </header>
    </div>
  );
}

export default App;
```

Ensuite nous allons créer un composant qui nous affichera un texte sous le <h1></h1> de notre page.

Pour faire cela au dessus de notre composant App() , nous allons créer un composant nommé Information qui aura la forme

```
export function Information() {
  return <h2>"information à afficher"</h2>
 }
 ```
 
 `Il faut maintenant l'insérer dans notre page à vous de jouer !!`
 

Nous avons donc créer un composant nommé Information() celui-ci a pour objectif de d'afficher un texte dans notre page, mais il se trouve dans le même fichier que notre fonction "App". 

`Vous devez le sortir de App.js et l'insérer dans un fichier nommé Information.js et vérifier que tous fonctionne correctement.`


Nous avons donc deux fichiers un qui contient la composant App()  et un autre qui contient Information(), la prochaine étapes est d epouvoir modifier le texte d'information. 
Pour cela il existe ce qu'on appel des "props", les props servent a passer en parametre des informations a un composant.

Pour faire cela il suffit de rajouter a un composant une variable props dans ses paramètres donc par exemple : 

```
export exemple(props){}

```

ensuite il faut definir quels types de props, nous voulons lui passer en paramètre. 
Dans notre exemple, nous voulons lui passer un texte soit : 

```
<Exemple texte=""/>
```

cela nous permet donc de recuperer le parametre texte dans notre composant :

```
export exemple(props){
  return <p>{props.texte}</p>
}
```

Dans notre composant information nous voulons lui passer en paramètre la date actuelle sous forme dd/MM/yyyy.

Il faut donc créer une fonction dans le composant App() qui passe la date en paramètre du composant information.

//une props enfant -> parent 
//différence entre class et function 
//Les hooks



