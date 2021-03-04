---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: abc97b0473353a0bc71aae59386bc5b5770b730b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933011"
---
# <span data-ttu-id="72de5-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="72de5-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="72de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72de5-102">SYNOPSIS</span></span>
<span data-ttu-id="72de5-103">Erstellen Sie ein neues CosmosDB VirtualNetworkRule-Objekt(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="72de5-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="72de5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72de5-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72de5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72de5-105">DESCRIPTION</span></span>
<span data-ttu-id="72de5-106">Erstellen Sie ein neues CosmosDB VirtualNetworkRule-Objekt(PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="72de5-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="72de5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72de5-107">EXAMPLES</span></span>

### <span data-ttu-id="72de5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72de5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="72de5-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72de5-109">PARAMETERS</span></span>

### <span data-ttu-id="72de5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72de5-110">-DefaultProfile</span></span>
<span data-ttu-id="72de5-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72de5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72de5-112">-ID</span><span class="sxs-lookup"><span data-stu-id="72de5-112">-Id</span></span>
<span data-ttu-id="72de5-113">Ressourcen-ID eines Subnetzes, z. B.: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="72de5-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="72de5-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="72de5-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="72de5-115">Boolescher Wert, um anzugeben, ob eine Firewallregel erstellt werden soll, bevor der vnet-Dienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="72de5-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="72de5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72de5-116">CommonParameters</span></span>
<span data-ttu-id="72de5-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72de5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72de5-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72de5-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72de5-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72de5-119">INPUTS</span></span>

### <span data-ttu-id="72de5-120">Keine</span><span class="sxs-lookup"><span data-stu-id="72de5-120">None</span></span>

## <span data-ttu-id="72de5-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72de5-121">OUTPUTS</span></span>

### <span data-ttu-id="72de5-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="72de5-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="72de5-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="72de5-123">NOTES</span></span>

## <span data-ttu-id="72de5-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="72de5-124">RELATED LINKS</span></span>
