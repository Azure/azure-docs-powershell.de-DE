---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009025"
---
# <span data-ttu-id="d8953-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8953-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="d8953-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8953-102">SYNOPSIS</span></span>
<span data-ttu-id="d8953-103">Legt die VPN-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="d8953-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="d8953-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8953-104">SYNTAX</span></span>

### <span data-ttu-id="d8953-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8953-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8953-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d8953-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8953-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8953-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8953-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8953-108">DESCRIPTION</span></span>
<span data-ttu-id="d8953-109">Das Cmdlet " **Set-AzVpnClientIpsecParameter** " legt die VPN-IPSec-Parameter für vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="d8953-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="d8953-110">Wenn virtuelles Netzwerkgateway erstellt wird, legt es den Satz von Standard-VPN-IPSec-Richtlinien auf dem Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="d8953-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="d8953-111">Zeigen Sie auf Websitebenutzer möchte bestimmte benutzerdefinierte IPSec-Richtlinien zum Herstellen einer Verbindung mit dem VPN-Gateway verwenden, muss der Benutzer diese IPSec-Richtlinie zuerst auf dem VPN-Gateway festlegen.</span><span class="sxs-lookup"><span data-stu-id="d8953-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="d8953-112">**AzVpnClientIpsecParameter** bietet eine Möglichkeit, dies zu tun.</span><span class="sxs-lookup"><span data-stu-id="d8953-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="d8953-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8953-113">EXAMPLES</span></span>

### <span data-ttu-id="d8953-114">Beispiel 1: legt eine benutzerdefinierte VPN-IPSec-Richtlinie auf vorhandenes virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="d8953-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="d8953-115">In diesem Beispiel wird die benutzerdefinierte VPN-IPSec-Richtlinie auf vorhandenes virtuelles Netzwerkgateway mit dem Namen ContosoVirtualGateway aus der Ressourcengruppe namens ContosoResourceGroup festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8953-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="d8953-116">New-AzVpnClientIpsecParameter-Cmdlet wird zum Erstellen des VPN-IPSec-Parameters-Objekts verwendet, das die Werte der übergebenen oder aller Parameter verwendet, die der Benutzer für ein vorhandenes virtuelles Netzwerkgateway in der ResourceGroup einrichten kann.</span><span class="sxs-lookup"><span data-stu-id="d8953-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="d8953-117">Dieses erstellte VpnClientIPsecParameters-Objekt wird an Set-AzVpnClientIpsecParameter Befehl übergeben, um die angegebene VPN-IPSec-benutzerdefinierte Richtlinie auf dem virtuellen Netzwerkgateway festzulegen, wie in obigem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d8953-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="d8953-118">Dieser Befehl gibt das VpnClientIPsecParameters-Objekt zurück, das die Parameter für "Menge" anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d8953-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="d8953-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8953-119">PARAMETERS</span></span>

### <span data-ttu-id="d8953-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8953-120">-DefaultProfile</span></span>
<span data-ttu-id="d8953-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8953-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8953-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8953-122">-InputObject</span></span>
<span data-ttu-id="d8953-123">Das virtuelle Netzwerkgateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="d8953-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="d8953-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8953-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8953-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8953-125">The resource group name.</span></span>

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

### <span data-ttu-id="d8953-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d8953-126">-ResourceId</span></span>
<span data-ttu-id="d8953-127">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d8953-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d8953-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="d8953-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="d8953-129">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="d8953-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="d8953-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8953-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="d8953-131">IPSec-Parameter für VPN-Client.</span><span class="sxs-lookup"><span data-stu-id="d8953-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="d8953-132">Dieser Parameterwert kann mithilfe von PS Befehl Let: neu-AzVpnClientIpsecParameter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d8953-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="d8953-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d8953-133">-Confirm</span></span>
<span data-ttu-id="d8953-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8953-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8953-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8953-135">-WhatIf</span></span>
<span data-ttu-id="d8953-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8953-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8953-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8953-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8953-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8953-138">CommonParameters</span></span>
<span data-ttu-id="d8953-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8953-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8953-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8953-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8953-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8953-141">INPUTS</span></span>

### <span data-ttu-id="d8953-142">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d8953-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="d8953-143">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d8953-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d8953-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d8953-144">System.String</span></span>

## <span data-ttu-id="d8953-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8953-145">OUTPUTS</span></span>

### <span data-ttu-id="d8953-146">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d8953-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="d8953-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8953-147">NOTES</span></span>

## <span data-ttu-id="d8953-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8953-148">RELATED LINKS</span></span>

[<span data-ttu-id="d8953-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8953-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="d8953-150">Neu – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8953-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="d8953-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d8953-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
