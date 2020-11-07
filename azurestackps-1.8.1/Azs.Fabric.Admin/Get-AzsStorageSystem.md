---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828227"
---
# <span data-ttu-id="d6e46-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="d6e46-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="d6e46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6e46-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e46-103">Gibt eine Liste aller Speichersubsysteme für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="d6e46-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="d6e46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6e46-104">SYNTAX</span></span>

### <span data-ttu-id="d6e46-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6e46-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d6e46-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d6e46-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d6e46-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6e46-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d6e46-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6e46-108">DESCRIPTION</span></span>
<span data-ttu-id="d6e46-109">Gibt eine Liste aller Speichersubsysteme für einen Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="d6e46-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="d6e46-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6e46-110">EXAMPLES</span></span>

### <span data-ttu-id="d6e46-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6e46-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="d6e46-112">Abrufen aller Speichersubsysteme von einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="d6e46-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="d6e46-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d6e46-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="d6e46-114">Rufen Sie ein Speichersubsystem ab, das einen Speicherort und einen Namen erhält.</span><span class="sxs-lookup"><span data-stu-id="d6e46-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="d6e46-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6e46-115">PARAMETERS</span></span>

### <span data-ttu-id="d6e46-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d6e46-116">-Name</span></span>
<span data-ttu-id="d6e46-117">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="d6e46-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d6e46-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="d6e46-118">-Location</span></span>
<span data-ttu-id="d6e46-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d6e46-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d6e46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6e46-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6e46-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="d6e46-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d6e46-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d6e46-122">-ResourceId</span></span>
<span data-ttu-id="d6e46-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d6e46-123">The resource id.</span></span>

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

### <span data-ttu-id="d6e46-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="d6e46-124">-Filter</span></span>
<span data-ttu-id="d6e46-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="d6e46-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="d6e46-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="d6e46-126">-Skip</span></span>
<span data-ttu-id="d6e46-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="d6e46-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d6e46-128">-Top</span><span class="sxs-lookup"><span data-stu-id="d6e46-128">-Top</span></span>
<span data-ttu-id="d6e46-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="d6e46-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d6e46-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="d6e46-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d6e46-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e46-131">CommonParameters</span></span>
<span data-ttu-id="d6e46-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6e46-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e46-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6e46-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e46-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6e46-134">INPUTS</span></span>

## <span data-ttu-id="d6e46-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6e46-135">OUTPUTS</span></span>

### <span data-ttu-id="d6e46-136">Microsoft. AzureStack. Management. Fabric. admin. Models. Speichersystem</span><span class="sxs-lookup"><span data-stu-id="d6e46-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="d6e46-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6e46-137">NOTES</span></span>

## <span data-ttu-id="d6e46-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6e46-138">RELATED LINKS</span></span>
