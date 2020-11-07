---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827864"
---
# <span data-ttu-id="162c6-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="162c6-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="162c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="162c6-102">SYNOPSIS</span></span>
<span data-ttu-id="162c6-103">Rufen Sie die Liste der Abonnement Ressourcenanbieter Kontingente an einem Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="162c6-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="162c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="162c6-104">SYNTAX</span></span>

### <span data-ttu-id="162c6-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="162c6-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="162c6-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="162c6-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="162c6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="162c6-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="162c6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="162c6-108">DESCRIPTION</span></span>
<span data-ttu-id="162c6-109">Rufen Sie die Liste der Kontingente an einem Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="162c6-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="162c6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="162c6-110">EXAMPLES</span></span>

### <span data-ttu-id="162c6-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="162c6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="162c6-112">Rufen Sie die Liste der Abonnement Ressourcenanbieter Kontingente an einem Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="162c6-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="162c6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="162c6-113">PARAMETERS</span></span>

### <span data-ttu-id="162c6-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="162c6-114">-Location</span></span>
<span data-ttu-id="162c6-115">Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="162c6-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="162c6-116">-Name</span></span>
<span data-ttu-id="162c6-117">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="162c6-117">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162c6-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="162c6-118">-ResourceId</span></span>
<span data-ttu-id="162c6-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="162c6-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162c6-120">CommonParameters</span></span>
<span data-ttu-id="162c6-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="162c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162c6-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="162c6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162c6-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="162c6-123">INPUTS</span></span>

## <span data-ttu-id="162c6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="162c6-124">OUTPUTS</span></span>

### <span data-ttu-id="162c6-125">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="162c6-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="162c6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="162c6-126">NOTES</span></span>

## <span data-ttu-id="162c6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="162c6-127">RELATED LINKS</span></span>

