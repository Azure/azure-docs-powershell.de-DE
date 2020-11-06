---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474650"
---
# <span data-ttu-id="14834-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="14834-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="14834-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14834-102">SYNOPSIS</span></span>
<span data-ttu-id="14834-103">Gibt Kontingente zurück, die die Kontingentgrenzen für Compute-Objekte angeben.</span><span class="sxs-lookup"><span data-stu-id="14834-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="14834-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14834-104">SYNTAX</span></span>

### <span data-ttu-id="14834-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="14834-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="14834-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="14834-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="14834-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14834-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="14834-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14834-108">DESCRIPTION</span></span>
<span data-ttu-id="14834-109">Abrufen einer Liste vorhandener Kontingente</span><span class="sxs-lookup"><span data-stu-id="14834-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="14834-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14834-110">EXAMPLES</span></span>

### <span data-ttu-id="14834-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14834-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="14834-112">Rufen Sie alle Compute-Kontingente an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="14834-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="14834-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="14834-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="14834-114">Abrufen eines bestimmten Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="14834-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="14834-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="14834-115">PARAMETERS</span></span>

### <span data-ttu-id="14834-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="14834-116">-Location</span></span>
<span data-ttu-id="14834-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="14834-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14834-118">-Name</span><span class="sxs-lookup"><span data-stu-id="14834-118">-Name</span></span>
<span data-ttu-id="14834-119">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="14834-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14834-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="14834-120">-ResourceId</span></span>
<span data-ttu-id="14834-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="14834-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14834-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14834-122">CommonParameters</span></span>
<span data-ttu-id="14834-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14834-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14834-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14834-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14834-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14834-125">INPUTS</span></span>

## <span data-ttu-id="14834-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14834-126">OUTPUTS</span></span>

### <span data-ttu-id="14834-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="14834-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="14834-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="14834-128">NOTES</span></span>

## <span data-ttu-id="14834-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14834-129">RELATED LINKS</span></span>

