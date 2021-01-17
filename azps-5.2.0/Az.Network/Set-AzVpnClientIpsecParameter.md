---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365069"
---
# <span data-ttu-id="07a7e-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="07a7e-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="07a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="07a7e-103">Legt die Vpn-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="07a7e-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="07a7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07a7e-104">SYNTAX</span></span>

### <span data-ttu-id="07a7e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="07a7e-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a7e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="07a7e-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a7e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07a7e-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a7e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07a7e-108">DESCRIPTION</span></span>
<span data-ttu-id="07a7e-109">Das **Cmdlet "Set-AzVpnClientIpsecParameter"** legt die vpn-ipsec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="07a7e-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="07a7e-110">Beim Erstellen des virtuellen Netzwerkgateways werden die standardmäßigen Vpn-IPSec-Richtlinien für das Gateway festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07a7e-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="07a7e-111">Für den Fall, dass der Benutzer von "Verweisen auf" bestimmte benutzerdefinierte Ipsec-Richtlinien zum Herstellen einer Verbindung mit dem VPN-Gateway verwenden möchte, muss der Benutzer diese "ipsec"-Richtlinie zuerst auf dem VPN-Gateway festlegen.</span><span class="sxs-lookup"><span data-stu-id="07a7e-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="07a7e-112">**Set-AzVpnClientIpsecParameter** bietet eine Möglichkeit dazu.</span><span class="sxs-lookup"><span data-stu-id="07a7e-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="07a7e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07a7e-113">EXAMPLES</span></span>

### <span data-ttu-id="07a7e-114">Beispiel 1: Legt eine benutzerdefinierte Vpn-Ipsec-Richtlinie auf ein vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="07a7e-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="07a7e-115">In diesem Beispiel wird die benutzerdefinierte Vpn-Ipsec-Richtlinie aus der Ressourcengruppe "ContosoResourceGroup" auf das vorhandene virtuelle Netzwerkgateway namens "ContosoVirtualGateway" definiert.</span><span class="sxs-lookup"><span data-stu-id="07a7e-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="07a7e-116">New-AzVpnClientIpsecParameter cmdlet wird verwendet, um das Vpn-IPSec-Parameterobjekt zu erstellen, in dem die übergebenen Werte eines oder aller Parameter verwendet werden, die der Benutzer für ein vorhandenes virtuelles Netzwerkgateway in ResourceGroup festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="07a7e-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="07a7e-117">Dieses erstellte "VpnClientIPsecParameters"-Objekt wird an den Befehl Set-AzVpnClientIpsecParameter übergeben, um die angegebene benutzerdefinierte Vpn-Ipsec-Richtlinie für das virtuelle Netzwerkgateway wie im obigen Beispiel gezeigt zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="07a7e-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="07a7e-118">Dieser Befehl gibt das Objekt "VpnClientIPsecParameters" zurück, das die festgelegten Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="07a7e-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="07a7e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07a7e-119">PARAMETERS</span></span>

### <span data-ttu-id="07a7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a7e-120">-DefaultProfile</span></span>
<span data-ttu-id="07a7e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07a7e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07a7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07a7e-122">-InputObject</span></span>
<span data-ttu-id="07a7e-123">Das Objekt des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="07a7e-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07a7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="07a7e-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07a7e-125">The resource group name.</span></span>

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

### <span data-ttu-id="07a7e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07a7e-126">-ResourceId</span></span>
<span data-ttu-id="07a7e-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="07a7e-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a7e-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="07a7e-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="07a7e-129">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="07a7e-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="07a7e-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="07a7e-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="07a7e-131">Ipsec-Parameter des Vpn-Clients.</span><span class="sxs-lookup"><span data-stu-id="07a7e-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="07a7e-132">Dieser Parameterwert kann mithilfe des Befehls "PS" let:New-AzVpnClientIpsecParameter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="07a7e-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07a7e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07a7e-133">-Confirm</span></span>
<span data-ttu-id="07a7e-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07a7e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a7e-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="07a7e-135">-WhatIf</span></span>
<span data-ttu-id="07a7e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07a7e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a7e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07a7e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a7e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a7e-138">CommonParameters</span></span>
<span data-ttu-id="07a7e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a7e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a7e-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a7e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a7e-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07a7e-141">INPUTS</span></span>

### <span data-ttu-id="07a7e-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="07a7e-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="07a7e-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="07a7e-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="07a7e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="07a7e-144">System.String</span></span>

## <span data-ttu-id="07a7e-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07a7e-145">OUTPUTS</span></span>

### <span data-ttu-id="07a7e-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="07a7e-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="07a7e-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07a7e-147">NOTES</span></span>

## <span data-ttu-id="07a7e-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07a7e-148">RELATED LINKS</span></span>

[<span data-ttu-id="07a7e-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="07a7e-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="07a7e-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="07a7e-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="07a7e-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="07a7e-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
