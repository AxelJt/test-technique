# test-technique

# Contexte

Une des équipes produit d'Evaneos a décidé d'améliorer une des pages du site afin d'améliorer son taux de conversion.
Pour rappel, on appelle le taux de conversion le nombre de demande de devis opérés sur la page divisé par le nombre de sessions sur ladite page.  
À cette fin, l'équipe a décidé d'implémenter une nouvelle fonctionnalité dont on soupçonne qu'elle pourrait considérablement améliorer l'expérience des utilisateurs. Pour s'en assurer, il a été décidé de mettre en ligne deux versions en parallèle :  
* une version qui contient la page **sans** la nouvelle fonctionnalité (version A)
* une version qui contient la page **avec** la nouvelle fonctionnalité (version B)  


À l'issue d'un mois de test:  
* la version A a eu 4000 sessions et 200 conversions (taux de conversion de 5%).
* la version B a eu 4000 sessions et 260 conversions (taux de conversion de 6.5%).

La question:  **ce résultat est-il statistiquement significatif , i.e la différence constatée entre les deux versions est-elle uniquement due à la nouvelle fonctionnalité?**
    
Vous essayerez de répondre à cette question en expliquant par étape le raisonnement et en affichant
des simulations du test.

### Approche conseillée

* Qu'est-ce qu'un A/B Test : https://www.definitions-marketing.com/definition/a-b-test/  
Reéxpliquer brièvement.  

  
*  On peut modéliser l'expérience de conversion par [une loi binomiale](https://fr.wikipedia.org/wiki/Loi_binomiale). 
Coder une fonction python qui simule le nombre de conversions d'une page qui a 5000 sessions sur la page et un taux de conversion en moyenne de 7%.  


* Si on répète l'expérience 10000 fois et qu'on trace l'histogramme du nombre de conversions, quelle distribution reconnait-on? Vous préciserez la moyenne et la variance de la distribution.  


* En déduire la probabilité d'obtenir **375 ou plus conversions** (i.e un taux de conversion réel supérieur à 7.5%).


* On estime qu'un taux de conversion est _anormalement élevé_ (i.e que la différence n'est pas due au hasard mais bien à l'efficacité de la nouvelle fonctionnalité) si la probabilité d'avoir autant de conversions est inférieure à 5%. On dit alors que la différence est statistiquement significative. Est-ce le cas ici?


* On réitère les simulations sauf que cette fois la page a 10000 sessions (et le même taux de conversion moyen). On cherche cette fois-ci à voir la probabilité d'avoir au moins 750 conversions.


* Conclure sur l'intérêt d'avoir plus de sessions pour déterminer l'efficacité d'une nouvelle fonctionnalité.


* Tracer sur un histograme le seuil au-delà duquel on atteint la significativité statistique (toujours dans l'expérience avec 10000 sessions).


* Tenter de répondre à la question initiale en répétant le raisonnement précédent.


**Question subsidiaire**:
Plutôt que de mettre en ligne les deux versions en même temps, un membre de l'équipe propose de mettre d'abord en ligne la version A, puis de mettre en ligne la version B. Qu'en pensez-vous?
