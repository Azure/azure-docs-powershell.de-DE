---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475453"
---
# <span data-ttu-id="df5f4-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="df5f4-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="df5f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="df5f4-103">Rufen Sie die Liste der delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="df5f4-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="df5f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df5f4-104">SYNTAX</span></span>

### <span data-ttu-id="df5f4-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="df5f4-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="df5f4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="df5f4-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="df5f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df5f4-107">DESCRIPTION</span></span>
<span data-ttu-id="df5f4-108">Rufen Sie die Liste der delegatedProviders.</span><span class="sxs-lookup"><span data-stu-id="df5f4-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="df5f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df5f4-109">EXAMPLES</span></span>

### <span data-ttu-id="df5f4-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="df5f4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="df5f4-111">Rufen Sie eine Liste der Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="df5f4-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="df5f4-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="df5f4-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="df5f4-113">Rufen Sie den jeweiligen Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="df5f4-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="df5f4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="df5f4-114">PARAMETERS</span></span>

### <span data-ttu-id="df5f4-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="df5f4-115">-DelegatedProviderId</span></span>
<span data-ttu-id="df5f4-116">DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="df5f4-116">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="df5f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5f4-117">CommonParameters</span></span>
<span data-ttu-id="df5f4-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df5f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5f4-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5f4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5f4-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df5f4-120">INPUTS</span></span>

## <span data-ttu-id="df5f4-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df5f4-121">OUTPUTS</span></span>

### <span data-ttu-id="df5f4-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="df5f4-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="df5f4-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="df5f4-123">NOTES</span></span>

## <span data-ttu-id="df5f4-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df5f4-124">RELATED LINKS</span></span>

