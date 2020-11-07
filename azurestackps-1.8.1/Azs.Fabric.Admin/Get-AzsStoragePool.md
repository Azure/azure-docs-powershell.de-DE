---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828232"
---
# <span data-ttu-id="5a03d-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="5a03d-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="5a03d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a03d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a03d-103">Gibt eine Liste aller Speicherpools für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5a03d-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="5a03d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a03d-104">SYNTAX</span></span>

### <span data-ttu-id="5a03d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a03d-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5a03d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5a03d-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a03d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a03d-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5a03d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a03d-108">DESCRIPTION</span></span>
<span data-ttu-id="5a03d-109">Gibt eine Liste aller Speicherpools für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5a03d-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="5a03d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a03d-110">EXAMPLES</span></span>

### <span data-ttu-id="5a03d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a03d-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="5a03d-112">Abrufen aller Speicherpools an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="5a03d-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="5a03d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5a03d-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="5a03d-114">Besorgen Sie sich eine Speicherpools an einem bestimmten Speicherort, wenn Sie einen speicherpoolnamen erhalten.</span><span class="sxs-lookup"><span data-stu-id="5a03d-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="5a03d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a03d-115">PARAMETERS</span></span>

### <span data-ttu-id="5a03d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a03d-116">-Name</span></span>
<span data-ttu-id="5a03d-117">Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="5a03d-117">Storage pool name.</span></span>

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

### <span data-ttu-id="5a03d-118">-Speichersystem</span><span class="sxs-lookup"><span data-stu-id="5a03d-118">-StorageSystem</span></span>
<span data-ttu-id="5a03d-119">Der Name des Speichersubsystems.</span><span class="sxs-lookup"><span data-stu-id="5a03d-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="5a03d-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="5a03d-120">-Location</span></span>
<span data-ttu-id="5a03d-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5a03d-121">Location of the resource.</span></span>

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

### <span data-ttu-id="5a03d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a03d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a03d-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="5a03d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5a03d-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5a03d-124">-ResourceId</span></span>
<span data-ttu-id="5a03d-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5a03d-125">The resource id.</span></span>

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

### <span data-ttu-id="5a03d-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="5a03d-126">-Filter</span></span>
<span data-ttu-id="5a03d-127">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="5a03d-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="5a03d-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="5a03d-128">-Skip</span></span>
<span data-ttu-id="5a03d-129">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="5a03d-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5a03d-130">-Top</span><span class="sxs-lookup"><span data-stu-id="5a03d-130">-Top</span></span>
<span data-ttu-id="5a03d-131">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="5a03d-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5a03d-132">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="5a03d-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5a03d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a03d-133">CommonParameters</span></span>
<span data-ttu-id="5a03d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a03d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a03d-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a03d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a03d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a03d-136">INPUTS</span></span>

## <span data-ttu-id="5a03d-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a03d-137">OUTPUTS</span></span>

### <span data-ttu-id="5a03d-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="5a03d-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="5a03d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a03d-139">NOTES</span></span>

## <span data-ttu-id="5a03d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a03d-140">RELATED LINKS</span></span>
