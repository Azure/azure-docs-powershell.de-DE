---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 77c41a4565a517a51b02c904d79953d79e908c39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941672"
---
# <span data-ttu-id="2bc44-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="2bc44-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="2bc44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bc44-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc44-103">Das Remove-AzExpressRouteGateway entfernt ein Azure ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="2bc44-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="2bc44-104">Dies ist ein Gateway speziell für die softwaredefinierte Konnektivität von Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="2bc44-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="2bc44-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bc44-105">SYNTAX</span></span>

### <span data-ttu-id="2bc44-106">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2bc44-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bc44-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2bc44-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bc44-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2bc44-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc44-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bc44-109">DESCRIPTION</span></span>
<span data-ttu-id="2bc44-110">Das Remove-AzExpressRouteGateway entfernt ein Azure ExpressRoute-Gateway.</span><span class="sxs-lookup"><span data-stu-id="2bc44-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="2bc44-111">Dies ist ein Gateway speziell für die softwaredefinierte Konnektivität von Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="2bc44-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="2bc44-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2bc44-112">EXAMPLES</span></span>

### <span data-ttu-id="2bc44-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2bc44-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="2bc44-114">In diesem Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares ExpressRoute-Gateway in Zentral-USA erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2bc44-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="2bc44-115">Wenn Sie die Eingabeaufforderung beim Löschen des virtuellen Gateways unterdrücken möchten, verwenden Sie das -Force-Flag.</span><span class="sxs-lookup"><span data-stu-id="2bc44-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="2bc44-116">Dadurch werden das ExpressRouteGateway und alle daran angefügten ExpressRouteConnections gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2bc44-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="2bc44-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2bc44-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="2bc44-118">In diesem Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares ExpressRoute-Gateway in West Central USA erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2bc44-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="2bc44-119">Dieser Löschvorgang erfolgt mithilfe der Powershell-Piping, bei der das vom Befehl "Get-AzExpressRouteGateway" zurückgegebene ExpressRouteGateway-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2bc44-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="2bc44-120">Wenn Sie die Eingabeaufforderung beim Löschen des virtuellen Gateways unterdrücken möchten, verwenden Sie das -Force-Flag.</span><span class="sxs-lookup"><span data-stu-id="2bc44-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="2bc44-121">Dadurch werden das ExpressRouteGateway und alle daran angefügten ExpressRouteConnections gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2bc44-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="2bc44-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2bc44-122">PARAMETERS</span></span>

### <span data-ttu-id="2bc44-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc44-123">-DefaultProfile</span></span>
<span data-ttu-id="2bc44-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bc44-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bc44-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2bc44-125">-Force</span></span>
<span data-ttu-id="2bc44-126">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="2bc44-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2bc44-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bc44-127">-InputObject</span></span>
<span data-ttu-id="2bc44-128">Das zu löschende ExpressRouteGateway-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2bc44-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="2bc44-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2bc44-129">-Name</span></span>
<span data-ttu-id="2bc44-130">Der Name des ExpressRouteGateways.</span><span class="sxs-lookup"><span data-stu-id="2bc44-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="2bc44-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bc44-131">-PassThru</span></span>
<span data-ttu-id="2bc44-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2bc44-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2bc44-133">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2bc44-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2bc44-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc44-134">-ResourceGroupName</span></span>
<span data-ttu-id="2bc44-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2bc44-135">The resource group name.</span></span>

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

### <span data-ttu-id="2bc44-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bc44-136">-ResourceId</span></span>
<span data-ttu-id="2bc44-137">Die Azure-Ressourcen-ID für das ExpressRouteGateway, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="2bc44-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="2bc44-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bc44-138">-Confirm</span></span>
<span data-ttu-id="2bc44-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bc44-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bc44-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc44-140">-WhatIf</span></span>
<span data-ttu-id="2bc44-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bc44-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc44-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bc44-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bc44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc44-143">CommonParameters</span></span>
<span data-ttu-id="2bc44-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc44-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc44-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc44-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2bc44-146">INPUTS</span></span>

### <span data-ttu-id="2bc44-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="2bc44-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="2bc44-148">System.String</span><span class="sxs-lookup"><span data-stu-id="2bc44-148">System.String</span></span>

## <span data-ttu-id="2bc44-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2bc44-149">OUTPUTS</span></span>

### <span data-ttu-id="2bc44-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2bc44-150">System.Boolean</span></span>

## <span data-ttu-id="2bc44-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2bc44-151">NOTES</span></span>

## <span data-ttu-id="2bc44-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2bc44-152">RELATED LINKS</span></span>
