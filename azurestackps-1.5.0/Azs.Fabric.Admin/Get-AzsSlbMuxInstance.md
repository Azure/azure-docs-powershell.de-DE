---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661900"
---
# <span data-ttu-id="29105-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="29105-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="29105-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29105-102">SYNOPSIS</span></span>
<span data-ttu-id="29105-103">Gibt eine Liste aller Instanzen des Software-Lastenausgleichs an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="29105-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="29105-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29105-104">SYNTAX</span></span>

### <span data-ttu-id="29105-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="29105-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="29105-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="29105-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="29105-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="29105-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="29105-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29105-108">DESCRIPTION</span></span>
<span data-ttu-id="29105-109">Gibt eine Liste aller Instanzen des Software-Lastenausgleichs an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="29105-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="29105-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29105-110">EXAMPLES</span></span>

### <span data-ttu-id="29105-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="29105-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="29105-112">Laden Sie die gesamte Software Load Balancer-Multiplexer-Instanz an einem Speicherort herunter.</span><span class="sxs-lookup"><span data-stu-id="29105-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="29105-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="29105-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="29105-114">Besorgen Sie sich eine bestimmte Multiplexer-Instanz des Software-Lastenausgleichs an einem Speicherort, der einen Namen erhält.</span><span class="sxs-lookup"><span data-stu-id="29105-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="29105-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="29105-115">PARAMETERS</span></span>

### <span data-ttu-id="29105-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="29105-116">-Filter</span></span>
<span data-ttu-id="29105-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="29105-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="29105-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="29105-118">-Location</span></span>
<span data-ttu-id="29105-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="29105-119">Location of the resource.</span></span>

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

### <span data-ttu-id="29105-120">-Name</span><span class="sxs-lookup"><span data-stu-id="29105-120">-Name</span></span>
<span data-ttu-id="29105-121">Der Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="29105-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="29105-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29105-122">-ResourceGroupName</span></span>
<span data-ttu-id="29105-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="29105-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="29105-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="29105-124">-ResourceId</span></span>
<span data-ttu-id="29105-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="29105-125">The resource id.</span></span>

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

### <span data-ttu-id="29105-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="29105-126">-Skip</span></span>
<span data-ttu-id="29105-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="29105-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="29105-128">-Top</span><span class="sxs-lookup"><span data-stu-id="29105-128">-Top</span></span>
<span data-ttu-id="29105-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="29105-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="29105-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="29105-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="29105-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29105-131">CommonParameters</span></span>
<span data-ttu-id="29105-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29105-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29105-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29105-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29105-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29105-134">INPUTS</span></span>

## <span data-ttu-id="29105-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29105-135">OUTPUTS</span></span>

### <span data-ttu-id="29105-136">Microsoft. AzureStack. Management. Fabric. admin. Models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="29105-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="29105-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="29105-137">NOTES</span></span>

## <span data-ttu-id="29105-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29105-138">RELATED LINKS</span></span>

