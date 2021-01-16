---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295384"
---
# <span data-ttu-id="63f70-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63f70-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="63f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f70-102">SYNOPSIS</span></span>
<span data-ttu-id="63f70-103">Fügt einem Anwendungsgateway einen Back-End-Adresspool hinzu.</span><span class="sxs-lookup"><span data-stu-id="63f70-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="63f70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63f70-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f70-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63f70-105">DESCRIPTION</span></span>
<span data-ttu-id="63f70-106">Das **Cmdlet "Add-AzApplicationGatewayBackendAddressPool"** fügt einem Anwendungsgateway einen Back-End-Adresspool hinzu.</span><span class="sxs-lookup"><span data-stu-id="63f70-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="63f70-107">Eine Back-End-Adresse kann mithilfe einer IP-Adresse, eines vollqualifizierten Domänennamens (Fully Qualified Domain Name, FQDN) oder von IP-Konfigurations-IDs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="63f70-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="63f70-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63f70-108">EXAMPLES</span></span>

### <span data-ttu-id="63f70-109">Beispiel 1: Hinzufügen eines Back-End-Adresspools mithilfe eines Back-End-Server-FQDNs</span><span class="sxs-lookup"><span data-stu-id="63f70-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="63f70-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable. Mit dem zweiten Befehl wird der Back-End-Adresspool des In-App-Gateways, das in $AppGw FQDNs gespeichert ist, addiert.</span><span class="sxs-lookup"><span data-stu-id="63f70-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="63f70-111">Beispiel 2: Hinzufügen eines Back-End-Adresspools mithilfe von Back-End-Server-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="63f70-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="63f70-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable. Mit dem zweiten Befehl wird der Back-End-Adresspool des In-App-Gateways, das in $AppGw über die IP-Adressen gespeichert ist, addiert.</span><span class="sxs-lookup"><span data-stu-id="63f70-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="63f70-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63f70-113">PARAMETERS</span></span>

### <span data-ttu-id="63f70-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63f70-114">-ApplicationGateway</span></span>
<span data-ttu-id="63f70-115">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Back-End-Adresspool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="63f70-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63f70-116">-Back-EndFqdns</span><span class="sxs-lookup"><span data-stu-id="63f70-116">-BackendFqdns</span></span>
<span data-ttu-id="63f70-117">Gibt eine Liste der Back-End-FQDNs an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="63f70-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f70-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="63f70-118">-BackendIPAddresses</span></span>
<span data-ttu-id="63f70-119">Gibt eine Liste der Back-End-IP-Adressen an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="63f70-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f70-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f70-120">-DefaultProfile</span></span>
<span data-ttu-id="63f70-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63f70-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63f70-122">-Name</span><span class="sxs-lookup"><span data-stu-id="63f70-122">-Name</span></span>
<span data-ttu-id="63f70-123">Gibt den Namen des Back-End-Serverpools an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="63f70-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="63f70-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63f70-124">-Confirm</span></span>
<span data-ttu-id="63f70-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63f70-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f70-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="63f70-126">-WhatIf</span></span>
<span data-ttu-id="63f70-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63f70-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f70-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63f70-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f70-129">CommonParameters</span></span>
<span data-ttu-id="63f70-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f70-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f70-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f70-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63f70-132">INPUTS</span></span>

### <span data-ttu-id="63f70-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63f70-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63f70-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63f70-134">OUTPUTS</span></span>

### <span data-ttu-id="63f70-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63f70-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63f70-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="63f70-136">NOTES</span></span>

## <span data-ttu-id="63f70-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="63f70-137">RELATED LINKS</span></span>

[<span data-ttu-id="63f70-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63f70-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63f70-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63f70-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63f70-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63f70-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63f70-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63f70-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63f70-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63f70-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="63f70-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="63f70-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
