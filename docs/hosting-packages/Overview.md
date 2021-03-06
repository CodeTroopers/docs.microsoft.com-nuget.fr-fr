---
title: Vue d’ensemble de l’hébergement de vos propres flux NuGet
description: Vue d’ensemble des possibilités d’hébergement de vos propres galeries ou flux de packages NuGet localement ou à distance.
author: karann-msft
ms.author: karann
manager: unnir
ms.date: 08/25/2017
ms.topic: conceptual
ms.reviewer: anangaur
ms.openlocfilehash: 48ebddb26aa6c236609691e099a82db80075944e
ms.sourcegitcommit: 2a6d200012cdb4cbf5ab1264f12fecf9ae12d769
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34818417"
---
# <a name="hosting-your-own-nuget-feeds"></a>Hébergement de vos propres flux NuGet

Plutôt que de mettre les packages à la disposition de tous, vous pouvez les réserver à un public limité, tel que votre organisation ou groupe de travail. De plus, certaines sociétés peuvent souhaiter restreindre les bibliothèques tierces que sont susceptibles d’utiliser leurs développeurs en leur demandant de puiser dans une source de packages limitée plutôt que dans nuget.org.

À ces fins, NuGet prend en charge la configuration de sources de packages privées des façons suivantes :

- Flux local : les packages sont simplement placés sur un partage de fichiers réseau approprié, dans l’idéal, en utilisant `nuget init` et `nuget add` pour créer une structure de dossiers hiérarchique (NuGet 3.3+). Pour plus d’informations, consultez [Flux locaux](../hosting-packages/local-feeds.md).
- NuGet.Server : les packages sont accessibles via un serveur HTTP local. Pour plus d’informations, consultez [NuGet.Server](../hosting-packages/nuget-server.md).
- Galerie NuGet : les packages sont hébergés sur un serveur Internet à l’aide du [projet de Galerie NuGet](https://github.com/NuGet/NuGetGallery#build-and-run-the-gallery-in-arbitrary-number-easy-steps) (github.com). Avec la Galerie NuGet, gérez les utilisateurs et profitez de fonctionnalités telles qu’une interface utilisateur web complète qui permet de rechercher et d’explorer les packages à partir du navigateur, comme nuget.org.

Il existe également plusieurs autres produits d’hébergement NuGet qui prennent en charge les flux privés distants, notamment les suivants :

- [Visual Studio Team Services Package Management](https://www.visualstudio.com/docs/package/nuget/publish), qui est également disponible sur Team Foundation Server 2017 et ultérieur.
- [MyGet](http://myget.org)
- [ProGet](http://inedo.com/proget) d’Inedo
- [NuGet Server](http://nugetserver.net/) : projet communautaire d’Inedo
- [NuGet Server (Open Source)](http://nuget-server.net) : implémentation open source similaire à NuGet Server d’Inedo
- [Artifactory](https://www.jfrog.com/artifactory/) de JFrog
- [Nexus](http://www.sonatype.org/nexus/) de Sonatype
- [TeamCity](https://www.jetbrains.com/teamcity/) de JetBrains

Quelle que soit la façon dont les packages sont hébergés, vous y accédez en les ajoutant à la liste des sources disponibles dans `NuGet.Config`. Vous pouvez effectuer cette opération dans Visual Studio, comme décrit dans [Sources de packages](../tools/package-manager-ui.md#package-sources), ou à partir de la ligne de commande à l’aide de [`nuget sources`](../tools/cli-ref-sources.md). Le chemin d’une source peut être le chemin d’un dossier local, le nom d’un réseau ou une URL.
