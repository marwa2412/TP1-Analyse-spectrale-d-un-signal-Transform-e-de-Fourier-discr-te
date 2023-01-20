# TP1: Analyse spectrale d'un signal & Transformée de Fourier discrète
## Objectifs 
	1. Représentation de signaux et applications de la transformée de Fourier discrète
	(TFD) sous Matlab. 
	2. Evaluation de l’intérêt du passage du domaine temporel au domaine fréquentiel 
	dans l’analyse et l’interprétation des signaux physiques réels.
	
## Introduction
	L'analyse spectrale d'un signal consiste à étudier la répartition de l'énergie du signal dans le domaine fréquentiel. La Transformée de Fourier Discrète 	 (DFT) est l'outil mathématique utilisé pour effectuer cette analyse. La DFT transforme un signal temporel en un signal fréquentiel en utilisant une série de 	      coefficients de Fourier. Les coefficients de la DFT peuvent être utilisés pour calculer la fréquence dominante d'un signal, et pour identifier les 		composantes fréquentielles d'un signal.

## Réalisation du TP
	 - Partie 1 : Représentation temporelle et fréquentielle
		1.Traçage de x(t)
		![image](https://user-images.githubusercontent.com/86896531/213668481-cc26b78b-9206-4f64-9a49-eaa6e29d2f7c.png)

		2.Commande fft
		![image](https://user-images.githubusercontent.com/86896531/213667507-f1dc3544-bdd2-42d0-ae73-c12601db41a7.png)
		
			•On a défini un vecteur de fréquence f, de N point et de pas df=fe/N (fréquence d’échantillonnage) .
			•La commande fft donne la représentation du signal dans le domaine fréquentiel.
			•Les raies des spectres obtenus sont symétriques par rapport à fe/2 (symétrie conjuguée).
			•L’utilisation de abs permet de tracer le spectre d’amplitude non exactes.
			•La division par N et la multiplication par 2 permet d’obtenir les valeurs exactes des amplitudes.
		3.Commande fftshift
		![image](https://user-images.githubusercontent.com/86896531/213667546-c3dd3478-e9a4-443c-8789-7c6d6b6ca6b5.png)
		
			•On cherche à avoir une symétrie par rapport à 0 donc on divise l’intervalle entre négatif et positif, on a l’intervalle fshift.
			•On trace donc avec la fonction fftshift qui effectue un décalage circulaire centré sur zéro du spectre en amplitude obtenu par la commande			    fft.
		4.Signal noise
		![image](https://user-images.githubusercontent.com/86896531/213667570-035e8a46-18a1-4317-b61c-59f281b7a9f1.png)

			•On crée un signal bruit blanc guassien à partir du signal x(t).
			•La fonction randn génère ce signal.
		5. Signal xnoise
		![image](https://user-images.githubusercontent.com/86896531/213667596-d693ccc6-bcfd-4a46-bebc-af5422301ee2.png)
		
			•On a combiné le signal x(t) avec le signal bruit, ce qui a donné le signal xnoise, puis on trace sa représentation dans le domaine 				 fréquentiel 
			sous forme du signal ynoise .
		6.Sound
		![image](https://user-images.githubusercontent.com/86896531/213667621-9843ca37-573a-4324-afb8-a61f28902af8.png)
		
			•La commande sound, exécutée dans Command Window, pour écouter les deux signaux

	 - Partie 2 : Analyse fréquentielle du chant du rorqual bleu
	![image](https://user-images.githubusercontent.com/86896531/213667656-54f90f87-f176-437b-9703-546be7183aa0.png)
	
			•On a d’abord récupéré les valeurs les valeurs et fréquences du signal et on a extrait un échantillon, stocké par la suite dans la variable 			     chant. 
			•Ainsi on a pu tracer le signal dans le domaine temporel et puis dans le domaine fréquentiel grâce à la transformée de fourrier.	 

## Conclusions
