---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004260"
---
# <span data-ttu-id="f8701-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f8701-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="f8701-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8701-102">SYNOPSIS</span></span>
<span data-ttu-id="f8701-103">Das Remove-AzExpressRouteGateway-Cmdlet entfernt ein Azure Express Route-Gateway.</span><span class="sxs-lookup"><span data-stu-id="f8701-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="f8701-104">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="f8701-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="f8701-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8701-105">SYNTAX</span></span>

### <span data-ttu-id="f8701-106">ByExpressRouteGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8701-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8701-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f8701-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8701-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f8701-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8701-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8701-109">DESCRIPTION</span></span>
<span data-ttu-id="f8701-110">Das Remove-AzExpressRouteGateway-Cmdlet entfernt ein Azure Express Route-Gateway.</span><span class="sxs-lookup"><span data-stu-id="f8701-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="f8701-111">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="f8701-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="f8701-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8701-112">EXAMPLES</span></span>

### <span data-ttu-id="f8701-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8701-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="f8701-114">In diesem Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares Express Route-Gateway in Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f8701-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="f8701-115">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="f8701-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="f8701-116">Dadurch werden die ExpressRouteGateway und alle ExpressRouteConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f8701-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="f8701-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f8701-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="f8701-118">In diesem Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Hub, skalierbares Express Route-Gateway in West Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f8701-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="f8701-119">Dieser Löschvorgang erfolgt mithilfe der PowerShell-Rohrverlegung, die das vom Get-AzExpressRouteGateway-Befehl zurückgegebene ExpressRouteGateway-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="f8701-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="f8701-120">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="f8701-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="f8701-121">Dadurch werden die ExpressRouteGateway und alle ExpressRouteConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f8701-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="f8701-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8701-122">PARAMETERS</span></span>

### <span data-ttu-id="f8701-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8701-123">-DefaultProfile</span></span>
<span data-ttu-id="f8701-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8701-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8701-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f8701-125">-Force</span></span>
<span data-ttu-id="f8701-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f8701-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f8701-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8701-127">-InputObject</span></span>
<span data-ttu-id="f8701-128">Das ExpressRouteGateway-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8701-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="f8701-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f8701-129">-Name</span></span>
<span data-ttu-id="f8701-130">Der ExpressRouteGateway-Name.</span><span class="sxs-lookup"><span data-stu-id="f8701-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="f8701-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8701-131">-PassThru</span></span>
<span data-ttu-id="f8701-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f8701-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f8701-133">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f8701-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f8701-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8701-134">-ResourceGroupName</span></span>
<span data-ttu-id="f8701-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8701-135">The resource group name.</span></span>

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

### <span data-ttu-id="f8701-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f8701-136">-ResourceId</span></span>
<span data-ttu-id="f8701-137">Die Azure-Ressourcen-ID für die ExpressRouteGateway, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8701-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="f8701-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8701-138">-Confirm</span></span>
<span data-ttu-id="f8701-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8701-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8701-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8701-140">-WhatIf</span></span>
<span data-ttu-id="f8701-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8701-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8701-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8701-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8701-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8701-143">CommonParameters</span></span>
<span data-ttu-id="f8701-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8701-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8701-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8701-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8701-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8701-146">INPUTS</span></span>

### <span data-ttu-id="f8701-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f8701-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="f8701-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f8701-148">System.String</span></span>

## <span data-ttu-id="f8701-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8701-149">OUTPUTS</span></span>

### <span data-ttu-id="f8701-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8701-150">System.Boolean</span></span>

## <span data-ttu-id="f8701-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8701-151">NOTES</span></span>

## <span data-ttu-id="f8701-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8701-152">RELATED LINKS</span></span>
