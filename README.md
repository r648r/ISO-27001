# ISO-27001

## Qu’est ce qu’un SMSI ?

- **SMSI** : Système de management de la sécurité de l’information 
  - **Définition globale** : permettre le pilotage de la sécurité de l’information 
  - **Périmètre** : Délimite ce que l'on souhaite protéger
    - ( Sécu informatique, Supports papier, Locaux, information mémorisé ) ∈ Sécurité de l’information
  - **Menace** : Intérieur ou ext du périmètre
  - **Amélioration continue**
    - Améliorer les mesures lorsqu’elles ne sont plus adaptées
    - Ajouter de nouvelles
    - Corriger les défauts constatés
    - Tirer un maximum d’XP des incidents de sécurité -> améliorer les procédures -> alimenter l’analyse de risques
    - Réévaluer régulièrement le contexte de l’organisme
   
## Formalisation du contexte et des enjeux
Décrire les activités de l’entreprise, en posant la question de leur nature, de leur criticité, du contexte légal.
- Description des activités de l’entreprise
- Description des enjeux liés aux activités de l’entreprise
- Contexte géographique
- Matrice SWOT 
- Identification des parties prenantes (y compris des gouvernements qui peuvent demander à respecter des lois).

### Exemple de formalisation du contexte
- les clients directs revendent ou font profiter de toute ou d’une partie du service qu’ils achètent.
- Dans ce cas, les utilisateurs finaux sont également partie prenante du SI.

#### Description des activités

- La société X a pour principale activité, l’hébergement de données sur le territoire Européen, et en particulier de données de santé. L’hébergement de ces dernières nécessite une certification HDS (Hébergeur de données de santé) lorsque celles-ci appartiennent à des citoyens français.

- La société X est consciente que ces données représentent une forte valeur marchande pour des cybercriminels et qu’en cas de compromission l’impact sur la vie des patients auxquels elles appartiennent serait majeur.

- La société X a décidé de formuler des objectifs de sécurité adaptés aux besoins en matière de disponibilité, d’intégrité, de confidentialité, et de traçabilité des données qu’elle est amenée à héberger pour tous ses clients. 

#### Parties prenantes

**PP - Internes**

- La direction, les métiers, les administrateurs SI, ainsi que tous les collaborateurs utilisant le SI sont des parties prenantes. Le SI doit tenir compte des besoins de sécurité des données leur appartenant, notamment des données relatives à leur identité, et des données à caractère personnelle les concernant.

**PP - Clients et utilisateurs finaux des services**

- Les clients confient des données pour hébergement sur les infrastructures de la société X. Toutes les données ne leur appartiennent pas nécessairement : elles peuvent être la propriété des utilisateurs finaux des services hébergés sur les infrastructures de la société X. Dans le cas particulier des données de santé, les patients en sont les propriétaires.

- Les clients et utilisateurs finaux attentent du SI, qu’il garantisse la disponibilité des données, leur intégrité et leur confidentialité.

- La liste complète des clients est accessible dans l’ERP de l’entreprise. La liste des utilisateurs finaux des services des clients est maintenue par les clients sous leur responsabilité contractuelle.

**PP - Autorités et législatives**

- Dans le cadre de l’hébergement de données à caractère personnel de citoyens européens, l’UE impose la conformité au RGPD et de garantir que les droits des citoyens afférents soient respectés. La CNIL est l’autorité de contrôle pour le territoire Français.

- Dans le cadre de l’hébergement de données de santé, l’Etat français demande la certification HDS, nécessitant elle-même la conformité à la norme ISO 27001.

- L’ANSSI est l’autorité de contrôle pour HDS.

**PP – Prestataires et fournisseurs critiques**

Les prestataires et fournisseurs suivants ont été identifiés comme critiques :

 - Société ABC : fournisseur principal de nos liens réseaux

 - Société DFG : fournisseur de nos liens réseaux de secours

 - Société HIJ : Administrateur de la solution de sécurité Y

Les prestataires ont imposé contractuellement le fait que les informations d’identification pour accéder à leurs portails et services sont sous la responsabilité de la société X.

Du fait de la forte interconnexion de nos systèmes avec ceux de la société HIJ, la société HIJ a fourni une liste d’exigences de sécurité consignées dans le document « PAS HIJ ».
Implémentation géographique

