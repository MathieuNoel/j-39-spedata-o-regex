# Leçon 13 : Travail sur les groupes

Nous l'avons vu lors des leçons précédentes, tous les quantificateurs (`*`, `+`, `{m,n}` et `?`) sont utilisables à l'intérieur des patterns de capture de groupe. C'est d'ailleurs la seule façon de les appliquer sur une séquence de caractères plutôt que sur un caractère isolé.

Imaginons par exemple que nous travaillons sur une liste de numéros de téléphone dont certains sont précédés de l'indicatif international (une série de 3 chiffres, 033 pour le france). Le pattern correct doit vérifier l'existence du groupe entier avec `(\d{3})?` et pas chaque caractère pris individuellement.

Certaines versions du moteur des expressions régulières permettent la création de groupes non-capturants. Ils permettent de correspondre à un groupe de caractères mais ne capturent pas la valeur qui ne sera pas dans les résultats de l'extraction. Pour ce faire, il suffit de commencer le pattern du groupe par `?:` comme par exemple `(:?\d+)`

## Exercice

Vous trouverez ci-dessous une liste de résolutions d'affichage courantes, essayez de capturer la largeur et la hauteur de chacune d'entre elles.

| tâche   | texte     | groupes capturés |
| ------- | --------- | ---------------- |
| capture | 1280x720  | `1280` `720`     |
| capture | 1920x1600 | `1920` `1600`    |
| capture | 1024x768  | `1024` `768`     |
