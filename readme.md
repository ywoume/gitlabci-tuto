Ex: assemblage d'une voiture
 - Créér un chassis
 - Créer une carroserie
 - Créer un moteur
 - Mettre le pneu
 - Assembler le tous et tester le tous
 
 Ce qui nous ammène à 2 process :
  - Assemblage
  - Test si l'assemblage s'est bien effectué
 
Pareil sur git lab on a 2 process à faire pour assembler une voiture
 - build 
 - test
 
 Concretement allons voir tous cela :
 
 ```bash
construire une voiture:
    script:
        - mkdir construire
        - cd construire
        - touch vehicule.txt
        # créons notre chassis
        - echo "Chassis" > vehicule.txt
        - echo "Carroserie" > vehicule.txt
        - echo "Moteur" > vehicule.txt
        - echo "Pneu" > vehicule.txt
    # look at the video
test la construction vehicule:
    script:
        # test permet de creer des expression conditionnels https://fr.wikipedia.org/wiki/Test_(Unix)
        - test -f build/vehicule.txt  
```