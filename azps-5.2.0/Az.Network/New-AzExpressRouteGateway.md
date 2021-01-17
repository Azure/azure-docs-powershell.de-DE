---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303096"
---
# <span data-ttu-id="a0175-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="a0175-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="a0175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0175-102">SYNOPSIS</span></span>
<span data-ttu-id="a0175-103">Erstellt ein skalierbares ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="a0175-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="a0175-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0175-104">SYNTAX</span></span>

### <span data-ttu-id="a0175-105">ByVirtualHubName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0175-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0175-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="a0175-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0175-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="a0175-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0175-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0175-108">DESCRIPTION</span></span>

<span data-ttu-id="a0175-109">New-AzExpressRouteGateway erstellt ein skalierbares ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="a0175-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="a0175-110">Dabei handelt es sich um softwaredefinierte Konnektivität für eine lokale Verbindung zu Azure innerhalb von VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="a0175-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="a0175-111">Dieses Gateway kann basierend auf der angegebenen Skalierungseinheit oder dem cmdlet Set-AzExpressRouteGateway skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="a0175-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="a0175-112">Eine Verbindung wird von einem lokalen ExpressRoute-Schaltkreis zum skalierbaren Gateway eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a0175-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="a0175-113">Das ExpressRouteGateway befindet sich an demselben Speicherort wie der VirtualHub, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a0175-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="a0175-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0175-114">EXAMPLES</span></span>

### <span data-ttu-id="a0175-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0175-115">Example 1</span></span>

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

<span data-ttu-id="a0175-116">Im vorstehenden Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtuelles Netzwerk und ein virtueller Hub in der West-US-Region in der Ressourcengruppe "testRG" in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="a0175-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a0175-117">Anschließend wird im virtuellen Hub mit 2 Skalierungseinheiten ein "ExpressRoute"-Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="a0175-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="a0175-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0175-118">PARAMETERS</span></span>

### <span data-ttu-id="a0175-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0175-119">-AsJob</span></span>
<span data-ttu-id="a0175-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a0175-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0175-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0175-121">-DefaultProfile</span></span>
<span data-ttu-id="a0175-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0175-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0175-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="a0175-123">-MaxScaleUnits</span></span>
<span data-ttu-id="a0175-124">Die maximale Anzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="a0175-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="a0175-125">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="a0175-125">Valid range > 2</span></span>

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

### <span data-ttu-id="a0175-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="a0175-126">-MinScaleUnits</span></span>
<span data-ttu-id="a0175-127">Die Mindestanzahl von Skalierungseinheiten für dieses ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="a0175-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="a0175-128">Gültiger Bereich > 2</span><span class="sxs-lookup"><span data-stu-id="a0175-128">Valid range > 2</span></span>

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

### <span data-ttu-id="a0175-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a0175-129">-Name</span></span>
<span data-ttu-id="a0175-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a0175-130">The resource name.</span></span>

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

### <span data-ttu-id="a0175-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0175-131">-ResourceGroupName</span></span>
<span data-ttu-id="a0175-132">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a0175-132">The resource name.</span></span>

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

### <span data-ttu-id="a0175-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0175-133">-Tag</span></span>
<span data-ttu-id="a0175-134">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="a0175-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a0175-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0175-135">-VirtualHub</span></span>
<span data-ttu-id="a0175-136">Der VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="a0175-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a0175-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="a0175-137">-VirtualHubId</span></span>
<span data-ttu-id="a0175-138">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="a0175-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a0175-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="a0175-139">-VirtualHubName</span></span>
<span data-ttu-id="a0175-140">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="a0175-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="a0175-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0175-141">-Confirm</span></span>
<span data-ttu-id="a0175-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0175-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0175-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a0175-143">-WhatIf</span></span>
<span data-ttu-id="a0175-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0175-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0175-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0175-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0175-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0175-146">CommonParameters</span></span>
<span data-ttu-id="a0175-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0175-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0175-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0175-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0175-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0175-149">INPUTS</span></span>

### <span data-ttu-id="a0175-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="a0175-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="a0175-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a0175-151">System.String</span></span>

## <span data-ttu-id="a0175-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0175-152">OUTPUTS</span></span>

### <span data-ttu-id="a0175-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="a0175-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="a0175-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0175-154">NOTES</span></span>

## <span data-ttu-id="a0175-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0175-155">RELATED LINKS</span></span>
