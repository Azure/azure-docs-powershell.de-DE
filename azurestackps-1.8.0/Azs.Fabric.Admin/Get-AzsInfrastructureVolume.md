---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827588"
---
# <span data-ttu-id="28f31-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="28f31-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="28f31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28f31-102">SYNOPSIS</span></span>
<span data-ttu-id="28f31-103">Gibt eine Liste aller Speicher-Volumes an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="28f31-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="28f31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28f31-104">SYNTAX</span></span>

### <span data-ttu-id="28f31-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="28f31-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="28f31-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="28f31-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="28f31-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="28f31-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="28f31-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28f31-108">DESCRIPTION</span></span>
<span data-ttu-id="28f31-109">Gibt eine Liste aller Speicher-Volumes an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="28f31-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="28f31-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28f31-110">EXAMPLES</span></span>

### <span data-ttu-id="28f31-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28f31-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="28f31-112">Sie erhalten eine Liste aller Speicher-Volumes an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="28f31-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="28f31-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="28f31-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="28f31-114">Besorgen Sie sich ein Speichervolumen nach Name an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="28f31-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="28f31-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="28f31-115">PARAMETERS</span></span>

### <span data-ttu-id="28f31-116">-Name</span><span class="sxs-lookup"><span data-stu-id="28f31-116">-Name</span></span>
<span data-ttu-id="28f31-117">Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="28f31-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="28f31-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="28f31-118">-StoragePool</span></span>
<span data-ttu-id="28f31-119">Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="28f31-119">Storage pool name.</span></span>

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

### <span data-ttu-id="28f31-120">-Speichersystem</span><span class="sxs-lookup"><span data-stu-id="28f31-120">-StorageSystem</span></span>
<span data-ttu-id="28f31-121">Darstellung einer Speichersystem Ressource</span><span class="sxs-lookup"><span data-stu-id="28f31-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="28f31-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="28f31-122">-Location</span></span>
<span data-ttu-id="28f31-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="28f31-123">Location of the resource.</span></span>

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

### <span data-ttu-id="28f31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28f31-124">-ResourceGroupName</span></span>
<span data-ttu-id="28f31-125">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="28f31-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="28f31-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="28f31-126">-ResourceId</span></span>
<span data-ttu-id="28f31-127">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="28f31-127">The resource id.</span></span>

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

### <span data-ttu-id="28f31-128">-Filter</span><span class="sxs-lookup"><span data-stu-id="28f31-128">-Filter</span></span>
<span data-ttu-id="28f31-129">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="28f31-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="28f31-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="28f31-130">-Skip</span></span>
<span data-ttu-id="28f31-131">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="28f31-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="28f31-132">-Top</span><span class="sxs-lookup"><span data-stu-id="28f31-132">-Top</span></span>
<span data-ttu-id="28f31-133">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="28f31-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="28f31-134">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="28f31-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="28f31-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f31-135">CommonParameters</span></span>
<span data-ttu-id="28f31-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f31-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f31-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f31-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f31-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28f31-138">INPUTS</span></span>

## <span data-ttu-id="28f31-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28f31-139">OUTPUTS</span></span>

### <span data-ttu-id="28f31-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Volume</span><span class="sxs-lookup"><span data-stu-id="28f31-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="28f31-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="28f31-141">NOTES</span></span>

## <span data-ttu-id="28f31-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28f31-142">RELATED LINKS</span></span>
