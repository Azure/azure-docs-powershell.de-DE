---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 513fbe1d973a75dbc1c967610d95882202bab147
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922752"
---
# <span data-ttu-id="912d6-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="912d6-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="912d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="912d6-102">SYNOPSIS</span></span>
<span data-ttu-id="912d6-103">Entfernt den benutzerdefinierten Vpn-IPSec-Richtliniensatz für die Virtual Network Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="912d6-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="912d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="912d6-104">SYNTAX</span></span>

### <span data-ttu-id="912d6-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="912d6-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="912d6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="912d6-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="912d6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="912d6-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="912d6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="912d6-108">DESCRIPTION</span></span>
<span data-ttu-id="912d6-109">Das Virtual Network Gateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="912d6-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="912d6-110">Das **Cmdlet Remove-AzVpnClientIpsecParameter** entfernt die benutzerdefinierten VPN-IPSec-Parameter, die auf Ihrem Virtual Network Gateway festgelegt wurden, wodurch wiederum die standardmäßige VPN-IPSec-Richtlinie auf dem VPN-Gateway basierend auf übergebenen VirtualNetworkGateway-Namen und Ressourcengruppennamen festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="912d6-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="912d6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="912d6-111">EXAMPLES</span></span>

### <span data-ttu-id="912d6-112">Beispiel 1: Löscht die festgelegten vpn-ipsec-Parameter, die im Virtual Network Gateway festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="912d6-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="912d6-113">Löscht die benutzerdefinierten Vpn-IPSec-Parameter, die auf Ihrem Virtuellen Netzwerkgateway mit dem Namen "myGateway" innerhalb der Ressourcengruppe "myRG" festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="912d6-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="912d6-114">Dieser Befehl gibt bool-Objekt zurück, das zeigt, ob das Entfernen erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="912d6-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="912d6-115">Hinweis: Dies führt zum Festlegen der standardmäßigen VPN-IPSec-Richtlinie auf Ihrem Virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="912d6-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="912d6-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="912d6-116">PARAMETERS</span></span>

### <span data-ttu-id="912d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912d6-117">-DefaultProfile</span></span>
<span data-ttu-id="912d6-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="912d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="912d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="912d6-119">-InputObject</span></span>
<span data-ttu-id="912d6-120">Das Objekt des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="912d6-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="912d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="912d6-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="912d6-122">The resource group name.</span></span>

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

### <span data-ttu-id="912d6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="912d6-123">-ResourceId</span></span>
<span data-ttu-id="912d6-124">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="912d6-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="912d6-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="912d6-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="912d6-126">Der Name des Virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="912d6-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="912d6-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="912d6-127">-Confirm</span></span>
<span data-ttu-id="912d6-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="912d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="912d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="912d6-129">-WhatIf</span></span>
<span data-ttu-id="912d6-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="912d6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="912d6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="912d6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="912d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912d6-132">CommonParameters</span></span>
<span data-ttu-id="912d6-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912d6-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="912d6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912d6-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="912d6-135">INPUTS</span></span>

### <span data-ttu-id="912d6-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="912d6-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="912d6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="912d6-137">System.String</span></span>

## <span data-ttu-id="912d6-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="912d6-138">OUTPUTS</span></span>

### <span data-ttu-id="912d6-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="912d6-139">System.Boolean</span></span>

## <span data-ttu-id="912d6-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="912d6-140">NOTES</span></span>

## <span data-ttu-id="912d6-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="912d6-141">RELATED LINKS</span></span>

[<span data-ttu-id="912d6-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="912d6-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="912d6-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="912d6-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="912d6-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="912d6-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
