---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174296"
---
# <span data-ttu-id="33dfb-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="33dfb-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="33dfb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="33dfb-103">Das Remove-AzExpressRouteGateway-Cmdlet entfernt ein Azure Express Route-Gateway.</span><span class="sxs-lookup"><span data-stu-id="33dfb-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="33dfb-104">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="33dfb-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="33dfb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33dfb-105">SYNTAX</span></span>

### <span data-ttu-id="33dfb-106">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="33dfb-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33dfb-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="33dfb-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33dfb-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="33dfb-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33dfb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33dfb-109">DESCRIPTION</span></span>
<span data-ttu-id="33dfb-110">Das Remove-AzExpressRouteGateway-Cmdlet entfernt ein Azure Express Route-Gateway.</span><span class="sxs-lookup"><span data-stu-id="33dfb-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="33dfb-111">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="33dfb-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="33dfb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33dfb-112">EXAMPLES</span></span>

### <span data-ttu-id="33dfb-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33dfb-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="33dfb-114">In diesem Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares Express Route-Gateway in Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33dfb-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="33dfb-115">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="33dfb-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="33dfb-116">Dadurch werden die ExpressRouteGateway und alle ExpressRouteConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33dfb-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="33dfb-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="33dfb-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="33dfb-118">In diesem Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Hub, skalierbares Express Route-Gateway in West Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33dfb-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="33dfb-119">Dieser Löschvorgang erfolgt mithilfe der PowerShell-Rohrverlegung, die das vom Get-AzExpressRouteGateway-Befehl zurückgegebene ExpressRouteGateway-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="33dfb-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="33dfb-120">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="33dfb-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="33dfb-121">Dadurch werden die ExpressRouteGateway und alle ExpressRouteConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="33dfb-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="33dfb-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="33dfb-122">PARAMETERS</span></span>

### <span data-ttu-id="33dfb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33dfb-123">-DefaultProfile</span></span>
<span data-ttu-id="33dfb-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33dfb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33dfb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="33dfb-125">-Force</span></span>
<span data-ttu-id="33dfb-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="33dfb-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="33dfb-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="33dfb-127">-InputObject</span></span>
<span data-ttu-id="33dfb-128">Das ExpressRouteGateway-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="33dfb-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="33dfb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="33dfb-129">-Name</span></span>
<span data-ttu-id="33dfb-130">Der ExpressRouteGateway-Name.</span><span class="sxs-lookup"><span data-stu-id="33dfb-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="33dfb-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33dfb-131">-PassThru</span></span>
<span data-ttu-id="33dfb-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="33dfb-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33dfb-133">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="33dfb-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33dfb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33dfb-134">-ResourceGroupName</span></span>
<span data-ttu-id="33dfb-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="33dfb-135">The resource group name.</span></span>

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

### <span data-ttu-id="33dfb-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="33dfb-136">-ResourceId</span></span>
<span data-ttu-id="33dfb-137">Die Azure-Ressourcen-ID für die ExpressRouteGateway, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="33dfb-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="33dfb-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="33dfb-138">-Confirm</span></span>
<span data-ttu-id="33dfb-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="33dfb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33dfb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33dfb-140">-WhatIf</span></span>
<span data-ttu-id="33dfb-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33dfb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33dfb-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33dfb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33dfb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33dfb-143">CommonParameters</span></span>
<span data-ttu-id="33dfb-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33dfb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33dfb-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33dfb-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33dfb-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33dfb-146">INPUTS</span></span>

### <span data-ttu-id="33dfb-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="33dfb-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="33dfb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="33dfb-148">System.String</span></span>

## <span data-ttu-id="33dfb-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33dfb-149">OUTPUTS</span></span>

### <span data-ttu-id="33dfb-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33dfb-150">System.Boolean</span></span>

## <span data-ttu-id="33dfb-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="33dfb-151">NOTES</span></span>

## <span data-ttu-id="33dfb-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33dfb-152">RELATED LINKS</span></span>
