---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475469"
---
# <span data-ttu-id="6e904-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="6e904-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="6e904-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e904-102">SYNOPSIS</span></span>
<span data-ttu-id="6e904-103">Gibt eine Liste aller Speicherpools für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="6e904-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="6e904-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e904-104">SYNTAX</span></span>

### <span data-ttu-id="6e904-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e904-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6e904-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6e904-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e904-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e904-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6e904-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e904-108">DESCRIPTION</span></span>
<span data-ttu-id="6e904-109">Gibt eine Liste aller Speicherpools für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="6e904-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="6e904-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e904-110">EXAMPLES</span></span>

### <span data-ttu-id="6e904-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6e904-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="6e904-112">Abrufen aller Speicherpools an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="6e904-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="6e904-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6e904-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="6e904-114">Besorgen Sie sich eine Speicherpools an einem bestimmten Speicherort, wenn Sie einen speicherpoolnamen erhalten.</span><span class="sxs-lookup"><span data-stu-id="6e904-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="6e904-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e904-115">PARAMETERS</span></span>

### <span data-ttu-id="6e904-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="6e904-116">-Filter</span></span>
<span data-ttu-id="6e904-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="6e904-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="6e904-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="6e904-118">-Location</span></span>
<span data-ttu-id="6e904-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="6e904-119">Location of the resource.</span></span>

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

### <span data-ttu-id="6e904-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6e904-120">-Name</span></span>
<span data-ttu-id="6e904-121">Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="6e904-121">Storage pool name.</span></span>

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

### <span data-ttu-id="6e904-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e904-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e904-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e904-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6e904-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6e904-124">-ResourceId</span></span>
<span data-ttu-id="6e904-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6e904-125">The resource id.</span></span>

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

### <span data-ttu-id="6e904-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="6e904-126">-Skip</span></span>
<span data-ttu-id="6e904-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="6e904-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6e904-128">-Speichersystem</span><span class="sxs-lookup"><span data-stu-id="6e904-128">-StorageSystem</span></span>
<span data-ttu-id="6e904-129">Speichersystem, in dem sich der Speicherpool befindet.</span><span class="sxs-lookup"><span data-stu-id="6e904-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="6e904-130">-Top</span><span class="sxs-lookup"><span data-stu-id="6e904-130">-Top</span></span>
<span data-ttu-id="6e904-131">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="6e904-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6e904-132">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6e904-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6e904-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e904-133">CommonParameters</span></span>
<span data-ttu-id="6e904-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e904-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e904-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e904-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e904-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e904-136">INPUTS</span></span>

## <span data-ttu-id="6e904-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e904-137">OUTPUTS</span></span>

### <span data-ttu-id="6e904-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="6e904-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="6e904-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e904-139">NOTES</span></span>

## <span data-ttu-id="6e904-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e904-140">RELATED LINKS</span></span>

