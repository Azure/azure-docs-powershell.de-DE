---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995100"
---
# <span data-ttu-id="6be76-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="6be76-101">Search-AzGraph</span></span>

## <span data-ttu-id="6be76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6be76-102">SYNOPSIS</span></span>
<span data-ttu-id="6be76-103">Fragt die Ressourcen ab, die vom Azure Resource Manager verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6be76-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="6be76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6be76-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6be76-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6be76-105">DESCRIPTION</span></span>
<span data-ttu-id="6be76-106">Weitere Informationen zur Abfragesyntax finden Sie hier: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="6be76-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="6be76-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6be76-107">EXAMPLES</span></span>

### <span data-ttu-id="6be76-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6be76-108">Example 1</span></span>
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

<span data-ttu-id="6be76-109">Einfache Ressourcenabfrage, die eine Teilmenge von Ressourcenfeldern anfordert.</span><span class="sxs-lookup"><span data-stu-id="6be76-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="6be76-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6be76-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="6be76-111">Eine komplexe Abfrage zu Ressourcen mit Feldauswahl, Filterung und Zusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="6be76-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="6be76-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6be76-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="6be76-113">Eine Abfrage mit allen virtuellen Computern, die keine verwalteten Datenträger verwenden und Anzeige Namen für Abonnements enthalten.</span><span class="sxs-lookup"><span data-stu-id="6be76-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="6be76-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="6be76-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="6be76-115">Eine Abfrage, die die Anzahl der Ressourcen nach Anzeige Namen für Mandanten und Abonnements anzeigt.</span><span class="sxs-lookup"><span data-stu-id="6be76-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="6be76-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6be76-116">PARAMETERS</span></span>

### <span data-ttu-id="6be76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be76-117">-DefaultProfile</span></span>
<span data-ttu-id="6be76-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6be76-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be76-119">-Query</span><span class="sxs-lookup"><span data-stu-id="6be76-119">-Query</span></span>
<span data-ttu-id="6be76-120">Ressourcen Diagramm Abfrage</span><span class="sxs-lookup"><span data-stu-id="6be76-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="6be76-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="6be76-121">-Subscription</span></span>
<span data-ttu-id="6be76-122">Abonnements, für die eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6be76-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="6be76-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="6be76-123">-Skip</span></span>
<span data-ttu-id="6be76-124">Ignoriert die ersten N Objekte und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="6be76-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="6be76-125">-First</span><span class="sxs-lookup"><span data-stu-id="6be76-125">-First</span></span>
<span data-ttu-id="6be76-126">Die maximale Anzahl von Objekten, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6be76-126">The maximum number of objects to return.</span></span> <span data-ttu-id="6be76-127">Zulässige Werte: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="6be76-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="6be76-128">Der Standardwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="6be76-128">Default value is 100.</span></span>

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

### <span data-ttu-id="6be76-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be76-129">CommonParameters</span></span>
<span data-ttu-id="6be76-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be76-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be76-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6be76-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be76-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6be76-132">INPUTS</span></span>

### <span data-ttu-id="6be76-133">Keine</span><span class="sxs-lookup"><span data-stu-id="6be76-133">None</span></span>

## <span data-ttu-id="6be76-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6be76-134">OUTPUTS</span></span>

### <span data-ttu-id="6be76-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6be76-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6be76-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="6be76-136">NOTES</span></span>

## <span data-ttu-id="6be76-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6be76-137">RELATED LINKS</span></span>
