---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148532"
---
# <span data-ttu-id="4d48d-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4d48d-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="4d48d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d48d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d48d-103">Erstellen Sie ein neues VirtuelleNetworkRule-Objekt (PSVirtualNetworkRule) aus.</span><span class="sxs-lookup"><span data-stu-id="4d48d-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="4d48d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d48d-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d48d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d48d-105">DESCRIPTION</span></span>
<span data-ttu-id="4d48d-106">Erstellen Sie ein neues VirtuelleNetworkRule-Objekt (PSVirtualNetworkRule) aus.</span><span class="sxs-lookup"><span data-stu-id="4d48d-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="4d48d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d48d-107">EXAMPLES</span></span>

### <span data-ttu-id="4d48d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d48d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="4d48d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d48d-109">PARAMETERS</span></span>

### <span data-ttu-id="4d48d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d48d-110">-DefaultProfile</span></span>
<span data-ttu-id="4d48d-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d48d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d48d-112">-ID</span><span class="sxs-lookup"><span data-stu-id="4d48d-112">-Id</span></span>
<span data-ttu-id="4d48d-113">Ressourcen-ID eines Subnetzes, z. B.: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="4d48d-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="4d48d-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d48d-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="4d48d-115">Boolesch, um anzugeben, ob eine Firewallregel erstellt werden soll, bevor der vnetdienstendpunkt im virtuellen Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4d48d-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="4d48d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d48d-116">CommonParameters</span></span>
<span data-ttu-id="4d48d-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d48d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d48d-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d48d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d48d-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d48d-119">INPUTS</span></span>

### <span data-ttu-id="4d48d-120">Keine</span><span class="sxs-lookup"><span data-stu-id="4d48d-120">None</span></span>

## <span data-ttu-id="4d48d-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d48d-121">OUTPUTS</span></span>

### <span data-ttu-id="4d48d-122">Microsoft.Azure.Commands.UmsDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4d48d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="4d48d-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d48d-123">NOTES</span></span>

## <span data-ttu-id="4d48d-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d48d-124">RELATED LINKS</span></span>
