# Ressources pour PHY3051/PHY6051

Les liens sont divisés par sujet. Ils peuvent inclure des _packages_ Python, des
livres, des articles et toute autre ressource utile pour l'utilisation ou
l'approfondissement des concepts couverts dans le cours.

Pour ajouter une ressource, suivez les instructions [ici](AJOUTS.md).

## Concepts d'analyse bayésienne

- [scikit-learn](https://scikit-learn.org/stable/) - _Package_ Python,
  implémentation de plusieurs fonctionalités utiles en opur l'analyse bayésienne
  et le _machine learning_
- [_Frequentism and Bayesianism: What's the Big Deal_](https://www.youtube.com/watch?v=KhAUfqhLakw) - Présentation par Jake VanderPlas sur les différences entre les méthodes fréquentiste et bayésienne

## Processus gaussiens (GPs)

- [Gaussian Processes for Machine Learning](http://gaussianprocess.org/gpml/) - Principal livre sur les GPs
- [A Visual Exploration of GPs](https://distill.pub/2019/visual-exploration-gaussian-processes/) - Blog qui explique les GPs et qui contient des outils de visualisation (matrice de covariances et exemples de fonctions).
- [scikit-learn](https://scikit-learn.org/stable/modules/gaussian_process.html) - Tutoriel sur les GPs avec [scikit-learn](https://scikit-learn.org/stable/)
- [George](https://george.readthedocs.io/en/latest/) - _Package_ Python simple pour les GPs (en mode « maintenance », voir [tinygp](https://tinygp.readthedocs.io/en/stable/) pour alternative plus récente du même auteur)
- [tinygp](https://tinygp.readthedocs.io/en/stable/) - _Package_ Python similaire à [George](https://george.readthedocs.io/en/latest/), mais avec Jax et activement développé.
- [celerite](https://celerite.readthedocs.io/en/stable/) - _Package_ Python similaire à [George](https://george.readthedocs.io/en/latest/), mais qui restreint les _kernels_ à une classe spécifique qui permettent des calculs plus rapide. Utile pour les signaux quasi-périodiques. (en mode « maintenance »)
- [celerite2](https://celerite2.readthedocs.io/en/latest/) - Version 2 de [celerite](https://celerite.readthedocs.io/en/stable/), fonctionne Python, C++, Theano et Jax.
- [GPyTorch](https://gpytorch.ai/) - _Package_ Python qui implémente des GPs
  avec PyTorch

## Markov Chain Monte-Carlo (MCMC)

- [Data Analyses Recipes: Using MCMC](https://ui.adsabs.harvard.edu/abs/2018ApJS..236...11H/abstract) - Article qui donne une introduction au MCMC, par les auteurs d'[emcee](https://emcee.readthedocs.io/en/stable/)
- [emcee](https://emcee.readthedocs.io/en/stable/) - _Package_ Python pour les MCMCs par ensemble.
- [ptemcee](https://github.com/willvousden/ptemcee) - Similaire à _emcee_, mais avec _Parallel-tempering_. Ne semble plus développé activement mais très utilisé et peu servir de référence.
- [zeus](https://zeus-mcmc.readthedocs.io/en/latest/) - _Package_ Python qui
  implémente la méthode MCMC d'_ensemble slice sampling_ (très récent en date d'avril 2022)

## Nested sampling

- [dynesty](https://dynesty.readthedocs.io/en/stable/) - _Nested sampling_ dynamique et static avec Python. Interface très similaire à _emcee_.
- [UltraNest](https://johannesbuchner.github.io/UltraNest/index.html) - _Nested
  sampling_ avec Python, « sans configuration à ajuster et avec justification théorique ». Peut servir d'alternative à [dynesty](https://dynesty.readthedocs.io/en/stable/).
- [MultiNest](https://github.com/farhanferoz/MultiNest) - _Nested sampling_ en Fortran.
- [PyMultiNest](https://johannesbuchner.github.io/PyMultiNest/) - Interface Python pour [MultiNest](https://github.com/farhanferoz/MultiNest).

## Deep learning

- [Deep Learning](https://www.deeplearningbook.org/) - Livre par Ian Goodfellow,Yoshua Bengio et Aaron Courville sur le _Deep Learning_. Très bonne introduction théorique.
- [Probabilistic Machline Learning](https://probml.github.io/pml-book/) - Série de livres par Kevin Murphy sur le deep learning, avec une approche probabiliste. Les livres 1 (intro) et 2 (avancé) sont plus récents et approfondissent plus de sujets.

### Librairies de calcul sur tenseur

Libraires qui implémentent des calculs similaires à NumPy, mais optimisées pour
GPU et pour l'autodérivation (_autodiff_).

- [PyTorch](https://pytorch.org/) - Librairie Python de _Deep learning_ développée par Facebook.
- [Tensorflow](https://www.tensorflow.org/) - Librairie Python de _Deep learning_ développée par Google.
- [Jax](https://jax.readthedocs.io/en/latest/) - Plus récent, interface similaire à NumPy, implémente autodiff, compilation Just-In-Time (JIT) sur GPU.
- [Aesara](https://aesara.readthedocs.io/en/latest/) (anciennement [Theano](https://theano-pymc.readthedocs.io/en/latest/)) - Librairie Python qui implémente l'autodérivation et la compilation vers C, Jax, Numba. Utilisée principalement avec PyMC3.

### Réseaux de neurone artificiels
- [PyTorch](https://pytorch.org/) et [Tensorflow](https://www.tensorflow.org/) permettent de définir des réseaux de neurones avec beaucoup de flexibilité.
- [Keras](https://keras.io/) - Interface Python qui utilise Tensorflow pour
  définir rapidement des modèles, les entrainer et les utiliser.

## Programmation probabiliste

Les libraires de programmation probabiliste implémentent les structures de base
pour l'inférence bayésienne et des algorithmes d'échantillonage (MCMC, _Hamiltonian Monte Carlo_, _No U-Turn Sampling_).

- [PyMC3](https://docs.pymc.io/en/v3/) - Modèles bayésiens, HMC, NUTS, GPs. Basé sur Theano.
- [Pyro](https://pyro.ai/) - Inférence bayésienne (MCMC, NUTS, Nested sampling) et _machine learning_ probabiliste avec PyTorch.
- [NumPyro](https://num.pyro.ai/en/latest/index.html#introductory-tutorials) - Version de [Pyro](https://pyro.ai/) basée sur Jax (interface similaire à NumPy)
- [Stan](https://mc-stan.org/) - Plateforme crée spécifiquement pour l'inférence bayésienne et la modélisation statistique.. Interfaces en Python, R, Julia et autres languages.

## Applications

Les sections suivantes incluent des ressources spécifiques à différents domaines
de la physique. La plupart utilisent d'autres ressources mentionnées ci-dessus.

### Astronomie

- [celerite](https://celerite.readthedocs.io/en/stable/) et [celerite2](https://celerite2.readthedocs.io/en/latest/) (voir [Processus Gaussiens (GPs)](#processus-gaussiens-(gps))) - Très utilisé pour modélisé la variation quasi-périodique de lumière dans certaines étoiles.
- [exoplanet](https://docs.exoplanet.codes/en/latest/) - Modélisation probabiliste d'orbite d'exoplanètes avec PyMC3
- [RadVel](https://radvel.readthedocs.io/en/latest/) - _Package_ Python pour modéliser les séries de vitesse radiale pour la détection d'exoplanète. Inclue des modèles et _priors_ pré-définis, des GPs et un MCMC.
- [orbitize!](https://orbitize.readthedocs.io/en/latest/) - _Package_ Python pour modéliser l'astrométrie relative (imagerie directe) d'exoplanètes. Interface similaire à RadVel.
- [batman](https://lweb.cfa.harvard.edu/~lkreidberg/batman/) - _Package_ Python pour modéliser les transits d'exoplanètes.

### Physique des particules

N'hésitez pas à inclure des ressources liées au cours et à ce sujet!

### Physique des plamsa

N'hésitez pas à inclure des ressources liées au cours et à ce sujet!
