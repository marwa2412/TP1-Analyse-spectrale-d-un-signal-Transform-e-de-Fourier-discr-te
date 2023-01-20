# TP1: Analyse spectrale d'un signal & Transformée de Fourier discrète
## Objectifs 
	1. Représentation de signaux et applications de la transformée de Fourier discrète
	(TFD) sous Matlab. 
	2. Evaluation de l’intérêt du passage du domaine temporel au domaine fréquentiel 
	dans l’analyse et l’interprétation des signaux physiques réels.
	
## Introduction
	L'analyse spectrale d'un signal consiste à étudier la répartition de l'énergie du signal dans le domaine fréquentiel. La Transformée de Fourier Discrète
	(DFT) est l'outil mathématique utilisé pour effectuer cette analyse. La DFT transforme un signal temporel en un signal fréquentiel en utilisant une série 
	de coefficients de Fourier. Les coefficients de la DFT peuvent être utilisés pour calculer la fréquence dominante d'un signal, et pour identifier les 	
	composantes fréquentielles d'un signal.

## Réalisation du TP
	 - Partie 1 : Représentation temporelle et fréquentielle
		1.Traçage de x(t)
		<img width="798" alt="signal temporel" src="https://user-images.githubusercontent.com/86896531/213705295-92fcd3df-2d18-4291-8dec-03a2ca78fee0.png">

		2.Commande fft
		<img width="797" alt="signal fréquentiel" src="https://user-images.githubusercontent.com/86896531/213705376-5c858521-8a85-498e-a84a69e2957db82.png">
		
			•On a défini un vecteur de fréquence f, de N point et de pas df=fe/N (fréquence d’échantillonnage) .
			•La commande fft donne la représentation du signal dans le domaine fréquentiel.
			•Les raies des spectres obtenus sont symétriques par rapport à fe/2 (symétrie conjuguée).
			•L’utilisation de abs permet de tracer le spectre d’amplitude non exactes.
			•La division par N et la multiplication par 2 permet d’obtenir les valeurs exactes des amplitudes.
		3.Commande fftshift
		<img width="768" alt="fftshift" src="https://user-images.githubusercontent.com/86896531/213705544-4c9accdd-ff63-4cae-8bd6-a5c81b769b6d.png">

			•On cherche à avoir une symétrie par rapport à 0 donc on divise l’intervalle entre négatif et positif, on a l’intervalle fshift.
			•On trace donc avec la fonction fftshift qui effectue un décalage circulaire centré sur zéro du spectre en amplitude obtenu par la commande
			fft.
		4.Signal noise
		<img width="796" alt="noise (2)" src="https://user-images.githubusercontent.com/86896531/213705609-1fa84ab7-fd49-4bc2-be2f-cab4070cc6c9.png">
		
			•On crée un signal bruit blanc guassien à partir du signal x(t).
			•La fonction **randn** génère ce signal.
		5. Signal xnoise
		<img width="797" alt="xnoise" src="https://user-images.githubusercontent.com/86896531/213705669-8358c97c-dae9-495e-8ee9-9952647fc9a0.png">
		
			•On a combiné le signal x(t) avec le signal bruit, ce qui a donné le signal xnoise, puis on trace sa représentation dans le domaine 	
			fréquentiel 
			sous forme du signal ynoise .
		6.Sound
		<img width="193" alt="sound" src="https://user-images.githubusercontent.com/86896531/213705733-38181a15-6241-4261-8834-cbb35554c49a.png">

			•La commande sound, exécutée dans Command Window, pour écouter les deux signaux

	 - Partie 2 : Analyse fréquentielle du chant du rorqual bleu
	 
		<img width="740" alt="rorqual bleu" src="https://user-images.githubusercontent.com/86896531/213705791-48d23cb0-59c4-4313-961e-2b9d2493b34b.png">
		
			•On a d’abord récupéré les valeurs les valeurs et fréquences du signal et on a extrait un échantillon, stocké par la suite dans la variable
			chant. 
			•Ainsi on a pu tracer le signal dans le domaine temporel et puis dans le domaine fréquentiel grâce à la transformée de fourrier.	 

## Conclusions
