---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475354"
---
# <span data-ttu-id="3b3be-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="3b3be-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="3b3be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b3be-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3be-103">Gibt eine Liste aller Speicher-Volumes an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="3b3be-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="3b3be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b3be-104">SYNTAX</span></span>

### <span data-ttu-id="3b3be-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b3be-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3b3be-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3b3be-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3b3be-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b3be-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3b3be-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3be-108">DESCRIPTION</span></span>
<span data-ttu-id="3b3be-109">Gibt eine Liste aller Speicher-Volumes an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="3b3be-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="3b3be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b3be-110">EXAMPLES</span></span>

### <span data-ttu-id="3b3be-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b3be-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="3b3be-112">Sie erhalten eine Liste aller Speicher-Volumes an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="3b3be-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="3b3be-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b3be-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="3b3be-114">Besorgen Sie sich ein Speichervolumen nach Name an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="3b3be-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="3b3be-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b3be-115">PARAMETERS</span></span>

### <span data-ttu-id="3b3be-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="3b3be-116">-Filter</span></span>
<span data-ttu-id="3b3be-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="3b3be-117">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3be-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="3b3be-118">-Location</span></span>
<span data-ttu-id="3b3be-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3b3be-119">Location of the resource.</span></span>

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

### <span data-ttu-id="3b3be-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3b3be-120">-Name</span></span>
<span data-ttu-id="3b3be-121">Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="3b3be-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="3b3be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3be-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b3be-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b3be-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3b3be-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3b3be-124">-ResourceId</span></span>
<span data-ttu-id="3b3be-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3b3be-125">The resource id.</span></span>

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

### <span data-ttu-id="3b3be-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="3b3be-126">-Skip</span></span>
<span data-ttu-id="3b3be-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="3b3be-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3b3be-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="3b3be-128">-StoragePool</span></span>
<span data-ttu-id="3b3be-129">Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="3b3be-129">Storage pool name.</span></span>

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

### <span data-ttu-id="3b3be-130">-Speichersystem</span><span class="sxs-lookup"><span data-stu-id="3b3be-130">-StorageSystem</span></span>
<span data-ttu-id="3b3be-131">Speichersystem, in dem sich das Infrastruktur Volumen befindet.</span><span class="sxs-lookup"><span data-stu-id="3b3be-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="3b3be-132">-Top</span><span class="sxs-lookup"><span data-stu-id="3b3be-132">-Top</span></span>
<span data-ttu-id="3b3be-133">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="3b3be-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3b3be-134">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3b3be-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3b3be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3be-135">CommonParameters</span></span>
<span data-ttu-id="3b3be-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3be-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3be-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3be-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b3be-138">INPUTS</span></span>

## <span data-ttu-id="3b3be-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b3be-139">OUTPUTS</span></span>

### <span data-ttu-id="3b3be-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Volume</span><span class="sxs-lookup"><span data-stu-id="3b3be-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="3b3be-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b3be-141">NOTES</span></span>

## <span data-ttu-id="3b3be-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b3be-142">RELATED LINKS</span></span>

