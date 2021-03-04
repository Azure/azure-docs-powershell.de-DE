---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e96d4fa13dc1b479c37b56cb3887b6d519df24f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943625"
---
# <span data-ttu-id="f3cca-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="f3cca-101">Search-AzGraph</span></span>

## <span data-ttu-id="f3cca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3cca-102">SYNOPSIS</span></span>
<span data-ttu-id="f3cca-103">Fragt die von Azure Resource Manager verwalteten Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="f3cca-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="f3cca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3cca-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3cca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3cca-105">DESCRIPTION</span></span>
<span data-ttu-id="f3cca-106">Weitere Informationen zur Abfragesyntax finden Sie hier: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="f3cca-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="f3cca-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3cca-107">EXAMPLES</span></span>

### <span data-ttu-id="f3cca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3cca-108">Example 1</span></span>
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

<span data-ttu-id="f3cca-109">Einfache Ressourcenabfrage, die eine Teilmenge von Ressourcenfeldern anfordert.</span><span class="sxs-lookup"><span data-stu-id="f3cca-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="f3cca-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f3cca-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="f3cca-111">Eine komplexe Abfrage zu Ressourcen mit Feldauswahl, Filterung und Zusammenfassung.</span><span class="sxs-lookup"><span data-stu-id="f3cca-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="f3cca-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f3cca-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="f3cca-113">Eine Abfrage mit allen virtuellen Computern, die keine verwalteten Datenträger verwenden und Abonnementanzeigenamen enthält.</span><span class="sxs-lookup"><span data-stu-id="f3cca-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="f3cca-114">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f3cca-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="f3cca-115">Eine Abfrage mit der Anzahl der Ressourcen nach Mandanten- und Abonnementanzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="f3cca-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="f3cca-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3cca-116">PARAMETERS</span></span>

### <span data-ttu-id="f3cca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3cca-117">-DefaultProfile</span></span>
<span data-ttu-id="f3cca-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3cca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3cca-119">-Query</span><span class="sxs-lookup"><span data-stu-id="f3cca-119">-Query</span></span>
<span data-ttu-id="f3cca-120">Ressourcendiagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="f3cca-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="f3cca-121">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3cca-121">-Subscription</span></span>
<span data-ttu-id="f3cca-122">Abonnements zum Ausführen von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="f3cca-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="f3cca-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="f3cca-123">-Skip</span></span>
<span data-ttu-id="f3cca-124">Ignoriert die ersten N-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="f3cca-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f3cca-125">-First</span><span class="sxs-lookup"><span data-stu-id="f3cca-125">-First</span></span>
<span data-ttu-id="f3cca-126">Die maximale Anzahl von Zurücksennungsobjekten.</span><span class="sxs-lookup"><span data-stu-id="f3cca-126">The maximum number of objects to return.</span></span> <span data-ttu-id="f3cca-127">Zulässige Werte: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="f3cca-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="f3cca-128">Der Standardwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="f3cca-128">Default value is 100.</span></span>

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

### <span data-ttu-id="f3cca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3cca-129">CommonParameters</span></span>
<span data-ttu-id="f3cca-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3cca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3cca-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3cca-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3cca-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3cca-132">INPUTS</span></span>

### <span data-ttu-id="f3cca-133">Keine</span><span class="sxs-lookup"><span data-stu-id="f3cca-133">None</span></span>

## <span data-ttu-id="f3cca-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3cca-134">OUTPUTS</span></span>

### <span data-ttu-id="f3cca-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f3cca-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f3cca-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3cca-136">NOTES</span></span>

## <span data-ttu-id="f3cca-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3cca-137">RELATED LINKS</span></span>