#### Sites géographiques
- Clinique Siège principal
    Localisation : Périphérie d’une ville côtière (zone inondable).
    Contexte : Proche de zones résidentielles et d’une zone portuaire.
- Clinique Montagne
    Localisation : Ville alpine isolée, en bordure d’une station de ski.
    Contexte : Conditions climatiques hivernales rigoureuses, forte fréquentation saisonnière.
- Clinique Métropole
    Localisation : Centre-ville d’une grande métropole.
    Contexte : Zone urbaine dense, forte compétition entre établissements médicaux.

### BIG 4

**Disponibilité**  
Nous ne pouvons pas accéder à vos résultats d'analyse pour le moment, car les serveurs sont temporairement indisponibles.

**Intégrité**  
Une incohérence a été détectée dans vos antécédents médicaux : un traitement incorrect a été ajouté par erreur.

**Confidentialité**  
Votre diagnostic a été accidentellement envoyé à une mauvaise adresse email. Nous enquêtons pour éviter que cela ne se reproduise.

**Traçabilité**  
Les journaux indiquent que l'erreur a été commise par l'infirmière Clara Dupont le 12 décembre à 14h05.

## Perimetre
le périmètre de votre SMSI doit figurer sur votre certificat ISO 27001 !

| Type de périmètre         | Avantages                                                                                       | Inconvénients                                                                            |
|---------------------------|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| **Périmètre global**      | Sécurité uniforme (nivellement par le haut). Moins d'interfaces à gérer.                        | La perte de certification impacte tout le périmètre.                                     |
| **Périmètre restreint**   | Moins coûteux. La perte de certification n'affecte que le périmètre concerné.                   | Différences de sécurité avec ce qui est hors périmètre. Nécessite des contrôles sur les interfaces.  |
| **Périmètre très restreint** | Interfaces critiques réduites (autres périmètres certifiés). Adapté à des contextes spécifiques. | Plus coûteux : chaque périmètre nécessite un audit indépendant.                      |

## PSSI (Politique de sécurité du système d'information)

De nombreux objectifs sont formulés de telle sorte qu’ils ne motivent pas d’effort, ou ne sont jamais atteints.

### Exemple
Ils faut au **spliter en s-partie** des titres généraux : 
1. Garantir la disponibilité, l’intégrité, la confidentialité et la traçabilité des données »
2. Garantir la disponibilité de nos services » **est un objectif non SMART mais qui peut être découpé :**
    - Maintenir la disponibilité du site web à 99% (mesure mensuelle)
    - Maintenir la disponibilité du support client en heure ouvrée à 98% (mesure hebdomadaire)
    - Maintenir la disponibilité des infrastructures informatiques à 99,9% hors période de maintenance, et à 99% en période de maintenance (mesure trimestrielle).


## Conduire une analyse de risques

Méthodologie existante (ISO27005 ou EBIOS RM) ou custom
Généralité
- Doc ∈ SMSI
- Approuvé et validé par la direction
- Versionné
- Protégé
Methodo
méthodologie choisie doit respecter les éléments suivants (Chapitre 6 de la norme ISO27001) :
  1. EBIOS RM :
      - Cadre de sécurité et périmètre d’étude : Identification du contexte et des objectifs.
      - Sources de risques : Identification des menaces et des acteurs menaçants.
      - Scénarios stratégiques : Élaboration d’hypothèses globales permettant d’identifier les impacts majeurs sur les objectifs organisationnels, notamment en termes de gouvernance, de réputation, et de continuité d’activité. 
      - Scénarios opérationnels : Exploration approfondie des mécanismes techniques et des processus spécifiques impliqués dans les risques, mettant en évidence les vulnérabilités et les conséquences pratiques à un niveau opérationnel.
      - Traitement des risques : Identification et priorisation des mesures de sécurité.
      Méthode collaborative et interactive (et Francaise).
   [FAQ EBIOS RM](https://club-ebios.org/site/faq/)

  
  2. ISO 27005 :
      - Contexte de gestion des risques.
      - Identification des risques.
      - Analyse des risques.
      - Évaluation des risques.
      - Traitement des risques.
      Approche générique, laissant libre l'utilisation d'autres outils ou techniques pour chaque étape (ex. : OCTAVE, FAIR).
















