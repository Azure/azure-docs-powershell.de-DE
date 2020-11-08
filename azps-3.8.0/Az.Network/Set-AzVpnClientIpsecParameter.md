---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 1ffa87d60426bc7b012dd003cf8a52b215502f59
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995353"
---
# <span data-ttu-id="42945-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="42945-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="42945-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42945-102">SYNOPSIS</span></span>
<span data-ttu-id="42945-103">Legt die VPN-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="42945-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="42945-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42945-104">SYNTAX</span></span>

### <span data-ttu-id="42945-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="42945-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42945-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="42945-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42945-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42945-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42945-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42945-108">DESCRIPTION</span></span>
<span data-ttu-id="42945-109">Das Cmdlet " **Set-AzVpnClientIpsecParameter** " legt die VPN-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="42945-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="42945-110">Wenn virtuelles Netzwerkgateway erstellt wird, legt es den Satz von Standard-VPN-IPSec-Richtlinien auf dem Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="42945-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="42945-111">Zeigen Sie auf Websitebenutzer möchte bestimmte benutzerdefinierte IPSec-Richtlinien zum Herstellen einer Verbindung mit dem VPN-Gateway verwenden, muss der Benutzer diese IPSec-Richtlinie zuerst auf dem VPN-Gateway festlegen.</span><span class="sxs-lookup"><span data-stu-id="42945-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="42945-112">**AzVpnClientIpsecParameter** bietet eine Möglichkeit, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="42945-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="42945-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42945-113">EXAMPLES</span></span>

### <span data-ttu-id="42945-114">Beispiel 1: legt eine benutzerdefinierte VPN-IPSec-Richtlinie auf vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="42945-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="42945-115">In diesem Beispiel wird die benutzerdefinierte VPN-IPSec-Richtlinie auf vorhandenes virtuelles Netzwerkgateway mit dem Namen ContosoVirtualGateway aus der Ressourcengruppe namens ContosoResourceGroup festgelegt.</span><span class="sxs-lookup"><span data-stu-id="42945-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="42945-116">New-AzVpnClientIpsecParameter-Cmdlet wird zum Erstellen des VPN-IPSec-Parameters-Objekts verwendet, das die Werte der übergebenen oder aller Parameter verwendet, die der Benutzer für ein vorhandenes virtuelles Netzwerkgateway in der ResourceGroup einrichten kann.</span><span class="sxs-lookup"><span data-stu-id="42945-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="42945-117">Dieses erstellte VpnClientIPsecParameters-Objekt wird an Set-AzVpnClientIpsecParameter Befehl übergeben, um die angegebene VPN-IPSec-benutzerdefinierte Richtlinie auf dem virtuellen Netzwerkgateway festzulegen, wie in obigem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="42945-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="42945-118">Dieser Befehl gibt das VpnClientIPsecParameters-Objekt zurück, das die Parameter für "Menge" anzeigt.</span><span class="sxs-lookup"><span data-stu-id="42945-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="42945-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="42945-119">PARAMETERS</span></span>

### <span data-ttu-id="42945-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42945-120">-DefaultProfile</span></span>
<span data-ttu-id="42945-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42945-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42945-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42945-122">-InputObject</span></span>
<span data-ttu-id="42945-123">Das virtuelle Netzwerkgateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="42945-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="42945-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42945-124">-ResourceGroupName</span></span>
<span data-ttu-id="42945-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42945-125">The resource group name.</span></span>

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

### <span data-ttu-id="42945-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="42945-126">-ResourceId</span></span>
<span data-ttu-id="42945-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="42945-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="42945-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="42945-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="42945-129">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="42945-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="42945-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="42945-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="42945-131">IPSec-Parameter für VPN-Client.</span><span class="sxs-lookup"><span data-stu-id="42945-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="42945-132">Dieser Parameterwert kann mithilfe von PS Befehl Let: neu-AzVpnClientIpsecParameter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="42945-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="42945-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42945-133">-Confirm</span></span>
<span data-ttu-id="42945-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42945-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42945-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42945-135">-WhatIf</span></span>
<span data-ttu-id="42945-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42945-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42945-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42945-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42945-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42945-138">CommonParameters</span></span>
<span data-ttu-id="42945-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42945-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42945-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42945-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42945-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42945-141">INPUTS</span></span>

### <span data-ttu-id="42945-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="42945-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="42945-143">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="42945-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="42945-144">System. String</span><span class="sxs-lookup"><span data-stu-id="42945-144">System.String</span></span>

## <span data-ttu-id="42945-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42945-145">OUTPUTS</span></span>

### <span data-ttu-id="42945-146">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="42945-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="42945-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="42945-147">NOTES</span></span>

## <span data-ttu-id="42945-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42945-148">RELATED LINKS</span></span>

[<span data-ttu-id="42945-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="42945-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="42945-150">Neu – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="42945-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="42945-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="42945-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
