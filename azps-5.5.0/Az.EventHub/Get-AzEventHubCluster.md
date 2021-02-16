---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153188"
---
# <span data-ttu-id="afd7c-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="afd7c-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="afd7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="afd7c-103">Ruft die Details eines einzelnen Ereignishubclusters ab oder ruft eine Liste der Ereignishub-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="afd7c-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="afd7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afd7c-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afd7c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="afd7c-106">Das Get-AzEventHubCluster-Cmdlet gibt entweder die Details eines Ereignishubclusters oder eine Liste aller Ereignishubclusters in einer bestimmten Ressourcengruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="afd7c-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="afd7c-107">Wenn der Clustername angegeben wird, werden die Details eines einzelnen Cluster zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="afd7c-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="afd7c-108">Wenn kein Clustername angegeben wird, wird eine Liste aller Cluster in der angegebenen Ressourcengruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="afd7c-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="afd7c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afd7c-109">EXAMPLES</span></span>

### <span data-ttu-id="afd7c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afd7c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="afd7c-111">Gibt die Initialen des Cluster 'Eventhub-Cluster-5557' aus der Ressourcengruppe 'RSG-Cluster27651' zurück.</span><span class="sxs-lookup"><span data-stu-id="afd7c-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="afd7c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afd7c-112">PARAMETERS</span></span>

### <span data-ttu-id="afd7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd7c-113">-DefaultProfile</span></span>
<span data-ttu-id="afd7c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afd7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afd7c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="afd7c-115">-Name</span></span>
<span data-ttu-id="afd7c-116">Clustername</span><span class="sxs-lookup"><span data-stu-id="afd7c-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="afd7c-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="afd7c-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd7c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd7c-119">CommonParameters</span></span>
<span data-ttu-id="afd7c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd7c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd7c-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afd7c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd7c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afd7c-122">INPUTS</span></span>

### <span data-ttu-id="afd7c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="afd7c-123">System.String</span></span>

## <span data-ttu-id="afd7c-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afd7c-124">OUTPUTS</span></span>

### <span data-ttu-id="afd7c-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="afd7c-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="afd7c-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="afd7c-126">NOTES</span></span>

## <span data-ttu-id="afd7c-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="afd7c-127">RELATED LINKS</span></span>
