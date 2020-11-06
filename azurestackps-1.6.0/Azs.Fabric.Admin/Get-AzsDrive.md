---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474605"
---
# <span data-ttu-id="83fc9-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="83fc9-101">Get-AzsDrive</span></span>

## <span data-ttu-id="83fc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="83fc9-103">Gibt eine Liste aller Speicherlaufwerke für einen bestimmten Cluster zurück.</span><span class="sxs-lookup"><span data-stu-id="83fc9-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="83fc9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83fc9-104">SYNTAX</span></span>

### <span data-ttu-id="83fc9-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="83fc9-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="83fc9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="83fc9-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="83fc9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="83fc9-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="83fc9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83fc9-108">DESCRIPTION</span></span>
<span data-ttu-id="83fc9-109">Gibt eine Liste aller Speicherlaufwerke für einen bestimmten Cluster zurück.</span><span class="sxs-lookup"><span data-stu-id="83fc9-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="83fc9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83fc9-110">EXAMPLES</span></span>

### <span data-ttu-id="83fc9-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="83fc9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="83fc9-112">Abrufen einer Liste aller Speicherlaufwerke für einen bestimmten Cluster</span><span class="sxs-lookup"><span data-stu-id="83fc9-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="83fc9-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="83fc9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="83fc9-114">Besorgen Sie sich ein Speicherlaufwerk nach Namen für einen bestimmten Cluster.</span><span class="sxs-lookup"><span data-stu-id="83fc9-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="83fc9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="83fc9-115">PARAMETERS</span></span>

### <span data-ttu-id="83fc9-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="83fc9-116">-Filter</span></span>
<span data-ttu-id="83fc9-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="83fc9-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="83fc9-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="83fc9-118">-Location</span></span>
<span data-ttu-id="83fc9-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="83fc9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="83fc9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="83fc9-120">-Name</span></span>
<span data-ttu-id="83fc9-121">Name des Speicherlaufwerks</span><span class="sxs-lookup"><span data-stu-id="83fc9-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="83fc9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83fc9-122">-ResourceGroupName</span></span>
<span data-ttu-id="83fc9-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="83fc9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="83fc9-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="83fc9-124">-ResourceId</span></span>
<span data-ttu-id="83fc9-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="83fc9-125">The resource id.</span></span>

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

### <span data-ttu-id="83fc9-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="83fc9-126">-ScaleUnit</span></span>
<span data-ttu-id="83fc9-127">Der Name der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="83fc9-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="83fc9-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="83fc9-128">-StorageSubSystem</span></span>
<span data-ttu-id="83fc9-129">Speichersubsystem, in dem sich das Laufwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="83fc9-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="83fc9-130">-Top</span><span class="sxs-lookup"><span data-stu-id="83fc9-130">-Top</span></span>
<span data-ttu-id="83fc9-131">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="83fc9-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="83fc9-132">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="83fc9-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="83fc9-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="83fc9-133">-Skip</span></span>
<span data-ttu-id="83fc9-134">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="83fc9-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="83fc9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fc9-135">CommonParameters</span></span>
<span data-ttu-id="83fc9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83fc9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fc9-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fc9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fc9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83fc9-138">INPUTS</span></span>

## <span data-ttu-id="83fc9-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83fc9-139">OUTPUTS</span></span>

### <span data-ttu-id="83fc9-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Drive</span><span class="sxs-lookup"><span data-stu-id="83fc9-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="83fc9-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="83fc9-141">NOTES</span></span>

## <span data-ttu-id="83fc9-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83fc9-142">RELATED LINKS</span></span>
