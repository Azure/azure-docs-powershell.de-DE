---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146721"
---
# <span data-ttu-id="6a7fd-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="6a7fd-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="6a7fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7fd-103">Das Remove-AzExpressRouteGateway entfernt ein Azure ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="6a7fd-104">Dies ist ein Gateway speziell für die softwaredefinierte Konnektivität des virtuellen Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="6a7fd-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a7fd-105">SYNTAX</span></span>

### <span data-ttu-id="6a7fd-106">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a7fd-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a7fd-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6a7fd-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a7fd-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6a7fd-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a7fd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a7fd-109">DESCRIPTION</span></span>
<span data-ttu-id="6a7fd-110">Das Remove-AzExpressRouteGateway entfernt ein Azure ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="6a7fd-111">Dies ist ein Gateway speziell für die softwaredefinierte Konnektivität des virtuellen Azure-WAN.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="6a7fd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a7fd-112">EXAMPLES</span></span>

### <span data-ttu-id="6a7fd-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a7fd-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="6a7fd-114">In diesem Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtueller Hub und ein skalierbares ExpressRoute-Gateway in den USA erstellt, die dann sofort gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="6a7fd-115">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="6a7fd-116">Dadurch werden das ExpressRouteGateway und alle damit verbundenen ExpressRouteConnections gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="6a7fd-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6a7fd-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="6a7fd-118">In diesem Beispiel wird eine Ressourcengruppe, ein virtuelles WAN, ein virtueller Hub und ein skalierbares "ExpressRoute-Gateway" in der Mitte der USA erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="6a7fd-119">Dieser Löschvorgang erfolgt mithilfe der Powershell-Piping, bei der das vom Befehl "Get-AzExpressRouteGateway" zurückgegebene Get-AzExpressRouteGateway wird.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="6a7fd-120">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="6a7fd-121">Dadurch werden das ExpressRouteGateway und alle damit verbundenen ExpressRouteConnections gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="6a7fd-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a7fd-122">PARAMETERS</span></span>

### <span data-ttu-id="6a7fd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7fd-123">-DefaultProfile</span></span>
<span data-ttu-id="6a7fd-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a7fd-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6a7fd-125">-Force</span></span>
<span data-ttu-id="6a7fd-126">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6a7fd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a7fd-127">-InputObject</span></span>
<span data-ttu-id="6a7fd-128">Das zu löschende ExpressRouteGateway-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-128">The ExpressRouteGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7fd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6a7fd-129">-Name</span></span>
<span data-ttu-id="6a7fd-130">Der Name des ExpressRouteGateways.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a7fd-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a7fd-131">-PassThru</span></span>
<span data-ttu-id="6a7fd-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a7fd-133">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a7fd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7fd-134">-ResourceGroupName</span></span>
<span data-ttu-id="6a7fd-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a7fd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a7fd-136">-ResourceId</span></span>
<span data-ttu-id="6a7fd-137">Die Azure-Ressourcen-ID für das zu löschende ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a7fd-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a7fd-138">-Confirm</span></span>
<span data-ttu-id="6a7fd-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7fd-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6a7fd-140">-WhatIf</span></span>
<span data-ttu-id="6a7fd-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a7fd-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7fd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7fd-143">CommonParameters</span></span>
<span data-ttu-id="6a7fd-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7fd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7fd-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7fd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7fd-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a7fd-146">INPUTS</span></span>

### <span data-ttu-id="6a7fd-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="6a7fd-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="6a7fd-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6a7fd-148">System.String</span></span>

## <span data-ttu-id="6a7fd-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a7fd-149">OUTPUTS</span></span>

### <span data-ttu-id="6a7fd-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a7fd-150">System.Boolean</span></span>

## <span data-ttu-id="6a7fd-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a7fd-151">NOTES</span></span>

## <span data-ttu-id="6a7fd-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a7fd-152">RELATED LINKS</span></span>
