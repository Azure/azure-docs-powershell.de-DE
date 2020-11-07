---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: fcf908f0c67a81ad9ff82eec3aad82f14ac6d1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821303"
---
# <span data-ttu-id="69322-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="69322-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="69322-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69322-102">SYNOPSIS</span></span>
<span data-ttu-id="69322-103">Entfernt die VPN-benutzerdefinierte IPSec-Richtlinie für die Ressource für virtuelles Netzwerk Gateway.</span><span class="sxs-lookup"><span data-stu-id="69322-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="69322-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69322-104">SYNTAX</span></span>

### <span data-ttu-id="69322-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="69322-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69322-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="69322-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69322-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="69322-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69322-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69322-108">DESCRIPTION</span></span>
<span data-ttu-id="69322-109">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="69322-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="69322-110">Das Cmdlet **Remove-AzVpnClientIpsecParameter** entfernt die VPN-benutzerdefinierten IPSec-Parameter, die für Ihr virtuelles Netzwerkgateway festgelegt wurden, wodurch wiederum die Standard-VPN-IPSec-Richtlinie für das VPN-Gateway basierend auf dem VirtualNetworkGateway-Namen und dem Namen der Ressourcengruppe übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="69322-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="69322-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69322-111">EXAMPLES</span></span>

### <span data-ttu-id="69322-112">1: Löscht die auf dem virtuellen Netzwerk Gateway gesetzten VPN-IPSec-Parameter</span><span class="sxs-lookup"><span data-stu-id="69322-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="69322-113">Löscht die VPN-benutzerdefinierten IPSec-Parameter, die für Ihr virtuelles Netzwerk Gateway gesetzt sind, mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="69322-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="69322-114">Dieser Befehl gibt das bool-Objekt zurück, das zeigt, ob die Entfernung erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="69322-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="69322-115">Hinweis: Dies führt zum Festlegen der standardmäßigen VPN-IPSec-Richtlinie für Ihr virtuelles Netzwerk Gateway.</span><span class="sxs-lookup"><span data-stu-id="69322-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="69322-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="69322-116">PARAMETERS</span></span>

### <span data-ttu-id="69322-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69322-117">-DefaultProfile</span></span>
<span data-ttu-id="69322-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69322-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69322-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69322-119">-InputObject</span></span>
<span data-ttu-id="69322-120">Das virtuelle Netzwerkgateway-Objekt</span><span class="sxs-lookup"><span data-stu-id="69322-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="69322-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69322-121">-ResourceGroupName</span></span>
<span data-ttu-id="69322-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69322-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69322-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="69322-123">-ResourceId</span></span>
<span data-ttu-id="69322-124">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="69322-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="69322-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="69322-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="69322-126">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="69322-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69322-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69322-127">-Confirm</span></span>
<span data-ttu-id="69322-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69322-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69322-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69322-129">-WhatIf</span></span>
<span data-ttu-id="69322-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69322-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69322-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69322-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69322-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69322-132">CommonParameters</span></span>
<span data-ttu-id="69322-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69322-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69322-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69322-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69322-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69322-135">INPUTS</span></span>

### <span data-ttu-id="69322-136">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="69322-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="69322-137">System. String</span><span class="sxs-lookup"><span data-stu-id="69322-137">System.String</span></span>

## <span data-ttu-id="69322-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69322-138">OUTPUTS</span></span>

### <span data-ttu-id="69322-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69322-139">System.Boolean</span></span>

## <span data-ttu-id="69322-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="69322-140">NOTES</span></span>

## <span data-ttu-id="69322-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69322-141">RELATED LINKS</span></span>

[<span data-ttu-id="69322-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="69322-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="69322-143">Neu – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="69322-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="69322-144">Satz-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="69322-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
