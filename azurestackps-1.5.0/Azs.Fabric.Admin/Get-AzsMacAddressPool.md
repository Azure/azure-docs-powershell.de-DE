---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475625"
---
# <span data-ttu-id="e4a46-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="e4a46-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="e4a46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4a46-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a46-103">Gibt eine Liste aller Mac-Adresspools an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="e4a46-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="e4a46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4a46-104">SYNTAX</span></span>

### <span data-ttu-id="e4a46-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4a46-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e4a46-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e4a46-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e4a46-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4a46-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e4a46-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4a46-108">DESCRIPTION</span></span>
<span data-ttu-id="e4a46-109">Gibt eine Liste aller Mac-Adresspools an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="e4a46-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="e4a46-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4a46-110">EXAMPLES</span></span>

### <span data-ttu-id="e4a46-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4a46-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="e4a46-112">Abrufen aller Mac-Adresspools an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="e4a46-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="e4a46-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4a46-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="e4a46-114">Abrufen eines bestimmten Mac-Adresspools an einem Speicherort, der auf dem Namen basiert.</span><span class="sxs-lookup"><span data-stu-id="e4a46-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="e4a46-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4a46-115">PARAMETERS</span></span>

### <span data-ttu-id="e4a46-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="e4a46-116">-Filter</span></span>
<span data-ttu-id="e4a46-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="e4a46-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e4a46-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="e4a46-118">-Location</span></span>
<span data-ttu-id="e4a46-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="e4a46-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e4a46-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e4a46-120">-Name</span></span>
<span data-ttu-id="e4a46-121">Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="e4a46-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="e4a46-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a46-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4a46-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="e4a46-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e4a46-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e4a46-124">-ResourceId</span></span>
<span data-ttu-id="e4a46-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e4a46-125">The resource id.</span></span>

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

### <span data-ttu-id="e4a46-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="e4a46-126">-Skip</span></span>
<span data-ttu-id="e4a46-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="e4a46-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e4a46-128">-Top</span><span class="sxs-lookup"><span data-stu-id="e4a46-128">-Top</span></span>
<span data-ttu-id="e4a46-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="e4a46-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e4a46-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="e4a46-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e4a46-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a46-131">CommonParameters</span></span>
<span data-ttu-id="e4a46-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4a46-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a46-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a46-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a46-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4a46-134">INPUTS</span></span>

## <span data-ttu-id="e4a46-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4a46-135">OUTPUTS</span></span>

### <span data-ttu-id="e4a46-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="e4a46-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="e4a46-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4a46-137">NOTES</span></span>

## <span data-ttu-id="e4a46-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4a46-138">RELATED LINKS</span></span>

