---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180227"
---
# <span data-ttu-id="bf9c6-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf9c6-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="bf9c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9c6-103">Fügt einen Back-End-Adresspool zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="bf9c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf9c6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf9c6-106">Mit dem Cmdlet **Add-AzApplicationGatewayBackendAddressPool** wird ein Back-End-Adresspool zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="bf9c6-107">Eine Back-End-Adresse kann mit einer IP-Adresse, einem vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder IP-Konfigurations-IDs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="bf9c6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf9c6-108">EXAMPLES</span></span>

### <span data-ttu-id="bf9c6-109">Beispiel 1: Hinzufügen eines Back-End-Adresspools mithilfe eines FQDN des Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="bf9c6-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="bf9c6-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Mit dem zweiten Befehl wird der Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways mithilfe von FQDNs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="bf9c6-111">Beispiel 2: Hinzufügen eines Back-End-Adresspools mithilfe von Back-End-Server-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="bf9c6-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="bf9c6-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Mit dem zweiten Befehl wird der Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways mithilfe von IP-Adressen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="bf9c6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf9c6-113">PARAMETERS</span></span>

### <span data-ttu-id="bf9c6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf9c6-114">-ApplicationGateway</span></span>
<span data-ttu-id="bf9c6-115">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Back-End-Adresspool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="bf9c6-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="bf9c6-116">-BackendFqdns</span></span>
<span data-ttu-id="bf9c6-117">Gibt eine Liste von Back-End-FQDNs an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="bf9c6-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="bf9c6-118">-BackendIPAddresses</span></span>
<span data-ttu-id="bf9c6-119">Gibt eine Liste der Back-End-IP-Adressen an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="bf9c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9c6-120">-DefaultProfile</span></span>
<span data-ttu-id="bf9c6-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf9c6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bf9c6-122">-Name</span></span>
<span data-ttu-id="bf9c6-123">Gibt den Namen des Back-End-Server Pools an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="bf9c6-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf9c6-124">-Confirm</span></span>
<span data-ttu-id="bf9c6-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf9c6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9c6-126">-WhatIf</span></span>
<span data-ttu-id="bf9c6-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9c6-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf9c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9c6-129">CommonParameters</span></span>
<span data-ttu-id="bf9c6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf9c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9c6-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf9c6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9c6-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf9c6-132">INPUTS</span></span>

### <span data-ttu-id="bf9c6-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf9c6-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf9c6-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf9c6-134">OUTPUTS</span></span>

### <span data-ttu-id="bf9c6-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf9c6-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf9c6-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf9c6-136">NOTES</span></span>

## <span data-ttu-id="bf9c6-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf9c6-137">RELATED LINKS</span></span>

[<span data-ttu-id="bf9c6-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf9c6-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bf9c6-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf9c6-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bf9c6-140">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf9c6-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bf9c6-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf9c6-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bf9c6-142">Satz-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bf9c6-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bf9c6-143">Satz-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bf9c6-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
