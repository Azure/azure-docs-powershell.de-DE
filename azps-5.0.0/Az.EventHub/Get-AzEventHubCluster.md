---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178904"
---
# <span data-ttu-id="df034-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="df034-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="df034-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df034-102">SYNOPSIS</span></span>
<span data-ttu-id="df034-103">Ruft die Details eines einzelnen Ereignis-Hub-Clusters ab oder ruft eine Liste mit Ereignis-Hub-Clustern ab.</span><span class="sxs-lookup"><span data-stu-id="df034-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="df034-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df034-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df034-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df034-105">DESCRIPTION</span></span>
<span data-ttu-id="df034-106">Das Get-AzEventHubCluster-Cmdlet gibt entweder die Details eines Ereignis-Hub-Clusters oder eine Liste aller Ereignis-Hub-Cluster in der angegebenen Ressourcengruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="df034-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="df034-107">Wenn der Clustername angegeben wird, werden die Details eines einzelnen Clusters zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df034-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="df034-108">Wenn kein Clustername angegeben wird, wird eine Liste aller Cluster in der angegebenen Ressourcengruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="df034-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="df034-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df034-109">EXAMPLES</span></span>

### <span data-ttu-id="df034-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df034-110">Example 1</span></span>
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

<span data-ttu-id="df034-111">Gibt den DETIALS des Clusters ' Eventhub-Cluster-5557 ' aus der Ressourcengruppe ' RSG-Cluster27651 ' zurück.</span><span class="sxs-lookup"><span data-stu-id="df034-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="df034-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="df034-112">PARAMETERS</span></span>

### <span data-ttu-id="df034-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df034-113">-DefaultProfile</span></span>
<span data-ttu-id="df034-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df034-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df034-115">-Name</span><span class="sxs-lookup"><span data-stu-id="df034-115">-Name</span></span>
<span data-ttu-id="df034-116">Cluster Name</span><span class="sxs-lookup"><span data-stu-id="df034-116">Cluster Name</span></span>

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

### <span data-ttu-id="df034-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df034-117">-ResourceGroupName</span></span>
<span data-ttu-id="df034-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="df034-118">Resource Group Name</span></span>

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

### <span data-ttu-id="df034-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df034-119">CommonParameters</span></span>
<span data-ttu-id="df034-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df034-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df034-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df034-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df034-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df034-122">INPUTS</span></span>

### <span data-ttu-id="df034-123">System. String</span><span class="sxs-lookup"><span data-stu-id="df034-123">System.String</span></span>

## <span data-ttu-id="df034-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df034-124">OUTPUTS</span></span>

### <span data-ttu-id="df034-125">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="df034-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="df034-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="df034-126">NOTES</span></span>

## <span data-ttu-id="df034-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df034-127">RELATED LINKS</span></span>
