---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007296"
---
# <span data-ttu-id="d24e2-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="d24e2-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="d24e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d24e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d24e2-103">Rufen Sie die Liste der delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="d24e2-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="d24e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d24e2-104">SYNTAX</span></span>

### <span data-ttu-id="d24e2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d24e2-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="d24e2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d24e2-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="d24e2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d24e2-107">DESCRIPTION</span></span>
<span data-ttu-id="d24e2-108">Rufen Sie die Liste der delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="d24e2-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="d24e2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d24e2-109">EXAMPLES</span></span>

### <span data-ttu-id="d24e2-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d24e2-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="d24e2-111">Rufen Sie eine Liste der Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="d24e2-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="d24e2-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d24e2-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="d24e2-113">Rufen Sie den jeweiligen Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="d24e2-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="d24e2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d24e2-114">PARAMETERS</span></span>

### <span data-ttu-id="d24e2-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="d24e2-115">-DelegatedProviderId</span></span>
<span data-ttu-id="d24e2-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="d24e2-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24e2-117">CommonParameters</span></span>
<span data-ttu-id="d24e2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24e2-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24e2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24e2-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d24e2-120">INPUTS</span></span>

## <span data-ttu-id="d24e2-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d24e2-121">OUTPUTS</span></span>

### <span data-ttu-id="d24e2-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="d24e2-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="d24e2-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d24e2-123">NOTES</span></span>

## <span data-ttu-id="d24e2-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d24e2-124">RELATED LINKS</span></span>

