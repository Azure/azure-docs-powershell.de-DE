---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93828043"
---
# <span data-ttu-id="883d9-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="883d9-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="883d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="883d9-102">SYNOPSIS</span></span>
<span data-ttu-id="883d9-103">Gibt eine Liste der Status der einzelnen Ressourcen unter einem Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="883d9-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="883d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="883d9-104">SYNTAX</span></span>

### <span data-ttu-id="883d9-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="883d9-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="883d9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="883d9-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="883d9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="883d9-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="883d9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="883d9-108">DESCRIPTION</span></span>
<span data-ttu-id="883d9-109">Gibt eine Liste der Status der einzelnen Ressourcen unter einem Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="883d9-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="883d9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="883d9-110">EXAMPLES</span></span>

### <span data-ttu-id="883d9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="883d9-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="883d9-112">Gibt eine Liste der Status der einzelnen Ressourcen unter einem Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="883d9-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="883d9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="883d9-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="883d9-114">Gibt den Integritätsstatus unter einem für Microsoft. Fabric. admin zurück.</span><span class="sxs-lookup"><span data-stu-id="883d9-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="883d9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="883d9-115">PARAMETERS</span></span>

### <span data-ttu-id="883d9-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="883d9-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="883d9-117">Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="883d9-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883d9-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="883d9-118">-ResourceRegistrationId</span></span>


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

### <span data-ttu-id="883d9-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="883d9-119">-Location</span></span>
<span data-ttu-id="883d9-120">Name der Region</span><span class="sxs-lookup"><span data-stu-id="883d9-120">Name of the region</span></span>

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

### <span data-ttu-id="883d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="883d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="883d9-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="883d9-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="883d9-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="883d9-123">-ResourceId</span></span>
<span data-ttu-id="883d9-124">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="883d9-124">The resource id.</span></span>

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

### <span data-ttu-id="883d9-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="883d9-125">-Filter</span></span>
<span data-ttu-id="883d9-126">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="883d9-126">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883d9-127">-Top</span><span class="sxs-lookup"><span data-stu-id="883d9-127">-Top</span></span>
<span data-ttu-id="883d9-128">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="883d9-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="883d9-129">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="883d9-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883d9-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="883d9-130">-Skip</span></span>
<span data-ttu-id="883d9-131">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="883d9-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="883d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883d9-132">CommonParameters</span></span>
<span data-ttu-id="883d9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="883d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883d9-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="883d9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883d9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="883d9-135">INPUTS</span></span>

## <span data-ttu-id="883d9-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="883d9-136">OUTPUTS</span></span>

### <span data-ttu-id="883d9-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="883d9-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="883d9-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="883d9-138">NOTES</span></span>

## <span data-ttu-id="883d9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="883d9-139">RELATED LINKS</span></span>
