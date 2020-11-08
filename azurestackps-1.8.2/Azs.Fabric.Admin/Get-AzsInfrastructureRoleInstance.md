---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007303"
---
# <span data-ttu-id="5a478-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="5a478-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="5a478-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a478-102">SYNOPSIS</span></span>
<span data-ttu-id="5a478-103">Gibt eine Liste aller Infrastrukturrollen Instanzen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5a478-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="5a478-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a478-104">SYNTAX</span></span>

### <span data-ttu-id="5a478-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a478-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5a478-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5a478-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a478-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a478-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5a478-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a478-108">DESCRIPTION</span></span>
<span data-ttu-id="5a478-109">Gibt eine Liste aller Infrastrukturrollen Instanzen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5a478-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="5a478-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a478-110">EXAMPLES</span></span>

### <span data-ttu-id="5a478-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a478-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="5a478-112">Gibt eine Liste aller Rolleninstanzen der Infrastruktur zurück.</span><span class="sxs-lookup"><span data-stu-id="5a478-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="5a478-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5a478-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="5a478-114">Gibt eine einzelne Infrastrukturrollen Instanz basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="5a478-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="5a478-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a478-115">PARAMETERS</span></span>

### <span data-ttu-id="5a478-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a478-116">-Name</span></span>
<span data-ttu-id="5a478-117">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="5a478-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="5a478-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="5a478-118">-Location</span></span>
<span data-ttu-id="5a478-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5a478-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5a478-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a478-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a478-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="5a478-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5a478-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5a478-122">-ResourceId</span></span>
<span data-ttu-id="5a478-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5a478-123">The resource id.</span></span>

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

### <span data-ttu-id="5a478-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="5a478-124">-Filter</span></span>
<span data-ttu-id="5a478-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="5a478-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="5a478-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="5a478-126">-Skip</span></span>
<span data-ttu-id="5a478-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="5a478-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5a478-128">-Top</span><span class="sxs-lookup"><span data-stu-id="5a478-128">-Top</span></span>
<span data-ttu-id="5a478-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="5a478-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5a478-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="5a478-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5a478-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a478-131">CommonParameters</span></span>
<span data-ttu-id="5a478-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a478-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a478-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a478-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a478-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a478-134">INPUTS</span></span>

## <span data-ttu-id="5a478-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a478-135">OUTPUTS</span></span>

### <span data-ttu-id="5a478-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="5a478-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="5a478-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a478-137">NOTES</span></span>

## <span data-ttu-id="5a478-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a478-138">RELATED LINKS</span></span>
