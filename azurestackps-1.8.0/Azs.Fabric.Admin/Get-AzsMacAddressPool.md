---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827575"
---
# <span data-ttu-id="371ac-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="371ac-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="371ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="371ac-102">SYNOPSIS</span></span>
<span data-ttu-id="371ac-103">Gibt eine Liste aller Mac-Adresspools an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="371ac-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="371ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="371ac-104">SYNTAX</span></span>

### <span data-ttu-id="371ac-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="371ac-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="371ac-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="371ac-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="371ac-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="371ac-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="371ac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="371ac-108">DESCRIPTION</span></span>
<span data-ttu-id="371ac-109">Gibt eine Liste aller Mac-Adresspools an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="371ac-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="371ac-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="371ac-110">EXAMPLES</span></span>

### <span data-ttu-id="371ac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="371ac-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="371ac-112">Abrufen aller Mac-Adresspools an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="371ac-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="371ac-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="371ac-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="371ac-114">Abrufen eines bestimmten Mac-Adresspools an einem Speicherort, der auf dem Namen basiert.</span><span class="sxs-lookup"><span data-stu-id="371ac-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="371ac-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="371ac-115">PARAMETERS</span></span>

### <span data-ttu-id="371ac-116">-Name</span><span class="sxs-lookup"><span data-stu-id="371ac-116">-Name</span></span>
<span data-ttu-id="371ac-117">Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="371ac-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="371ac-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="371ac-118">-Location</span></span>
<span data-ttu-id="371ac-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="371ac-119">Location of the resource.</span></span>

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

### <span data-ttu-id="371ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="371ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="371ac-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="371ac-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="371ac-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="371ac-122">-ResourceId</span></span>
<span data-ttu-id="371ac-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="371ac-123">The resource id.</span></span>

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

### <span data-ttu-id="371ac-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="371ac-124">-Filter</span></span>
<span data-ttu-id="371ac-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="371ac-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="371ac-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="371ac-126">-Skip</span></span>
<span data-ttu-id="371ac-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="371ac-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="371ac-128">-Top</span><span class="sxs-lookup"><span data-stu-id="371ac-128">-Top</span></span>
<span data-ttu-id="371ac-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="371ac-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="371ac-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="371ac-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="371ac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371ac-131">CommonParameters</span></span>
<span data-ttu-id="371ac-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="371ac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371ac-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371ac-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371ac-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="371ac-134">INPUTS</span></span>

## <span data-ttu-id="371ac-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="371ac-135">OUTPUTS</span></span>

### <span data-ttu-id="371ac-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="371ac-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="371ac-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="371ac-137">NOTES</span></span>

## <span data-ttu-id="371ac-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="371ac-138">RELATED LINKS</span></span>
