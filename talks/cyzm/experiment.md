#EXPERIMENTS

=====

##results:Tree parsing
##filter out verbs in the sentence of the minimal distance on the grammar tree
=====
example:

* verb results for "STEVE JOBS" and "PIXAR"

There are some correct relations

<pre>
	# correct relations
	co-founded
	served.
	
</pre>	


however some are affected by the grammar structure(mainly clauses） 

* XXX announced that XXX
* XXX declared that XXX


<pre>	
	#in clauses
	announced expired.
	announced expired.
	announced had agreed.
	floyd described interfered.
	revealed advised understand.
</pre>	

<pre>
	#passive voice
	dedicating was wrote.
	dedicating was wrote was dear guiding.
	are dedicated.
	bought was given.
	was running 
	tried
	failed 
</pre>

=====

the relationship between:
* "mona lisa" "renaissance"

	* da_vinci renaissance
	
<pre>
	saw known
	inspired.
	inspired.
	were making.
</pre>
	
	* mona lisa da_vinci
	
<pre>
	began painting.
</pre>



=====

## results: 
## using the common ancestors of 2 entities in the dependencies tree
 
=====


1. relationship between Jobs,Pixar

<pre>
	[('jobs', 'pixar', {'verb': 'co-founded'}),
	 ('jobs', 'pixar', {'verb': 'bought'}),
	 ('jobs', 'pixar', {'verb': 'announced'}),
	 ('jobs', 'pixar', {'verb': 'tried'}),
	 ('jobs', 'pixar', {'verb': 'worked'}),
	 ('jobs', 'pixar', {'verb': 'replaced'}),
	 ('jobs', 'pixar', {'verb': 'announced'}),
	 ('jobs', 'pixar', {'verb': 'described'}),
	 ('jobs', 'pixar', {'verb': 'revealed'}),
	 ('jobs', 'pixar', {'verb': 'pixar'}),
	 ('jobs', 'pixar', {'verb': 'visionary'}),
	 ('jobs', 'pixar', {'verb': 'dedicated'})]
</pre>

=====

1. relationship between e1:barack obama,e2: united states

<pre>
	[('barack', 'united', {'verb': 'president'}),
	 ('obama', 'states', {'verb': 'ties'}),
	 ('obama', 'united', {'verb': 'received'}),
	 ('obama', 'united', {'verb': 'announced'}),
	 ('obama', 'united', {'verb': 'state'}),
	 ('obama', 'united', {'verb': 'established'}),
	 ('obama', 'united', {'verb': 'pass'}),
	 ('obama', 'united', {'verb': 'called'}),
	 ('obama', 'united', {'verb': 'delivered'}),
	 ('obama', 'united', {'verb': 'announced'}),
	 ('obama', 'united', {'verb': 'said'}),
	 ('obama', 'united', {'verb': 'authorized'}),
	 ('obama', 'united', {'verb': 'rejected'}),
	 ('obama', 'united', {'verb': '25'}),
	 ('obama', 'united', {'verb': 'may'}),
	 ('obama', 'united', {'verb': '2011'})]
</pre>


=====

## indirect relations

1. relationship between e1:mona lisa and e2:Renaissance
    
	* The em here is **"leonardo da vinci"**
	 
	* relationship between e1,em:
	<pre>
		[('lisa', 'leonardo', {'verb': 'believed'}),
		 ('lisa', 'leonardo', {'verb': 'is'}),
		 ('lisa', 'leonardo', {'verb': 'states'}),
		 ('lisa', 'leonardo', {'verb': 'likens'}),
		 ('lisa', 'leonardo', {'verb': 'working'}),
		 ('mona', 'leonardo', {'verb': 'undertook'}),
		 ('mona', 'leonardo', {'verb': 'comes'}),
		 ('mona', 'leonardo', {'verb': 'began'}),
		 ('mona', 'leonardo', {'verb': 'arguable'}),
		 ('mona', 'leonardo', {'verb': 'fitted'}),
		 ('mona', 'leonardo', {'verb': 'lisa'}),
		 ('mona', 'leonardo', {'verb': 'is'}),
		 ('mona', 'leonardo', {'verb': 'study'})]
	</pre>

	* relationship between e2,em:
	<pre>
		[('leonardo', 'renaissance', {'verb': 'described'}),
		 ('leonardo', 'renaissance', {'verb': 'were'}),
		 ('leonardo', 'renaissance', {'verb': 'recognized'}),
		 ('da', 'renaissance', {'verb': 'painterslist'}),
		 ('da', 'renaissance', {'verb': 'memory'}),
		 ('da', 'renaissance', {'verb': 'vinci'}),
		 ('da', 'renaissance', {'verb': 'vinci'}),
		 ('da', 'renaissance', {'verb': 'airportlist'})]
	</pre>
	
=====
* hard sentences 
![](./data/hard_sentences_example.png)



=====
## problems so far
=====

* entity searching:
	* "leonardo da vinci": I can search for "leonardo",and "da vinci"
	* "data mining" I **cannot** search for "data" and " mining"
* ranking the results

=====
## related work for mining relationships from text
=====

* Yan Y, Okazaki N, Matsuo Y, et al. Unsupervised relation extraction by mining Wikipedia texts using information from the web[C]//Proceedings of the Joint Conference of the 47th Annual Meeting of the ACL and the 4th International Joint Conference on Natural Language Processing of the AFNLP: Volume 2-Volume 2. Association for Computational Linguistics, 2009: 1021-1029.

* Wang Y, Yang B, Qu L, et al. Harvesting facts from textual web sources by constrained label propagation[C]//Proceedings of the 20th ACM international conference on Information and knowledge management. ACM, 2011: 837-846.

* surface clustering for the dependencies 
![](./data/dependency_graph.png)

* relation cluster results in the above paper

![](./data/relation.png)


