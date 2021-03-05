---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950699"
---
# <span data-ttu-id="8e086-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e086-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="8e086-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e086-102">SYNOPSIS</span></span>
<span data-ttu-id="8e086-103">Aktualisiert einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8e086-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="8e086-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e086-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e086-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e086-105">DESCRIPTION</span></span>
<span data-ttu-id="8e086-106">Das **Set-AzPrivateEndpoint-Cmdlet** aktualisiert einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8e086-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="8e086-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e086-107">EXAMPLES</span></span>

### <span data-ttu-id="8e086-108">1: Erstellt einen privaten Endpunkt und ersetzt eines seiner Subnetze durch einen anderen.</span><span class="sxs-lookup"><span data-stu-id="8e086-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="8e086-109">In diesem Beispiel wird ein privater Endpunkt mit einem Subnetz erstellt, der dann aus der Speicherdarstellung des virtuellen Netzwerks in ein anderes Subnetz ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8e086-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="8e086-110">Das Set-PrivateEndpoint-Cmdlet wird dann verwendet, um den geänderten privaten Endpunktzustand auf der Dienstseite zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="8e086-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="8e086-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e086-111">PARAMETERS</span></span>

### <span data-ttu-id="8e086-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e086-112">-AsJob</span></span>
<span data-ttu-id="8e086-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8e086-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e086-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e086-114">-DefaultProfile</span></span>
<span data-ttu-id="8e086-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e086-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e086-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e086-116">-PrivateEndpoint</span></span>
<span data-ttu-id="8e086-117">Gibt ein privates Endpunktobjekt an, das den Zustand darstellt, auf den der private Endpunkt festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e086-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="8e086-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e086-118">CommonParameters</span></span>
<span data-ttu-id="8e086-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e086-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e086-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e086-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e086-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e086-121">INPUTS</span></span>

### <span data-ttu-id="8e086-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e086-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="8e086-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e086-123">OUTPUTS</span></span>

### <span data-ttu-id="8e086-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e086-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="8e086-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e086-125">NOTES</span></span>

## <span data-ttu-id="8e086-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e086-126">RELATED LINKS</span></span>

[<span data-ttu-id="8e086-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e086-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="8e086-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e086-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="8e086-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="8e086-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


