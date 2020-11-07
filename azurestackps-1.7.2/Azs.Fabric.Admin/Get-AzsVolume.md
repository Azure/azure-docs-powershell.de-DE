---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826536"
---
# <span data-ttu-id="4d843-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="4d843-101">Get-AzsVolume</span></span>

## <span data-ttu-id="4d843-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d843-102">SYNOPSIS</span></span>
<span data-ttu-id="4d843-103">Gibt eine Liste aller Speicher-Volumes an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="4d843-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="4d843-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d843-104">SYNTAX</span></span>

### <span data-ttu-id="4d843-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d843-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4d843-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4d843-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4d843-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d843-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4d843-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d843-108">DESCRIPTION</span></span>
<span data-ttu-id="4d843-109">Gibt eine Liste aller Speicher-Volumes an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="4d843-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="4d843-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d843-110">EXAMPLES</span></span>

### <span data-ttu-id="4d843-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4d843-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="4d843-112">Sie erhalten eine Liste aller Speicher-Volumes an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="4d843-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="4d843-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4d843-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="4d843-114">Besorgen Sie sich ein Speichervolumen nach Name an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="4d843-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="4d843-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d843-115">PARAMETERS</span></span>

### <span data-ttu-id="4d843-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="4d843-116">-Filter</span></span>
<span data-ttu-id="4d843-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="4d843-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="4d843-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="4d843-118">-Location</span></span>
<span data-ttu-id="4d843-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4d843-119">Location of the resource.</span></span>

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

### <span data-ttu-id="4d843-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d843-120">-Name</span></span>
<span data-ttu-id="4d843-121">Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="4d843-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="4d843-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d843-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d843-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="4d843-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4d843-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4d843-124">-ResourceId</span></span>
<span data-ttu-id="4d843-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4d843-125">The resource id.</span></span>

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

### <span data-ttu-id="4d843-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4d843-126">-ScaleUnit</span></span>
<span data-ttu-id="4d843-127">Der Name der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="4d843-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="4d843-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="4d843-128">-StorageSubSystem</span></span>
<span data-ttu-id="4d843-129">Speichersubsystem, in dem sich die Lautstärke befindet.</span><span class="sxs-lookup"><span data-stu-id="4d843-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="4d843-130">-Top</span><span class="sxs-lookup"><span data-stu-id="4d843-130">-Top</span></span>
<span data-ttu-id="4d843-131">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="4d843-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4d843-132">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="4d843-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4d843-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="4d843-133">-Skip</span></span>
<span data-ttu-id="4d843-134">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="4d843-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4d843-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d843-135">CommonParameters</span></span>
<span data-ttu-id="4d843-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d843-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d843-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d843-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d843-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d843-138">INPUTS</span></span>

## <span data-ttu-id="4d843-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d843-139">OUTPUTS</span></span>

### <span data-ttu-id="4d843-140">Microsoft. AzureStack. Management. Fabric. admin. Models. Volume</span><span class="sxs-lookup"><span data-stu-id="4d843-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="4d843-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d843-141">NOTES</span></span>

## <span data-ttu-id="4d843-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d843-142">RELATED LINKS</span></span>
