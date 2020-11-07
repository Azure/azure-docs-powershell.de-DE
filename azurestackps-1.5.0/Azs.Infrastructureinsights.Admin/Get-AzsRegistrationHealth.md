---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661931"
---
# <span data-ttu-id="e6acd-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="e6acd-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="e6acd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6acd-102">SYNOPSIS</span></span>
<span data-ttu-id="e6acd-103">Gibt eine Liste der Status der einzelnen Ressourcen unter einem Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="e6acd-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="e6acd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6acd-104">SYNTAX</span></span>

### <span data-ttu-id="e6acd-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6acd-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e6acd-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e6acd-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="e6acd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6acd-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="e6acd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6acd-108">DESCRIPTION</span></span>
<span data-ttu-id="e6acd-109">Gibt eine Liste der Status der einzelnen Ressourcen unter einem Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="e6acd-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="e6acd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6acd-110">EXAMPLES</span></span>

### <span data-ttu-id="e6acd-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6acd-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="e6acd-112">Gibt eine Liste der Status der einzelnen Ressourcen unter einem Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="e6acd-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="e6acd-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6acd-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="e6acd-114">Gibt den Integritätsstatus unter einem für Microsoft. Fabric. admin zurück.</span><span class="sxs-lookup"><span data-stu-id="e6acd-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="e6acd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6acd-115">PARAMETERS</span></span>

### <span data-ttu-id="e6acd-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="e6acd-116">-Filter</span></span>
<span data-ttu-id="e6acd-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="e6acd-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e6acd-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="e6acd-118">-Location</span></span>
<span data-ttu-id="e6acd-119">Name der Region</span><span class="sxs-lookup"><span data-stu-id="e6acd-119">Name of the region</span></span>

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

### <span data-ttu-id="e6acd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e6acd-120">-Name</span></span>
<span data-ttu-id="e6acd-121">Der Ressourcenname des Integritäts Objekts, das der Ressourcen Registrierungs-ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6acd-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6acd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6acd-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6acd-123">Der Ressourcengruppenname, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="e6acd-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="e6acd-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e6acd-124">-ResourceId</span></span>
<span data-ttu-id="e6acd-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e6acd-125">The resource id.</span></span>

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

### <span data-ttu-id="e6acd-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="e6acd-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="e6acd-127">Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="e6acd-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6acd-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="e6acd-128">-Skip</span></span>
<span data-ttu-id="e6acd-129">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="e6acd-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e6acd-130">-Top</span><span class="sxs-lookup"><span data-stu-id="e6acd-130">-Top</span></span>
<span data-ttu-id="e6acd-131">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="e6acd-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e6acd-132">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="e6acd-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e6acd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6acd-133">CommonParameters</span></span>
<span data-ttu-id="e6acd-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6acd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6acd-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6acd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6acd-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6acd-136">INPUTS</span></span>

## <span data-ttu-id="e6acd-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6acd-137">OUTPUTS</span></span>

### <span data-ttu-id="e6acd-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="e6acd-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="e6acd-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6acd-139">NOTES</span></span>

## <span data-ttu-id="e6acd-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6acd-140">RELATED LINKS</span></span>

