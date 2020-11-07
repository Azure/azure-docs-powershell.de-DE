---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828259"
---
# <span data-ttu-id="14443-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="14443-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="14443-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14443-102">SYNOPSIS</span></span>
<span data-ttu-id="14443-103">Gibt eine Liste aller logischen Netzwerke an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="14443-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="14443-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14443-104">SYNTAX</span></span>

### <span data-ttu-id="14443-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="14443-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="14443-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="14443-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="14443-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="14443-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="14443-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14443-108">DESCRIPTION</span></span>
<span data-ttu-id="14443-109">Gibt eine Liste aller logischen Netzwerke an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="14443-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="14443-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14443-110">EXAMPLES</span></span>

### <span data-ttu-id="14443-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14443-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="14443-112">Abrufen aller logischen Netzwerke an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="14443-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="14443-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="14443-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="14443-114">Abrufen bestimmter logischer Netzwerke an einem Speicherort, der auf einem Namen basiert.</span><span class="sxs-lookup"><span data-stu-id="14443-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="14443-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="14443-115">PARAMETERS</span></span>

### <span data-ttu-id="14443-116">-Name</span><span class="sxs-lookup"><span data-stu-id="14443-116">-Name</span></span>
<span data-ttu-id="14443-117">Der Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="14443-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="14443-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="14443-118">-Location</span></span>
<span data-ttu-id="14443-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="14443-119">Location of the resource.</span></span>

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

### <span data-ttu-id="14443-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14443-120">-ResourceGroupName</span></span>
<span data-ttu-id="14443-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="14443-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="14443-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="14443-122">-ResourceId</span></span>
<span data-ttu-id="14443-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="14443-123">The resource id.</span></span>

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

### <span data-ttu-id="14443-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="14443-124">-Filter</span></span>
<span data-ttu-id="14443-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="14443-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="14443-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="14443-126">-Skip</span></span>
<span data-ttu-id="14443-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="14443-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="14443-128">-Top</span><span class="sxs-lookup"><span data-stu-id="14443-128">-Top</span></span>
<span data-ttu-id="14443-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="14443-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="14443-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="14443-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="14443-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14443-131">CommonParameters</span></span>
<span data-ttu-id="14443-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14443-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14443-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14443-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14443-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14443-134">INPUTS</span></span>

## <span data-ttu-id="14443-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14443-135">OUTPUTS</span></span>

### <span data-ttu-id="14443-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="14443-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="14443-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="14443-137">NOTES</span></span>

## <span data-ttu-id="14443-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14443-138">RELATED LINKS</span></span>
