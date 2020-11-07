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
ms.locfileid: "93827351"
---
# <span data-ttu-id="b4d67-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b4d67-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="b4d67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4d67-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d67-103">Gibt Kontingente zurück, die die Kontingentgrenzen für Compute-Objekte angeben.</span><span class="sxs-lookup"><span data-stu-id="b4d67-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="b4d67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4d67-104">SYNTAX</span></span>

### <span data-ttu-id="b4d67-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4d67-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d67-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b4d67-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4d67-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d67-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b4d67-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4d67-108">DESCRIPTION</span></span>
<span data-ttu-id="b4d67-109">Abrufen einer Liste vorhandener Kontingente</span><span class="sxs-lookup"><span data-stu-id="b4d67-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="b4d67-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4d67-110">EXAMPLES</span></span>

### <span data-ttu-id="b4d67-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b4d67-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="b4d67-112">Rufen Sie alle Compute-Kontingente an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="b4d67-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="b4d67-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b4d67-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="b4d67-114">Abrufen eines bestimmten Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="b4d67-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="b4d67-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4d67-115">PARAMETERS</span></span>

### <span data-ttu-id="b4d67-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="b4d67-116">-Location</span></span>
<span data-ttu-id="b4d67-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b4d67-117">Location of the resource.</span></span>

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

### <span data-ttu-id="b4d67-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b4d67-118">-Name</span></span>
<span data-ttu-id="b4d67-119">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="b4d67-119">Name of the quota.</span></span>

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

### <span data-ttu-id="b4d67-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b4d67-120">-ResourceId</span></span>
<span data-ttu-id="b4d67-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b4d67-121">The resource id.</span></span>

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

### <span data-ttu-id="b4d67-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d67-122">CommonParameters</span></span>
<span data-ttu-id="b4d67-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d67-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d67-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d67-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d67-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4d67-125">INPUTS</span></span>

## <span data-ttu-id="b4d67-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4d67-126">OUTPUTS</span></span>

### <span data-ttu-id="b4d67-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="b4d67-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="b4d67-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4d67-128">NOTES</span></span>

## <span data-ttu-id="b4d67-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4d67-129">RELATED LINKS</span></span>

