---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828272"
---
# <span data-ttu-id="ad553-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="ad553-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="ad553-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad553-102">SYNOPSIS</span></span>
<span data-ttu-id="ad553-103">Gibt eine Liste aller Infrastrukturrollen Instanzen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="ad553-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="ad553-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad553-104">SYNTAX</span></span>

### <span data-ttu-id="ad553-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad553-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ad553-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="ad553-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad553-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad553-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad553-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad553-108">DESCRIPTION</span></span>
<span data-ttu-id="ad553-109">Gibt eine Liste aller Infrastrukturrollen Instanzen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="ad553-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="ad553-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad553-110">EXAMPLES</span></span>

### <span data-ttu-id="ad553-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad553-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="ad553-112">Gibt eine Liste aller Rolleninstanzen der Infrastruktur zurück.</span><span class="sxs-lookup"><span data-stu-id="ad553-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="ad553-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ad553-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="ad553-114">Gibt eine einzelne Infrastrukturrollen Instanz basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="ad553-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="ad553-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad553-115">PARAMETERS</span></span>

### <span data-ttu-id="ad553-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ad553-116">-Name</span></span>
<span data-ttu-id="ad553-117">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="ad553-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="ad553-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="ad553-118">-Location</span></span>
<span data-ttu-id="ad553-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ad553-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ad553-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad553-120">-ResourceGroupName</span></span>
<span data-ttu-id="ad553-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="ad553-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ad553-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ad553-122">-ResourceId</span></span>
<span data-ttu-id="ad553-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ad553-123">The resource id.</span></span>

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

### <span data-ttu-id="ad553-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="ad553-124">-Filter</span></span>
<span data-ttu-id="ad553-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="ad553-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="ad553-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="ad553-126">-Skip</span></span>
<span data-ttu-id="ad553-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="ad553-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ad553-128">-Top</span><span class="sxs-lookup"><span data-stu-id="ad553-128">-Top</span></span>
<span data-ttu-id="ad553-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="ad553-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ad553-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ad553-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ad553-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad553-131">CommonParameters</span></span>
<span data-ttu-id="ad553-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad553-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad553-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad553-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad553-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad553-134">INPUTS</span></span>

## <span data-ttu-id="ad553-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad553-135">OUTPUTS</span></span>

### <span data-ttu-id="ad553-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="ad553-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="ad553-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad553-137">NOTES</span></span>

## <span data-ttu-id="ad553-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad553-138">RELATED LINKS</span></span>
