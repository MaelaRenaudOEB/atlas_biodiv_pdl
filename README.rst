
Plateforme de visualisation des données naturalistes des Pays de la Loire, basée sur GeoNature-atlas
===============

Projet de plateforme web permettant de visualiser les données "biodiversité" du réseau naturaliste des Pays de la Loire. 


Bases de développement
------------


Cette plateforme est développée à partir des outils de gestion de données naturalistes (voir `GeoNature <http://geonature.fr>`_) développés par le Parc National des Ecrins et le Parc national des Cévennes :

- la structure de base de données de `GeoNature <https://github.com/PnEcrins/GeoNature>`_ ;
- l'outil complet `UsersHub <https://github.com/PnEcrins/UsersHub>`_ ;
- l'outil complet `TaxHub <https://github.com/PnX-SI/TaxHub>`_ ;
- l'outil complet `Geonature-atlas <https://github.com/PnEcrins/GeoNature-atlas>`_ modifié pour les besoins du CEN Pays de la Loire.

La plateforme est développée sur un serveur Ubuntu 16.04 (`fichiers d'installation <https://github.com/Splendens/install_all_geonature_ubuntu16_04>`_)




La plateforme Biodiversité - Pays de la Loire
------------

La plateforme de visusalistion est basée sur `Geonature-atlas <https://github.com/PnEcrins/GeoNature-atlas>`_, en cours de modification pour permettre : 

- le moissonnage des données naturalistes dégradées (= non précises) des bases de données des partenaires naturalistes ;
- l'affichage des données par mailles, communes et intercommunalités ;
- l'affichage de graphes de synthèses sur les territoires (statistiques par groupes, statistiques par statuts...).



Modifications en cours
------------

**Bases de données**

- Ajout de vues matérialisées à la DB geonatureatlas pour l'affichage par communes, intercommunalités, départements


**Application**

- Ajout des fonctionnalités de visualisation des données par communes, intercommunalités et département 
- Ajout des fonctionnalités de visualisation des données par mailles utm
- Ajout des fonctionnalités de visualisation de graphes de statistiques sur les territoires
- Cartographie globale du territoire avec des filtres



Modifications apportées
------------

**Bases de données**

- `Modification des zonages <https://github.com/Splendens/atlas_biodiv_pdl/blob/master/modifdb/couches_reference.rst>`_ (territoire, communes) pour les Pays de la Loire
- Ajout des structures productrices des données affichées (modifications de la vm_observations)
- Ajout d'un schéma par base de données partenaires moissonnées à la DB geonatureatlas 
- Récupération des données des DB externes (via FDW)
- Modifications de la récupération des mailles (données dégradées aux centroïdes des mailles)

**Application**

- Modification de la page d'accueil 
- Affichage des structures productrices des données affichées (modifications des entités, modèles et vues des fiches espèces, fiches groupes, rang taxonomique et fiches communes)
- Ajout de la `génération générique de pages d'informations <https://github.com/PnEcrins/GeoNature-atlas/issues/131>`_  + création de pages "partenaires", "collectivtés", "particuliers"
- Ajout de bouttons vers les pages dédiées aux utilisateurs à côté des cartographies (informations pour fournir ou récupérer des données) 

