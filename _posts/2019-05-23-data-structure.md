---
layout:     post
title:      Les structures de données, Array et Set en Ruby

date:       2019-05-23
summary:    
categories: Developper skills
mathjax: true
---

Voici quelques problèmes d'entretient d'embauche, tirés du ["Workshop Paris Ruby "](https://www.meetup.com/fr-FR/parisrb/?chapter_analytics_code=UA-24741027-2).

![ruby](/images/ruby2.png)

Nous essaierons de faire attention à la complexité temporelle/spatiale, le fameux O(n).

Je tiens à préciser que c'est pour un niveau junior, et si vous voulez essayer, lisez l'énoncé et regarder les exemples. Si vous le sentez, écrivez vos tests d'abord !

# Les Tableaux 

### Les anagrammes

**Problème**

Vérifier si deux chaînes de caractères données sont des anagrammes. 

>*Un anagramme* est présent si les deux chaînes contiennent exactement les mêmes lettres, chacune le même nombre de fois (donc en extrayant toutes les lettres de la première chaîne, vous pouvez écrire la seconde sans qu'une lettre de la première ne manque ou soit en trop).


*Par exemple*

*"public relations"* est un anagramme de "crap built on lies."

*"clint eastwood"* est un anagramme de *"old west action"*

**Note:** "on ne tient pas compte ni des espaces, ni des majuscules. Ainsi "d go" est un anagramme de "God", pareil pour "dog" et "o d g"."

---

**Solution**

```ruby
def anagrams(string1, string2)
	# à vous 
end
```


---

C'est partie! 



```ruby 
	def anagrams(string1, string2)
	#On compare les 2 chaines de caractère
	string1.chars.sort == string2.chars.sort

end 
puts anagrams("god";"dog")
```

"The `chars method` returns an enumeration of the string's characters."

Et sa nous donne: 

![anagram](/images/anagram.png)

---