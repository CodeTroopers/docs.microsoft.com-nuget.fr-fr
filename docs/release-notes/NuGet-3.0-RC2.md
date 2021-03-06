---
title: Notes de mise à jour de NuGet 3.0 RC2
description: Notes de version, y compris les problèmes connus, les correctifs de bogues, les fonctionnalités ajoutées et DCR de NuGet 3.0 RC2.
author: karann-msft
ms.author: karann
manager: unnir
ms.date: 11/11/2016
ms.topic: conceptual
ms.openlocfilehash: eb8b514fa967cc6ef850483b6b2a5df3ab27a550
ms.sourcegitcommit: 3eab9c4dd41ea7ccd2c28bb5ab16f6fbbec13708
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
ms.locfileid: "31819882"
---
# <a name="nuget-30-rc2-release-notes"></a>Notes de mise à jour de NuGet 3.0 RC2

[Notes de version RC de NuGet 3.0](../release-notes/nuget-3.0-RC.md) | [Notes de version de NuGet 3.0](../release-notes/nuget-3.0.0.md)

NuGet 3.0 RC2 3 juin 2015 a été publiée en tant qu’une version intermédiaire à partir de la galerie d’extensions Visual Studio 2015 et [Codeplex](https://nuget.codeplex.com/releases/view/615507). Cette version comporte un nombre importants de correctifs de bogues et des améliorations de performances, il nous semble ont été importantes de mise à jour avant la version de Visual Studio 2015 terminée. Cette version de l’extension NuGet est uniquement disponible pour Visual Studio 2015.

Au total, nous avons fermé 158 problèmes dans cette version, et vous pouvez passer en revue les [la liste complète des problèmes sur GitHub](https://github.com/NuGet/Home/issues?utf8=%E2%9C%93&q=is%3Aclosed+milestone%3A3.0.0-RTM+sort%3Aupdated-asc+updated%3A%3C%3D2015-06-01).

## <a name="summary-of-top-issues-resolved"></a>Résumé des principaux problèmes résolus

* [Mise à jour fréquentes réseau appelle au moment de l’actualisation de la fenêtre du Gestionnaire de package](https://github.com/NuGet/Home/issues/515)
* [Retardé de défilement lorsque la modification à installé vue dans le Gestionnaire de package](https://github.com/NuGet/Home/issues/519)
* [Les appels réseau doivent être exécutés sur un thread d’arrière-plan](https://github.com/NuGet/Home/issues/516)
* [Case à cocher « Ne pas afficher la fenêtre d’aperçu » ajouté](https://github.com/NuGet/Home/issues/566)
* [Processus ajouté la limitation pour réduire l’utilisation du processeur](https://github.com/NuGet/Home/issues/356)
* Une référence de bibliothèque de classes portable gestion améliorée
    * [https://github.com/NuGet/Home/issues/562](https://github.com/NuGet/Home/issues/562)
    * [https://github.com/NuGet/Home/issues/454](https://github.com/NuGet/Home/issues/454)
    * [https://github.com/NuGet/Home/issues/440](https://github.com/NuGet/Home/issues/440)
* [La saisie semi-automatique service a été respectant la casse](https://github.com/NuGet/Home/issues/198)
* [Mise à jour pour rétablir les informations d’identification de l’authentification de base](https://github.com/NuGet/Home/issues/456)
* [Journalisation des erreurs améliorées](https://github.com/NuGet/Home/issues/407)
* [Powershell amélioré les messages d’erreur lors de l’appel de Package de mise à jour](https://github.com/NuGet/Home/issues/5)

Téléchargez ce [mettre à jour à l’extension NuGet](https://nuget.codeplex.com/releases/view/615507) à partir de Codeplex et gardez un œil [notre blog](http://blog.nuget.org) pour plus d’avancement et les annonces de NuGet 3.0 !