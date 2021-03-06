---
title: Index de service, NuGet API
description: L’index de service est le point d’entrée de l’API HTTP de NuGet et énumère les fonctionnalités du serveur.
author: joelverhagen
ms.author: jver
manager: skofman
ms.date: 10/26/2017
ms.topic: reference
ms.reviewer: kraigb
ms.openlocfilehash: 84e623e8480e4d17edad2ec3b2da6dcb6e53d21b
ms.sourcegitcommit: 3eab9c4dd41ea7ccd2c28bb5ab16f6fbbec13708
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
ms.locfileid: "31822092"
---
# <a name="service-index"></a>Index de service

L’index de service est un document JSON qui est le point d’entrée pour une source de package NuGet et permet une implémentation de client découvrir les fonctionnalités de la source du package. L’index de service est un objet JSON avec deux propriétés obligatoires : `version` (la version du schéma de l’index de service) et `resources` (les points de terminaison ou les fonctions de la source du package).

index de service NuGet.org se trouve dans `https://api.nuget.org/v3/index.json`.

## <a name="versioning"></a>Gestion de version

Le `version` valeur est une chaîne de version analysables SemVer 2.0.0 qui indique la version du schéma de l’index de service. L’API exige qu’un numéro de version principale de la chaîne de version `3`. Comme les modifications sans rupture sont apportées au schéma d’index de service, version mineure de la chaîne version augmente.

Chaque ressource dans l’index de service est créée indépendamment de la version de schéma d’index service.

La version de schéma actuelle est `3.0.0`. Le `3.0.0` version est fonctionnellement équivalente à l’ancien `3.0.0-beta.1` version mais doit être préféré car il communique plus clairement le schéma stable, défini.

## <a name="http-methods"></a>Méthodes HTTP

L’index de service est accessible à l’aide des méthodes HTTP `GET` et `HEAD`.

## <a name="resources"></a>Ressources

Le `resources` propriété contient un tableau de ressources pris en charge par cette source de package.

### <a name="resource"></a>Ressource

Une ressource est un objet dans le `resources` tableau. Il représente une fonctionnalité avec version de la source de package. Une ressource a les propriétés suivantes :

Name          | Type   | Obligatoire | Notes
------------- | ------ | -------- | -----
@id           | chaîne | oui      | L’URL de la ressource
@type         | chaîne | oui      | Une constante de chaîne qui représente le type de ressource
commentaire       | chaîne | Non       | Description explicite de la ressource

Le `@id` est une URL qui doit être absolu et doit avoir le schéma HTTP ou HTTPS.

Le `@type` est utilisé pour identifier le protocole à utiliser lors de l’interaction avec les ressources. Le type de la ressource est une chaîne opaque, mais généralement a le format :

    {RESOURCE_NAME}/{RESOURCE_VERSION}

Les clients doivent coder en dur le `@type` valeurs comprendre et de les rechercher dans l’index de service d’une source de package. Le texte exact `@type` utilisés aujourd'hui, les valeurs sont énumérées dans les documents de référence de ressource individuelle répertoriés dans le [présentation de l’API](overview.md#resources-and-schema).

Pour des raisons de cette documentation, la documentation sur les différentes ressources est essentiellement groupée par le `{RESOURCE_NAME}` trouvés dans l’index de service qui est analogue à un regroupement par scénario. 

Il est inutile que chaque ressource a une valeur unique `@id` ou `@type`. C’est à l’implémentation du client pour déterminer quelle ressource préférez un autre. Une implémentation possible est que les ressources d’identiques ou compatibles `@type` peut être utilisé de manière alternée en cas d’erreur de serveur ou d’échec de connexion.

### <a name="sample-request"></a>Exemple de demande

TÉLÉCHARGER https://api.nuget.org/v3/index.json

### <a name="sample-response"></a>Exemple de réponse

[!code-JSON [service-index.json](./_data/service-index.json)]
