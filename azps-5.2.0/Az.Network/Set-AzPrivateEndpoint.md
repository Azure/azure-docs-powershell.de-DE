---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300563"
---
# <span data-ttu-id="c7567-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7567-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="c7567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7567-102">SYNOPSIS</span></span>
<span data-ttu-id="c7567-103">Aktualisiert einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c7567-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="c7567-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7567-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7567-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7567-105">DESCRIPTION</span></span>
<span data-ttu-id="c7567-106">Das **Set-AzPrivateEndpoint-Cmdlet** aktualisiert einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c7567-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="c7567-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7567-107">EXAMPLES</span></span>

### <span data-ttu-id="c7567-108">1: Erstellt einen privaten Endpunkt und ersetzt eines seiner Subnetze durch einen anderen.</span><span class="sxs-lookup"><span data-stu-id="c7567-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="c7567-109">In diesem Beispiel wird ein privater Endpunkt mit einem Subnetz erstellt, der dann von der Speicherdarstellung des virtuellen Netzwerks in ein anderes Subnetz ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c7567-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="c7567-110">Das Set-PrivateEndpoint cmdlet wird dann verwendet, um den geänderten privaten Endpunktstatus auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c7567-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="c7567-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7567-111">PARAMETERS</span></span>

### <span data-ttu-id="c7567-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7567-112">-AsJob</span></span>
<span data-ttu-id="c7567-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c7567-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7567-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7567-114">-DefaultProfile</span></span>
<span data-ttu-id="c7567-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7567-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7567-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7567-116">-PrivateEndpoint</span></span>
<span data-ttu-id="c7567-117">Gibt ein privates Endpunktobjekt an, das den Zustand darstellt, auf den der private Endpunkt festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7567-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7567-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7567-118">CommonParameters</span></span>
<span data-ttu-id="c7567-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7567-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7567-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7567-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7567-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7567-121">INPUTS</span></span>

### <span data-ttu-id="c7567-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7567-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="c7567-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7567-123">OUTPUTS</span></span>

### <span data-ttu-id="c7567-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7567-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="c7567-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c7567-125">NOTES</span></span>

## <span data-ttu-id="c7567-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c7567-126">RELATED LINKS</span></span>

[<span data-ttu-id="c7567-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7567-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="c7567-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7567-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="c7567-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7567-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


