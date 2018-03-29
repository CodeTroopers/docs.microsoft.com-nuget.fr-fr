---
title: Vérifier la commande NuGet CLI | Documents Microsoft
author: dtivel
ms.author: dtivel
manager: doronm
ms.date: 03/06/2018
ms.topic: reference
ms.prod: nuget
ms.technology: ''
description: Informations de référence pour le nuget.exe vérifier la commande
keywords: vérifier la référence de NuGet, vérifiez la commande
ms.reviewer:
- karann
- rmpablos
ms.workload:
- dotnet
- aspnet
ms.openlocfilehash: 4423e491e0ab5dc1e13982440db42bc9b0e85c38
ms.sourcegitcommit: beb229893559824e8abd6ab16707fd5fe1c6ac26
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2018
---
# <a name="verify-command-nuget-cli"></a><span data-ttu-id="ac3eb-104">Vérifiez la commande (NuGet CLI)</span><span class="sxs-lookup"><span data-stu-id="ac3eb-104">verify command (NuGet CLI)</span></span>

<span data-ttu-id="ac3eb-105">**S’applique à :** package consommation &bullet; **versions prises en charge :** 4.6 +</span><span class="sxs-lookup"><span data-stu-id="ac3eb-105">**Applies to:** package consumption &bullet; **Supported versions:** 4.6+</span></span>

<span data-ttu-id="ac3eb-106">Vérifie un package.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-106">Verifies a package.</span></span>

## <a name="usage"></a><span data-ttu-id="ac3eb-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ac3eb-107">Usage</span></span>

```cli
nuget verify <package(s)> [options]
```

<span data-ttu-id="ac3eb-108">où `<package(s)>` est un ou plusieurs `.nupkg` fichiers.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-108">where `<package(s)>` is one or more `.nupkg` files.</span></span>

## <a name="options"></a><span data-ttu-id="ac3eb-109">Options</span><span class="sxs-lookup"><span data-stu-id="ac3eb-109">Options</span></span>

| <span data-ttu-id="ac3eb-110">Option</span><span class="sxs-lookup"><span data-stu-id="ac3eb-110">Option</span></span> | <span data-ttu-id="ac3eb-111">Description</span><span class="sxs-lookup"><span data-stu-id="ac3eb-111">Description</span></span> |
| --- | --- |
| <span data-ttu-id="ac3eb-112">Tous</span><span class="sxs-lookup"><span data-stu-id="ac3eb-112">All</span></span> | <span data-ttu-id="ac3eb-113">Spécifie que toutes les vérifications possibles doivent être effectuées sur l’ou les packages.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-113">Specifies that all verifications possible should be performed on the package(s).</span></span> |
| <span data-ttu-id="ac3eb-114">CertificateFingerprint</span><span class="sxs-lookup"><span data-stu-id="ac3eb-114">CertificateFingerprint</span></span> | <span data-ttu-id="ac3eb-115">Spécifie un ou plusieurs des empreintes certificat SHA-256 de certificats (s), lesquelles packages signés doivent être signées avec.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-115">Specifies one or more SHA-256 certificate fingerprints of certificates(s) which signed packages must be signed with.</span></span> <span data-ttu-id="ac3eb-116">Une empreinte de certificat SHA-256 est un hachage SHA-256 du certificat.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-116">A certificate SHA-256 fingerprint is a SHA-256 hash of the certificate.</span></span> <span data-ttu-id="ac3eb-117">Plusieurs entrées doivent être séparées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-117">Multiple inputs should be semicolon separated.</span></span> |
| <span data-ttu-id="ac3eb-118">ConfigFile</span><span class="sxs-lookup"><span data-stu-id="ac3eb-118">ConfigFile</span></span> | <span data-ttu-id="ac3eb-119">Le fichier de configuration NuGet à appliquer.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-119">The NuGet configuration file to apply.</span></span> <span data-ttu-id="ac3eb-120">Si non spécifié, `%AppData%\NuGet\NuGet.Config` (Windows) ou `~/.nuget/NuGet/NuGet.Config` (Mac/Linux) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-120">If not specified, `%AppData%\NuGet\NuGet.Config` (Windows) or `~/.nuget/NuGet/NuGet.Config` (Mac/Linux) is used.</span></span>|
| <span data-ttu-id="ac3eb-121">ForceEnglishOutput</span><span class="sxs-lookup"><span data-stu-id="ac3eb-121">ForceEnglishOutput</span></span> | <span data-ttu-id="ac3eb-122">Force nuget.exe pour exécuter à l’aide d’une culture dite indifférente, en anglais.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-122">Forces nuget.exe to run using an invariant, English-based culture.</span></span> |
| <span data-ttu-id="ac3eb-123">Help</span><span class="sxs-lookup"><span data-stu-id="ac3eb-123">Help</span></span> | <span data-ttu-id="ac3eb-124">Affiche l’aide de la commande.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-124">Displays help information for the command.</span></span> |
| <span data-ttu-id="ac3eb-125">Non interactif</span><span class="sxs-lookup"><span data-stu-id="ac3eb-125">NonInteractive</span></span> | <span data-ttu-id="ac3eb-126">Supprime les invites de saisie utilisateur ou les confirmations.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-126">Suppresses prompts for user input or confirmations.</span></span> |
| <span data-ttu-id="ac3eb-127">Signatures</span><span class="sxs-lookup"><span data-stu-id="ac3eb-127">Signatures</span></span> | <span data-ttu-id="ac3eb-128">Spécifie que la vérification des signatures de package doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-128">Specifies that package signature verification should be performed.</span></span> |
| <span data-ttu-id="ac3eb-129">Commentaires</span><span class="sxs-lookup"><span data-stu-id="ac3eb-129">Verbosity</span></span> | <span data-ttu-id="ac3eb-130">Spécifie la quantité de détails affichés dans la sortie : *normal*, *silencieux*, *détaillées*.</span><span class="sxs-lookup"><span data-stu-id="ac3eb-130">Specifies the amount of detail displayed in the output: *normal*, *quiet*, *detailed*.</span></span> |

## <a name="examples"></a><span data-ttu-id="ac3eb-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="ac3eb-131">Examples</span></span>

```cli
nuget verify -Signatures .\..\MyPackage.nupkg -CertificateFingerprint "CE40881FF5F0AD3E58965DA20A9F571EF1651A56933748E1BF1C99E537C4E039;5F874AAF47BCB268A19357364E7FBB09D6BF9E8A93E1229909AC5CAC865802E2" -Verbosity detailed

nuget verify -Signatures c:\packages\MyPackage.nupkg -CertificateFingerprint CE40881FF5F0AD3E58965DA20A9F571EF1651A56933748E1BF1C99E537C4E039

nuget verify -Signatures MyPackage.nupkg -Verbosity quiet

nuget verify -Signatures .\*.nupkg
```