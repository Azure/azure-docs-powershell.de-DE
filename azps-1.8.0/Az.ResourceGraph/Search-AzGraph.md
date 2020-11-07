---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: 5a9a47ff6f4a329d3e48ec54df85ade3be5ae84d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659672"
---
# <span data-ttu-id="a0a29-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="a0a29-101">Search-AzGraph</span></span>

## <span data-ttu-id="a0a29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0a29-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a29-103">Fragt die Ressourcen ab, die vom Azure Resource Manager verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="a0a29-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="a0a29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0a29-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0a29-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0a29-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a29-106">Weitere Informationen zur Abfragesyntax finden Sie hier: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="a0a29-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="a0a29-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0a29-107">EXAMPLES</span></span>

### <span data-ttu-id="a0a29-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0a29-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="a0a29-109">Einfache Ressourcenabfrage, die eine Teilmenge von Ressourcenfeldern anfordert.</span><span class="sxs-lookup"><span data-stu-id="a0a29-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="a0a29-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a0a29-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="a0a29-111">Eine komplexe Abfrage zu Ressourcen mit Feldauswahl, Filterung und Zusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="a0a29-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="a0a29-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0a29-112">PARAMETERS</span></span>

### <span data-ttu-id="a0a29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a29-113">-DefaultProfile</span></span>
<span data-ttu-id="a0a29-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0a29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a29-115">-Query</span><span class="sxs-lookup"><span data-stu-id="a0a29-115">-Query</span></span>
<span data-ttu-id="a0a29-116">Ressourcen Diagramm Abfrage</span><span class="sxs-lookup"><span data-stu-id="a0a29-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a29-117">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0a29-117">-Subscription</span></span>
<span data-ttu-id="a0a29-118">Abonnements, für die eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0a29-118">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a29-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="a0a29-119">-Skip</span></span>
<span data-ttu-id="a0a29-120">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="a0a29-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a29-121">-First</span><span class="sxs-lookup"><span data-stu-id="a0a29-121">-First</span></span>
<span data-ttu-id="a0a29-122">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a0a29-122">The maximum number of objects to return.</span></span> <span data-ttu-id="a0a29-123">Zulässige Werte: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="a0a29-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="a0a29-124">Der Standardwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="a0a29-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a29-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a29-125">CommonParameters</span></span>
<span data-ttu-id="a0a29-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a29-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a29-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a29-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a29-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0a29-128">INPUTS</span></span>

### <span data-ttu-id="a0a29-129">Keine</span><span class="sxs-lookup"><span data-stu-id="a0a29-129">None</span></span>

## <span data-ttu-id="a0a29-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0a29-130">OUTPUTS</span></span>

### <span data-ttu-id="a0a29-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a0a29-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a0a29-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0a29-132">NOTES</span></span>

## <span data-ttu-id="a0a29-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0a29-133">RELATED LINKS</span></span>
