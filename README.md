# Ressources pour PHY3051/PHY6051

Voici une liste non exhaustive de ressources utiles pour les sujets abordés dans le cours PHY3051.

Les liens sont divisés par sujet.
Ils peuvent inclure des _packages_ Python, des livres, des articles et toute autre ressource utile pour l'utilisation ou l'approfondissement des concepts couverts dans le cours.

N'hésitez pas à ajouter des ressources! Pour le faire, suivez les instructions [ici](AJOUTS.md).

<!-- toc -->

- [Inférence bayésienne](#inference-bayesienne)
  * [Markov Chain Monte-Carlo (MCMC)](#markov-chain-monte-carlo-mcmc)
  * [Nested sampling](#nested-sampling)
  * [Programmation probabiliste](#programmation-probabiliste)
- [Machine Learning](#machine-learning)
  * [Processus gaussiens (GPs)](#processus-gaussiens-gps)
  * [Deep learning](#deep-learning)
  * [Librairies de calcul sur tenseur](#librairies-de-calcul-sur-tenseur)
  * [Réseaux neuronaux artificiels](#reseaux-neuronaux-artificiels)
- [Applications](#applications)
  * [Astronomie](#astronomie)
  * [Physique des particules](#physique-des-particules)
  * [Physique des plamsa](#physique-des-plamsa)
  * [Biophysique](#biophysique)
  * [Physique des matériaux](#physique-des-materiaux)
- [Outils de développement logiciel](#outils-de-developpement-logiciel)
  * [Git](#git)
  * [Environnement Python](#environnement-python)
  * [Environnements de développements (IDEs) et éditeurs de texte](#environnements-de-developpements-ides-et-editeurs-de-texte)
  * [Autre](#autre)

<!-- tocstop -->

## Inférence bayésienne

### Markov Chain Monte-Carlo (MCMC)

- [Data Analyses Recipes: Using MCMC](https://ui.adsabs.harvard.edu/abs/2018ApJS..236...11H/abstract) - Article qui donne une introduction au MCMC, par les auteurs d'[emcee](https://emcee.readthedocs.io/en/stable/)
- [emcee](https://emcee.readthedocs.io/en/stable/) - _Package_ Python pour les MCMCs par ensemble.
- [ptemcee](https://github.com/willvousden/ptemcee) - Similaire à _emcee_, mais avec _Parallel-tempering_. Ne semble plus développé activement mais très utilisé et peu servir de référence.
- [zeus](https://zeus-mcmc.readthedocs.io/en/latest/) - _Package_ Python qui
  implémente la méthode MCMC d'_ensemble slice sampling_ (très récent en date d'avril 2022)
  [Blackjax](https://blackjax-devs.github.io/blackjax/) - MCMC et HMC avec JAX
- Voir aussi [la section sur la programmation probabiliste](#programmation-probabiliste)

### Nested sampling

- [dynesty](https://dynesty.readthedocs.io/en/stable/) - _Nested sampling_ dynamique et static avec Python. Interface très similaire à _emcee_.
- [UltraNest](https://johannesbuchner.github.io/UltraNest/index.html) - _Nested
  sampling_ avec Python, « sans configuration à ajuster et avec justification théorique ». Peut servir d'alternative à [dynesty](https://dynesty.readthedocs.io/en/stable/).
- [MultiNest](https://github.com/farhanferoz/MultiNest) - _Nested sampling_ en Fortran.
- [PyMultiNest](https://johannesbuchner.github.io/PyMultiNest/) - Interface Python pour [MultiNest](https://github.com/farhanferoz/MultiNest).

### Programmation probabiliste

Les libraires de programmation probabiliste implémentent les structures de base
pour l'inférence bayésienne et des algorithmes d'échantillonage (MCMC, _Hamiltonian Monte Carlo_, _No U-Turn Sampling_).

- [NumPyro](https://num.pyro.ai/en/latest/index.html#introductory-tutorials) - Version de [Pyro](https://pyro.ai/) basée sur Jax (interface similaire à NumPy)
- [PyMC](https://docs.pymc.io) - Modèles bayésiens, HMC, NUTS, GPs. Basé sur PyTensor
- [Stan](https://mc-stan.org/) - Plateforme crée spécifiquement pour l'inférence bayésienne et la modélisation statistique.. Interfaces en Python, R, Julia et autres languages.
- [Pyro](https://pyro.ai/) - Inférence bayésienne (MCMC, NUTS, Nested sampling) et _machine learning_ probabiliste avec PyTorch.

## Machine Learning

- [Probabilistic Machline Learning](https://probml.github.io/pml-book/) - Série de livres par Kevin Murphy sur le deep learning, avec une approche probabiliste. Les livres 1 (intro) et 2 (avancé) sont plus récents et approfondissent plus de sujets.
- [scikit-learn](https://scikit-learn.org/stable/) - _Package_ Python pour le _machine learning_

### Processus gaussiens (GPs)

- [Gaussian Processes for Machine Learning](http://gaussianprocess.org/gpml/) - Principal livre sur les GPs
- [A Visual Exploration of GPs](https://distill.pub/2019/visual-exploration-gaussian-processes/) - Blog qui explique les GPs et qui contient des outils de visualisation (matrice de covariances et exemples de fonctions).
- [scikit-learn](https://scikit-learn.org/stable/modules/gaussian_process.html) - Tutoriel sur les GPs avec [scikit-learn](https://scikit-learn.org/stable/)
- [George](https://george.readthedocs.io/en/latest/) - _Package_ Python simple pour les GPs (en mode « maintenance », voir [tinygp](https://tinygp.readthedocs.io/en/stable/) pour alternative plus récente du même auteur)
- [tinygp](https://tinygp.readthedocs.io/en/stable/) - _Package_ Python similaire à [George](https://george.readthedocs.io/en/latest/), mais avec Jax et activement développé.
- [celerite](https://celerite.readthedocs.io/en/stable/) - _Package_ Python similaire à [George](https://george.readthedocs.io/en/latest/), mais qui restreint les _kernels_ à une classe spécifique qui permettent des calculs plus rapide. Utile pour les signaux quasi-périodiques. (en mode « maintenance »)
- [celerite2](https://celerite2.readthedocs.io/en/latest/) - Version 2 de [celerite](https://celerite.readthedocs.io/en/stable/), fonctionne Python, C++, Theano et Jax.
- [GPyTorch](https://gpytorch.ai/) - _Package_ Python qui implémente des GPs
  avec PyTorch


### Deep learning

- [Deep Learning](https://www.deeplearningbook.org/) - Livre par Ian Goodfellow,Yoshua Bengio et Aaron Courville sur le _Deep Learning_. Très bonne introduction théorique.


### Librairies de calcul sur tenseur

Libraires qui implémentent des calculs similaires à NumPy, mais optimisées pour GPU et pour l'autodérivation (_autodiff_).

- [PyTorch](https://pytorch.org/) - Librairie Python de _Deep learning_ développée par Facebook.
- [Tensorflow](https://www.tensorflow.org/) - Librairie Python de _Deep learning_ développée par Google.
- [Jax](https://jax.readthedocs.io/en/latest/) - Plus récent, interface similaire à NumPy, implémente autodiff, compilation Just-In-Time (JIT) sur GPU. Aussi de Google.
- [PyTensor](https://pytensor.readthedocs.io/en/latest/) - Librairie Python qui implémente l'autodérivation et la compilation vers C, Jax, Numba. Utilisée principalement avec PyMC.

### Réseaux neuronaux artificiels

- [PyTorch](https://pytorch.org/) et [Tensorflow](https://www.tensorflow.org/) permettent de définir des réseaux de neurones avec beaucoup de flexibilité.
- [Keras](https://keras.io/) - Interface Python qui utilise Tensorflow pour définir rapidement des modèles, les entrainer et les utiliser.
- [Equinox](https://docs.kidger.site/equinox/): réseaux neuronaux avec JAX
- [Flax](https://flax.readthedocs.io/en/latest/): réseaux neuronaux avec JAX

## Applications

Les sections suivantes incluent des ressources spécifiques à différents domaines
de la physique. La plupart utilisent d'autres ressources mentionnées ci-dessus.

### Astronomie

- [exoplanet](https://docs.exoplanet.codes/en/latest/) - Modélisation probabiliste d'orbite d'exoplanètes avec PyMC
- [jaxoplanet](https://jax.exoplanet.codes/en/latest/) - Comme `exoplanet`, mais avec JAX
- [RadVel](https://radvel.readthedocs.io/en/latest/) - _Package_ Python pour modéliser les séries de vitesse radiale pour la détection d'exoplanète. Inclue des modèles et _priors_ pré-définis, des GPs et un MCMC.
- [orbitize!](https://orbitize.readthedocs.io/en/latest/) - _Package_ Python pour modéliser l'astrométrie relative (imagerie directe) d'exoplanètes. Interface similaire à RadVel.
- [batman](https://lweb.cfa.harvard.edu/~lkreidberg/batman/) - _Package_ Python pour modéliser les transits d'exoplanètes.
- [Astropy](https://www.astropy.org/) - Plein de fonctions et _packages_ utiles pour l'astronomie avec Python
- [petitRADTRANS](https://petitradtrans.readthedocs.io/en/latest/): spectres d'exoplanètes
- [exojax](https://secondearths.sakura.ne.jp/exojax/): spectres d'exoplanètes avec JAX

### Physique des particules

N'hésitez pas à [inclure](AJOUTS.md) des ressources liées au cours et à ce sujet!

### Physique des plamsa

N'hésitez pas à [inclure](AJOUTS.md) des ressources liées au cours et à ce sujet!

### Biophysique

N'hésitez pas à [inclure](AJOUTS.md) des ressources liées au cours et à ce sujet!

### Physique des matériaux

N'hésitez pas à [inclure](AJOUTS.md) des ressources liées au cours et à ce sujet!

## Outils de développement logiciel

Ces outils ne sont pas directement liés au cours, mais sont utiles pour l'analyse de données et la programmation.

### Git

- [Git](https://git-scm.com/) (Voir aussi le [Guide Git de GitHub](https://github.com/git-guides/)) - Pour versionner votre code localement
- [Github](https://github.com/) - Pour sauvegarder votre code en ligne et y accéder sur différents ordinateurs
- [GitKraken](https://www.gitkraken.com/) - Interface graphique pour Git
- [Github Desktop](https://desktop.github.com/) - Interface Graphique pour Git (Windows et MacOS seulement)
- [Template gitignore pour Python](https://github.com/github/gitignore/blob/main/Python.gitignore)

### Environnement Python

- [Miniconda](https://docs.conda.io/projects/miniconda/en/latest/) - Installe le minimum requis pour utiliser conda. Permet d'avoir plusieurs versions de Python et de créer des environnements virtuels.
- [Anaconda](https://www.anaconda.com/download/) - Distribution Conda qui inclut un environnement complet (très volumineux)
- [venv](https://docs.python.org/3/library/venv.html) - Pour créer des environnements virutels avec Python sans Conda
- [virtualenv](https://virtualenv.pypa.io/en/latest/)- Comme `venv`, mais avec un peu plus de fonctionnalités
- [pyenv](https://github.com/pyenv/pyenv) - Alternative à Conda pour utiliser différentes version de Python (bug un peu plus avec certains _packages_ scientifiques dans  mon expérience)

### Environnements de développements (IDEs) et éditeurs de texte

- [Visual Studio Code](https://code.visualstudio.com/) - Éditeur de texte/IDE qui supporte bien Python et les notebooks Jupyter
- [PyCharm](https://www.jetbrains.com/pycharm/) - IDE pour Python et notebooks Jupyter (version pro gratuite avec votre courriel UdeM)
- [Spyder](https://www.spyder-ide.org/) - IDE pour la programmation scientifique en Python
- [JupyterLab](https://jupyter.org/) - Environnement pour les notebooks Jupyter qui inclut aussi un éditeur de texte, terminal, etc.

### Autre

- [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/): Environnement Linux dans le terminal Windows
