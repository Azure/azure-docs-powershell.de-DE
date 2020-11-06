---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
ms.openlocfilehash: 34e143b3ca6114fd90d52a5ad6ee8c022fda5688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503490"
---
# <span data-ttu-id="46959-101">Remove-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46959-101">Remove-AzureRmVpnGateway</span></span>

## <span data-ttu-id="46959-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46959-102">SYNOPSIS</span></span>
<span data-ttu-id="46959-103">Das Remove-AzureRmVpnGateway-Cmdlet entfernt ein Azure VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="46959-103">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="46959-104">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="46959-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46959-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46959-105">SYNTAX</span></span>

### <span data-ttu-id="46959-106">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="46959-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46959-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="46959-107">ByVpnGatewayObject</span></span>
```
Remove-AzureRmVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46959-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="46959-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzureRmVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46959-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46959-109">DESCRIPTION</span></span>
<span data-ttu-id="46959-110">Das Remove-AzureRmVpnGateway-Cmdlet entfernt ein Azure VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="46959-110">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="46959-111">Hierbei handelt es sich um ein Gateway, das für die Software definierte Konnektivität von Azure Virtual WAN spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="46959-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="46959-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46959-112">EXAMPLES</span></span>

### <span data-ttu-id="46959-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46959-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="46959-114">In diesem Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares VPN-Gateway in Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46959-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="46959-115">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="46959-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="46959-116">Dadurch werden die VpnGateway und alle VpnConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46959-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="46959-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="46959-117">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzureRmVpnGateway-Passthru
```

<span data-ttu-id="46959-118">In diesem Beispiel werden eine Ressourcengruppe, virtuelles WAN, virtueller Hub, skalierbares VPN-Gateway in Central US erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46959-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="46959-119">Dieser Löschvorgang erfolgt mithilfe der PowerShell-Rohrverlegung, die das vom Get-AzureRmVpnGateway-Befehl zurückgegebene VpnGateway-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="46959-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzureRmVpnGateway command.</span></span>
<span data-ttu-id="46959-120">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Gateways zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="46959-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="46959-121">Dadurch werden die VpnGateway und alle VpnConnections, die an Sie angefügt sind, gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46959-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="46959-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="46959-122">PARAMETERS</span></span>

### <span data-ttu-id="46959-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46959-123">-DefaultProfile</span></span>
<span data-ttu-id="46959-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46959-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46959-125">-Force</span><span class="sxs-lookup"><span data-stu-id="46959-125">-Force</span></span>
<span data-ttu-id="46959-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="46959-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46959-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46959-127">-InputObject</span></span>
<span data-ttu-id="46959-128">Das vpnGateway-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="46959-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46959-129">-Name</span><span class="sxs-lookup"><span data-stu-id="46959-129">-Name</span></span>
<span data-ttu-id="46959-130">Der vpnGateway-Name.</span><span class="sxs-lookup"><span data-stu-id="46959-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46959-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46959-131">-PassThru</span></span>
<span data-ttu-id="46959-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="46959-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="46959-133">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="46959-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46959-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46959-134">-ResourceGroupName</span></span>
<span data-ttu-id="46959-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46959-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46959-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="46959-136">-ResourceId</span></span>
<span data-ttu-id="46959-137">Die Azure-Ressourcen-ID für die vpnGateway, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="46959-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46959-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46959-138">-Confirm</span></span>
<span data-ttu-id="46959-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46959-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46959-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46959-140">-WhatIf</span></span>
<span data-ttu-id="46959-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46959-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46959-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46959-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46959-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46959-143">CommonParameters</span></span>
<span data-ttu-id="46959-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46959-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46959-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46959-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46959-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46959-146">INPUTS</span></span>

### <span data-ttu-id="46959-147">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="46959-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="46959-148">System. String</span><span class="sxs-lookup"><span data-stu-id="46959-148">System.String</span></span>

## <span data-ttu-id="46959-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46959-149">OUTPUTS</span></span>

### <span data-ttu-id="46959-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46959-150">System.Boolean</span></span>

## <span data-ttu-id="46959-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="46959-151">NOTES</span></span>

## <span data-ttu-id="46959-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46959-152">RELATED LINKS</span></span>
