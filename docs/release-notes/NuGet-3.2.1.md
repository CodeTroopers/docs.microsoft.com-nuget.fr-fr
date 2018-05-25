---
title: Notes de mise à jour de NuGet 3.2.1
description: Notes de publication pour NuGet 3.2.1, notamment de problèmes connus, des correctifs de bogues, les fonctionnalités ajoutées et dcr.
author: karann-msft
ms.author: karann
manager: unnir
ms.date: 11/11/2016
ms.topic: conceptual
ms.openlocfilehash: 039fabaaacfdffd76fa88ff8183548e97cd4719b
ms.sourcegitcommit: 3eab9c4dd41ea7ccd2c28bb5ab16f6fbbec13708
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="nuget-321-release-notes"></a><span data-ttu-id="7bcda-103">Notes de mise à jour de NuGet 3.2.1</span><span class="sxs-lookup"><span data-stu-id="7bcda-103">NuGet 3.2.1 Release Notes</span></span>

<span data-ttu-id="7bcda-104">[Notes de publication NuGet 3.2](../release-notes/nuget-3.2.md) | [NuGet 3.3 Notes de publication](../release-notes/nuget-3.3.md)</span><span class="sxs-lookup"><span data-stu-id="7bcda-104">[NuGet 3.2 Release Notes](../release-notes/nuget-3.2.md) | [NuGet 3.3 Release Notes](../release-notes/nuget-3.3.md)</span></span>

<span data-ttu-id="7bcda-105">NuGet 3.2.1 pour la ligne de commande a été publiée le 12 octobre 2015, avec quelques optimisations et correctifs pour la version 3.2 et est disponible à partir de [dist.nuget.org](http://dist.nuget.org/index.html).</span><span class="sxs-lookup"><span data-stu-id="7bcda-105">NuGet 3.2.1 for the command-line was released October 12, 2015 with a handful of optimizations and fixes for the 3.2 release and is available from [dist.nuget.org](http://dist.nuget.org/index.html).</span></span>

## <a name="improvements"></a><span data-ttu-id="7bcda-106">Améliorations apportées à</span><span class="sxs-lookup"><span data-stu-id="7bcda-106">Improvements</span></span>

* <span data-ttu-id="7bcda-107">NuGet utilise désormais le fichier de configuration avec la casse d’origine de `NuGet.Config`.</span><span class="sxs-lookup"><span data-stu-id="7bcda-107">NuGet now uses the configuration file with the original casing of `NuGet.Config`.</span></span>  <span data-ttu-id="7bcda-108">Ceci est important sur les systèmes d’exploitation qui respecte la casse [1427](https://github.com/NuGet/Home/issues/1427)</span><span class="sxs-lookup"><span data-stu-id="7bcda-108">This is important on case-sensitive operating systems [1427](https://github.com/NuGet/Home/issues/1427)</span></span>
* <span data-ttu-id="7bcda-109">NuGet restore ignore désormais des projets dnx (`*.xproj`) qui doit être traité avec `dnu` [1227](https://github.com/NuGet/Home/issues/1227)</span><span class="sxs-lookup"><span data-stu-id="7bcda-109">NuGet restore will now ignore dnx projects (`*.xproj`) that should be processed with `dnu` [1227](https://github.com/NuGet/Home/issues/1227)</span></span>
* <span data-ttu-id="7bcda-110">Optimisé l’utilisation du réseau lorsque vous travaillez avec `index.json` et les données de l’enregistrement du package [1426](https://github.com/NuGet/Home/issues/1426)</span><span class="sxs-lookup"><span data-stu-id="7bcda-110">Optimized network utilization when working with `index.json` and package registration data [1426](https://github.com/NuGet/Home/issues/1426)</span></span>
* <span data-ttu-id="7bcda-111">Téléchargement de ressources gérant de manière à être plus robustes avec les services v2 [1448](https://github.com/NuGet/Home/issues/1448)</span><span class="sxs-lookup"><span data-stu-id="7bcda-111">Improved resource download handling to be more robust with v2 services [1448](https://github.com/NuGet/Home/issues/1448)</span></span>

## <a name="fixes"></a><span data-ttu-id="7bcda-112">Correctifs</span><span class="sxs-lookup"><span data-stu-id="7bcda-112">Fixes</span></span>

* <span data-ttu-id="7bcda-113">Met à jour correctement mise à jour de NuGet `.csproj` / `.vcxproj` références [1483](https://github.com/NuGet/Home/issues/1483)</span><span class="sxs-lookup"><span data-stu-id="7bcda-113">NuGet update correctly updates `.csproj`/`.vcxproj` references [1483](https://github.com/NuGet/Home/issues/1483)</span></span>
* <span data-ttu-id="7bcda-114">Maintenant empêchant toute un dossier .nuget local création lorsque Impossible de trouver un SpecialFolders.UserProfile [1531](https://github.com/NuGet/Home/issues/1531)</span><span class="sxs-lookup"><span data-stu-id="7bcda-114">Now preventing a local .nuget folder from being created when a SpecialFolders.UserProfile cannot be located [1531](https://github.com/NuGet/Home/issues/1531)</span></span>
* <span data-ttu-id="7bcda-115">Amélioration de la gestion des packages dans le cache local qui sont endommagés pendant le téléchargement [1405](https://github.com/NuGet/Home/issues/1405) [1157](https://github.com/NuGet/Home/issues/1157)</span><span class="sxs-lookup"><span data-stu-id="7bcda-115">Improved handling of packages in local cache that are corrupted during download [1405](https://github.com/NuGet/Home/issues/1405) [1157](https://github.com/NuGet/Home/issues/1157)</span></span>

<span data-ttu-id="7bcda-116">Une liste complète des problèmes résolus pour les en ligne de commande et de Visual Studio se trouve dans NuGet GitHub [3.2.1 jalon](https://github.com/NuGet/Home/issues?q=milestone%3A3.2.1+is%3Aclosed)</span><span class="sxs-lookup"><span data-stu-id="7bcda-116">A complete list of issues addressed for the command-line and Visual Studio extension can be found in the NuGet GitHub [3.2.1 milestone](https://github.com/NuGet/Home/issues?q=milestone%3A3.2.1+is%3Aclosed)</span></span>

## <a name="known-issues"></a><span data-ttu-id="7bcda-117">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="7bcda-117">Known Issues</span></span>

<span data-ttu-id="7bcda-118">Nous continuons à effectuer le suivi des problèmes sur notre liste de problèmes de GitHub qui se trouve à : [http://github.com/nuget/home/issues](http://github.com/nuget/home/issues)</span><span class="sxs-lookup"><span data-stu-id="7bcda-118">We continue to track issues on our GitHub issues list which can be found at: [http://github.com/nuget/home/issues](http://github.com/nuget/home/issues)</span></span>