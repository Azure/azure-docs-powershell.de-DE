---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299194"
---
# <span data-ttu-id="bf1ca-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bf1ca-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="bf1ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1ca-103">Erstellen Sie ein neues CosmosDB-VirtualNetworkRule-Objekt (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="bf1ca-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="bf1ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1ca-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf1ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1ca-106">Erstellen Sie ein neues CosmosDB-VirtualNetworkRule-Objekt (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="bf1ca-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="bf1ca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="bf1ca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf1ca-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="bf1ca-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf1ca-109">PARAMETERS</span></span>

### <span data-ttu-id="bf1ca-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1ca-110">-DefaultProfile</span></span>
<span data-ttu-id="bf1ca-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf1ca-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1ca-112">-ID</span><span class="sxs-lookup"><span data-stu-id="bf1ca-112">-Id</span></span>
<span data-ttu-id="bf1ca-113">Ressourcen-ID eines Subnets, beispielsweise:/Subscriptions/{SubscriptionId}/resourceGroups/{GroupName}/Providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/Subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="bf1ca-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1ca-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bf1ca-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="bf1ca-115">Boolescher Wert, der angibt, ob eine Firewall-Regel erstellt werden soll, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="bf1ca-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1ca-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1ca-116">CommonParameters</span></span>
<span data-ttu-id="bf1ca-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1ca-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1ca-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf1ca-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1ca-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf1ca-119">INPUTS</span></span>

### <span data-ttu-id="bf1ca-120">Keine</span><span class="sxs-lookup"><span data-stu-id="bf1ca-120">None</span></span>

## <span data-ttu-id="bf1ca-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf1ca-121">OUTPUTS</span></span>

### <span data-ttu-id="bf1ca-122">Microsoft. Azure. Commands. CosmosDB. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bf1ca-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="bf1ca-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf1ca-123">NOTES</span></span>

## <span data-ttu-id="bf1ca-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf1ca-124">RELATED LINKS</span></span>
