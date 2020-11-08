---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003834"
---
# <span data-ttu-id="aee27-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aee27-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="aee27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aee27-102">SYNOPSIS</span></span>
<span data-ttu-id="aee27-103">Erstellen Sie ein neues CosmosDB-VirtualNetworkRule-Objekt (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="aee27-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="aee27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aee27-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aee27-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aee27-105">DESCRIPTION</span></span>
<span data-ttu-id="aee27-106">Erstellen Sie ein neues CosmosDB-VirtualNetworkRule-Objekt (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="aee27-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="aee27-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aee27-107">EXAMPLES</span></span>

### <span data-ttu-id="aee27-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aee27-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="aee27-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aee27-109">PARAMETERS</span></span>

### <span data-ttu-id="aee27-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee27-110">-DefaultProfile</span></span>
<span data-ttu-id="aee27-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aee27-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aee27-112">-ID</span><span class="sxs-lookup"><span data-stu-id="aee27-112">-Id</span></span>
<span data-ttu-id="aee27-113">Ressourcen-ID eines Subnets, beispielsweise:/Subscriptions/{SubscriptionId}/resourceGroups/{GroupName}/Providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/Subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="aee27-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="aee27-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="aee27-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="aee27-115">Boolescher Wert, der angibt, ob eine Firewall-Regel erstellt werden soll, bevor das virtuelle Netzwerk den vnet-Dienstendpunkt aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="aee27-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="aee27-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee27-116">CommonParameters</span></span>
<span data-ttu-id="aee27-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aee27-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee27-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aee27-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee27-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aee27-119">INPUTS</span></span>

### <span data-ttu-id="aee27-120">Keine</span><span class="sxs-lookup"><span data-stu-id="aee27-120">None</span></span>

## <span data-ttu-id="aee27-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aee27-121">OUTPUTS</span></span>

### <span data-ttu-id="aee27-122">Microsoft. Azure. Commands. CosmosDB. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aee27-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="aee27-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="aee27-123">NOTES</span></span>

## <span data-ttu-id="aee27-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aee27-124">RELATED LINKS</span></span>
