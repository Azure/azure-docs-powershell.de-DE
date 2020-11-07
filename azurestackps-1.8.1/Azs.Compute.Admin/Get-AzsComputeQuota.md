---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840791"
---
# <span data-ttu-id="a646e-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="a646e-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="a646e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a646e-102">SYNOPSIS</span></span>
<span data-ttu-id="a646e-103">Gibt Kontingente zurück, die die Kontingentgrenzen für Compute-Objekte angeben.</span><span class="sxs-lookup"><span data-stu-id="a646e-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="a646e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a646e-104">SYNTAX</span></span>

### <span data-ttu-id="a646e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a646e-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="a646e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a646e-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="a646e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a646e-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a646e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a646e-108">DESCRIPTION</span></span>
<span data-ttu-id="a646e-109">Abrufen einer Liste vorhandener Kontingente</span><span class="sxs-lookup"><span data-stu-id="a646e-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="a646e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a646e-110">EXAMPLES</span></span>

### <span data-ttu-id="a646e-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a646e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="a646e-112">Rufen Sie alle Compute-Kontingente an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="a646e-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="a646e-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a646e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="a646e-114">Abrufen eines bestimmten Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="a646e-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="a646e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a646e-115">PARAMETERS</span></span>

### <span data-ttu-id="a646e-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="a646e-116">-Location</span></span>
<span data-ttu-id="a646e-117">{{Fill Location Description}}</span><span class="sxs-lookup"><span data-stu-id="a646e-117">{{Fill Location Description}}</span></span>

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

### <span data-ttu-id="a646e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a646e-118">-Name</span></span>
<span data-ttu-id="a646e-119">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="a646e-119">Name of the quota.</span></span>

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

### <span data-ttu-id="a646e-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a646e-120">-ResourceId</span></span>
<span data-ttu-id="a646e-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a646e-121">The resource id.</span></span>

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

### <span data-ttu-id="a646e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a646e-122">CommonParameters</span></span>
<span data-ttu-id="a646e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a646e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a646e-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a646e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a646e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a646e-125">INPUTS</span></span>

## <span data-ttu-id="a646e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a646e-126">OUTPUTS</span></span>

### <span data-ttu-id="a646e-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="a646e-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="a646e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a646e-128">NOTES</span></span>

## <span data-ttu-id="a646e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a646e-129">RELATED LINKS</span></span>

