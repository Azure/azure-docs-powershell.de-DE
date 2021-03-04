---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: df81d3df31ad1d04914164d04321151e0df2dfdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930000"
---
# <span data-ttu-id="7028b-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7028b-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="7028b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7028b-102">SYNOPSIS</span></span>
<span data-ttu-id="7028b-103">Erstellt ein skalierbares ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7028b-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="7028b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7028b-104">SYNTAX</span></span>

### <span data-ttu-id="7028b-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7028b-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7028b-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7028b-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7028b-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7028b-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7028b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7028b-108">DESCRIPTION</span></span>

<span data-ttu-id="7028b-109">New-AzExpressRouteGateway erstellt ein skalierbares ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7028b-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="7028b-110">Dies ist eine softwaredefinierte Konnektivität für lokale Verbindungen mit Azure im VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="7028b-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="7028b-111">Dieses Gateway kann basierend auf der skalierungseinheit skaliert werden, die in diesem oder dem Set-AzExpressRouteGateway angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7028b-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="7028b-112">Es wird eine Verbindung von einem lokalen ExpressRoute-Schaltkreis zum skalierbaren Gateway eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="7028b-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="7028b-113">Das ExpressRouteGateway befindet sich an demselben Speicherort wie der VirtualHub, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7028b-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="7028b-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7028b-114">EXAMPLES</span></span>

### <span data-ttu-id="7028b-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7028b-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="7028b-116">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in West USA in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="7028b-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7028b-117">Anschließend wird im virtuellen Hub ein ExpressRoute-Gateway mit zwei Skalierungseinheiten erstellt.</span><span class="sxs-lookup"><span data-stu-id="7028b-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="7028b-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7028b-118">PARAMETERS</span></span>

### <span data-ttu-id="7028b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7028b-119">-AsJob</span></span>
<span data-ttu-id="7028b-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7028b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7028b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7028b-121">-DefaultProfile</span></span>
<span data-ttu-id="7028b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7028b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7028b-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7028b-123">-MaxScaleUnits</span></span>
<span data-ttu-id="7028b-124">Die maximale Anzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="7028b-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7028b-125">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="7028b-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="7028b-126">-MinScaleUnits</span></span>
<span data-ttu-id="7028b-127">Die Mindestanzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="7028b-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="7028b-128">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="7028b-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7028b-129">-Name</span></span>
<span data-ttu-id="7028b-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7028b-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7028b-131">-ResourceGroupName</span></span>
<span data-ttu-id="7028b-132">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7028b-132">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="7028b-133">-Tag</span></span>
<span data-ttu-id="7028b-134">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="7028b-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7028b-135">-VirtualHub</span></span>
<span data-ttu-id="7028b-136">Der VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7028b-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="7028b-137">-VirtualHubId</span></span>
<span data-ttu-id="7028b-138">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7028b-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="7028b-139">-VirtualHubName</span></span>
<span data-ttu-id="7028b-140">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7028b-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7028b-141">-Confirm</span></span>
<span data-ttu-id="7028b-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7028b-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7028b-143">-WhatIf</span></span>
<span data-ttu-id="7028b-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7028b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7028b-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7028b-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7028b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7028b-146">CommonParameters</span></span>
<span data-ttu-id="7028b-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7028b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7028b-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7028b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7028b-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7028b-149">INPUTS</span></span>

### <span data-ttu-id="7028b-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7028b-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="7028b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7028b-151">System.String</span></span>

## <span data-ttu-id="7028b-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7028b-152">OUTPUTS</span></span>

### <span data-ttu-id="7028b-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="7028b-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="7028b-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7028b-154">NOTES</span></span>

## <span data-ttu-id="7028b-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7028b-155">RELATED LINKS</span></span>
