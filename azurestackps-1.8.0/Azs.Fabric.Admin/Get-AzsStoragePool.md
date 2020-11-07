---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827552"
---
# <span data-ttu-id="ff5b0-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="ff5b0-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="ff5b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5b0-103">Gibt eine Liste aller Speicherpools für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="ff5b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff5b0-104">SYNTAX</span></span>

### <span data-ttu-id="ff5b0-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff5b0-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ff5b0-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="ff5b0-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff5b0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff5b0-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ff5b0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff5b0-108">DESCRIPTION</span></span>
<span data-ttu-id="ff5b0-109">Gibt eine Liste aller Speicherpools für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="ff5b0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff5b0-110">EXAMPLES</span></span>

### <span data-ttu-id="ff5b0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff5b0-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="ff5b0-112">Abrufen aller Speicherpools an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="ff5b0-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="ff5b0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ff5b0-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="ff5b0-114">Besorgen Sie sich eine Speicherpools an einem bestimmten Speicherort, wenn Sie einen speicherpoolnamen erhalten.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="ff5b0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff5b0-115">PARAMETERS</span></span>

### <span data-ttu-id="ff5b0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ff5b0-116">-Name</span></span>
<span data-ttu-id="ff5b0-117">Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-117">Storage pool name.</span></span>

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

### <span data-ttu-id="ff5b0-118">-Speichersystem</span><span class="sxs-lookup"><span data-stu-id="ff5b0-118">-StorageSystem</span></span>
<span data-ttu-id="ff5b0-119">Der Name des Speichersubsystems.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="ff5b0-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="ff5b0-120">-Location</span></span>
<span data-ttu-id="ff5b0-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-121">Location of the resource.</span></span>

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

### <span data-ttu-id="ff5b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff5b0-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ff5b0-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ff5b0-124">-ResourceId</span></span>
<span data-ttu-id="ff5b0-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-125">The resource id.</span></span>

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

### <span data-ttu-id="ff5b0-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="ff5b0-126">-Filter</span></span>
<span data-ttu-id="ff5b0-127">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="ff5b0-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="ff5b0-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="ff5b0-128">-Skip</span></span>
<span data-ttu-id="ff5b0-129">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ff5b0-130">-Top</span><span class="sxs-lookup"><span data-stu-id="ff5b0-130">-Top</span></span>
<span data-ttu-id="ff5b0-131">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ff5b0-132">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ff5b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5b0-133">CommonParameters</span></span>
<span data-ttu-id="ff5b0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff5b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5b0-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5b0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5b0-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff5b0-136">INPUTS</span></span>

## <span data-ttu-id="ff5b0-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff5b0-137">OUTPUTS</span></span>

### <span data-ttu-id="ff5b0-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="ff5b0-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="ff5b0-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff5b0-139">NOTES</span></span>

## <span data-ttu-id="ff5b0-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff5b0-140">RELATED LINKS</span></span>
