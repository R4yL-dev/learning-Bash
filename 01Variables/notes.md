# Variables

Une variable en Bash est crée lorsque nous lui donnons une valeur.
Une variable peu contenire un nombre, un caractère ou une string.
Les nom de variable sont sensible à la case et peuvent comporter des chiffres, des lettres et des "_".
Pour assigner une valeur à une variable, nous devons utilier le "=". Il ne faut surtout pas mettre d'espace autour !!

```bash
PRICE_PER_APPLE=5
MyFirstLetters=ABC
greeting='Hello           world!'
```

## Référencer une variable

Nous pouvons utiliser "\" afin d'escape les caractères splciaux

```bash
PRICE_PER_APPLE=5
echo "The price of an Apple is: \$HK $PRICE_PER_APPLE".
```

Encapsuler la variable avec ${} permet d'éviter les ambiguités.

```bash
MyFirstLetters=ABC
echo "The first 10 letters in the alphabet are: ${MyFirstLetters}DEFGHIJ"
```

Encapsuler le nom de la variable avec "" permet de presérver les espaces.

```bash
greeting="Hello         World!!"
echo $greeting" now with spaces: $greeting"
```

Nous pouvons assigner la valeur de retour d'une commande à une variable. Ceci s'appel la subsitution.
Pour substituer nous pouvons utiliser \`\` ou $().

```bash
FILELIST=`ls`
FileWithTimeStamp=/tmp/my-dir/file_$(/bin/date +%Y-%m-%d).txt
```

Dans cette exemple, quand le script est executé, la commande à l'intérieur de $() est executée et son retour est capturé.
