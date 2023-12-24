# React Native
Créer un nouveau projet
```sh
$ npx create-expo-app --template
  > Blank (Typescript)
```

Le projet se créer avec `npm` mais je te conseille d'utiliser `yarn` pour du ***React Native***.
*(Ça tu sais faire, tu supprimes le `package-lock.json` et les `node_modules/`)*
```sh
$ yarn install
```
*(il y a des warnings mais t'inquiètes ça fait ça quand c'est neuf)*

Faudra installer l'app `Expo Go`, et pour lancer ton app tu run la cmd en dessous et tu scan le qr code
```sh
$ npx expo start
```

## Structure
Comme le `index.html` en ***Vue.js***, le point d'entrée de ton projet c'est le fichier `App.tsx` à la racine.
La base évidemment, petit dossier `src/` à la racine du projet. 

Pour les dossiers qui vont se retrouver dans le `src/`, je te met à gauche l'équivalent ***Vue.js*** (si le dossier n'a pas le même nom mais sert à la même chose) et à droite la convention ***React Native*** (convention que j'ai trouvé et que j'ai décidé d'appliquer).
- `views` => `screens` | Pages principales de ton app (*Login*, *SignUp*, *Home*, *Profile*, etc.)
- `components` | Les composants réutilisables pour ton app (*ewi comme en **Vue.js***), ne pas hésiter à faire des composants pour les `boutons`, `inputs`, etc.
- `interfaces` | C'est du `Typescript` alors oui tu auras sûrement besoin d'interfaces
- `services` | Si besoin de se connecter à une API, les services qui sont bien utiles
- `utils` | Pour les fonctions globales à ton app (encore une fois, pareil que pour ***Vue.js***)
- `validations` | Alors ça j'en avais pas utiliser, mais ça s'utilise aussi avec ***React Native*** (j'ai vu qu'un mec a eu des erreurs, alors si jamais [GitHub - Ussage with react native](https://github.com/typestack/class-validator/issues/1746))
- `router` | Tu en aura pas, je te le met en précision mais le router sera gérer par la navigation (à voir plus bas)
- `store` => `contexts` | Pour stocker des informations globalement dans ton app de la même façon que le `store` ***Vue.js***. Tu auras plus de précision là dessus plus bas également sur la partie **Context**

## Navigation
Pour la navigation (changement de page, sidebar, bottombar, etc.) [React Navigation](https://reactnavigation.org/docs/getting-started).
En fait, la `navigation` c'est comme le `router` de ***Vue.js*** mais avec plus de chose.
Ce qui est bien c'est que tu peux cumuler les navigations.

## Context
C'est une notion assez complexe, alors je te met la doc et si jamais t'as besoin d'un exemple plus poussé hésite pas à me demander.
- Doc : [Context](https://react.dev/learn/passing-data-deeply-with-context)

Fonction que tu retrouves dans la doc du `Context`
- [createContext](https://react.dev/reference/react/createContext)
- [useContext](https://react.dev/reference/react/useContext)

## Voir plus
Alors pour finir évidement la doc ***Expo***. Tu auras pleins de composants et de librairies trop stylés, mais ça je te laisserai voir par toi même.
- [Expo](https://expo.dev/)
- [Librairies & composants](https://docs.expo.dev/versions/latest/)

## À venir
- SafeAreaContext
- ImagePicker (et différent picker)
