---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: e59f09d44c1d6003122992cb5f14f51b411be25e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660961"
---
# <span data-ttu-id="61f94-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61f94-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="61f94-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61f94-102">SYNOPSIS</span></span>
<span data-ttu-id="61f94-103">Fügt einen Back-End-Adresspool zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="61f94-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="61f94-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61f94-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f94-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f94-105">DESCRIPTION</span></span>
<span data-ttu-id="61f94-106">Mit dem Cmdlet **Add-AzApplicationGatewayBackendAddressPool** wird ein Back-End-Adresspool zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="61f94-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="61f94-107">Eine Back-End-Adresse kann mit einer IP-Adresse, einem vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder IP-Konfigurations-IDs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61f94-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="61f94-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61f94-108">EXAMPLES</span></span>

### <span data-ttu-id="61f94-109">Beispiel 1: Hinzufügen eines Back-End-Adresspools mithilfe eines FQDN des Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="61f94-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="61f94-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Mit dem zweiten Befehl wird der Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways mithilfe von FQDNs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="61f94-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="61f94-111">Beispiel 2: Hinzufügen eines Back-End-Adresspools mithilfe von Back-End-Server-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="61f94-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="61f94-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Mit dem zweiten Befehl wird der Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways mithilfe von IP-Adressen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="61f94-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="61f94-113">Beispiel 3: zurückgekehrter Back-End-Adresspool mithilfe der ID der IP-Adresse des Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="61f94-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="61f94-114">Der erste Befehl ruft ein Netzwerkschnittstellenobjekt mit dem Namen Nic01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $NIC 01-Variablen. Der zweite Befehl ruft ein Netzwerkschnittstellenobjekt mit dem Namen Nic02 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup02 gehört, und speichert es in der Variablen $NIC 02. Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der Befehl Forth verwendet die IDs der Back-End-IP-Konfiguration aus $NIC 01 und $NIC 02, um den Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="61f94-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="61f94-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="61f94-115">PARAMETERS</span></span>

### <span data-ttu-id="61f94-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f94-116">-ApplicationGateway</span></span>
<span data-ttu-id="61f94-117">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Back-End-Adresspool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="61f94-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="61f94-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="61f94-118">-BackendFqdns</span></span>
<span data-ttu-id="61f94-119">Gibt eine Liste von Back-End-FQDNs an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="61f94-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="61f94-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="61f94-120">-BackendIPAddresses</span></span>
<span data-ttu-id="61f94-121">Gibt eine Liste der Back-End-IP-Adressen an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="61f94-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="61f94-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f94-122">-DefaultProfile</span></span>
<span data-ttu-id="61f94-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61f94-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f94-124">-Name</span><span class="sxs-lookup"><span data-stu-id="61f94-124">-Name</span></span>
<span data-ttu-id="61f94-125">Gibt den Namen des Back-End-Server Pools an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="61f94-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="61f94-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61f94-126">-Confirm</span></span>
<span data-ttu-id="61f94-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61f94-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f94-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f94-128">-WhatIf</span></span>
<span data-ttu-id="61f94-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61f94-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f94-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61f94-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f94-131">CommonParameters</span></span>
<span data-ttu-id="61f94-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f94-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f94-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f94-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61f94-134">INPUTS</span></span>

### <span data-ttu-id="61f94-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f94-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61f94-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61f94-136">OUTPUTS</span></span>

### <span data-ttu-id="61f94-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f94-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61f94-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="61f94-138">NOTES</span></span>

## <span data-ttu-id="61f94-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61f94-139">RELATED LINKS</span></span>

[<span data-ttu-id="61f94-140">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61f94-140">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="61f94-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61f94-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="61f94-142">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61f94-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="61f94-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61f94-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="61f94-144">Satz-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="61f94-144">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


