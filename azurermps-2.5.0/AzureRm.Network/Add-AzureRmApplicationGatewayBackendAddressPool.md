---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 6f22c8026d3b72a6c9cd52563252aa3d4bcad039
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849644"
---
# <span data-ttu-id="3ee43-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ee43-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="3ee43-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ee43-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee43-103">Fügt einen Back-End-Adresspool zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="3ee43-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ee43-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ee43-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee43-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ee43-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee43-106">Mit dem Cmdlet **Add-AzureRmApplicationGatewayBackendAddressPool** wird ein Back-End-Adresspool zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="3ee43-107">Eine Back-End-Adresse kann mit einer IP-Adresse, einem vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder IP-Konfigurations-IDs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ee43-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="3ee43-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ee43-108">EXAMPLES</span></span>

### <span data-ttu-id="3ee43-109">Beispiel 1: Hinzufügen eines Back-End-Adresspools mithilfe eines FQDN des Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="3ee43-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="3ee43-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Mit dem zweiten Befehl wird der Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways mithilfe von FQDNs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="3ee43-111">Beispiel 2: Hinzufügen eines Back-End-Adresspools mithilfe von Back-End-Server-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="3ee43-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="3ee43-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Mit dem zweiten Befehl wird der Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways mithilfe von IP-Adressen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="3ee43-113">Beispiel 3: zurückgekehrter Back-End-Adresspool mithilfe der ID der IP-Adresse des Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="3ee43-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="3ee43-114">Der erste Befehl ruft ein Netzwerkschnittstellenobjekt mit dem Namen Nic01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $NIC 01-Variablen. Der zweite Befehl ruft ein Netzwerkschnittstellenobjekt mit dem Namen Nic02 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup02 gehört, und speichert es in der Variablen $NIC 02. Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der Befehl Forth verwendet die IDs der Back-End-IP-Konfiguration aus $NIC 01 und $NIC 02, um den Back-End-Adresspool des in $AppGw gespeicherten Anwendungs Gateways hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ee43-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3ee43-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ee43-115">PARAMETERS</span></span>

### <span data-ttu-id="3ee43-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ee43-116">-ApplicationGateway</span></span>
<span data-ttu-id="3ee43-117">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Back-End-Adresspool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee43-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="3ee43-118">-BackendFqdns</span></span>
<span data-ttu-id="3ee43-119">Gibt eine Liste von Back-End-FQDNs an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee43-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="3ee43-120">-BackendIPAddresses</span></span>
<span data-ttu-id="3ee43-121">Gibt eine Liste der Back-End-IP-Adressen an, die dieses Cmdlet als Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee43-122">-DefaultProfile</span></span>
<span data-ttu-id="3ee43-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ee43-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee43-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3ee43-124">-Name</span></span>
<span data-ttu-id="3ee43-125">Gibt den Namen des Back-End-Server Pools an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee43-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ee43-126">-Confirm</span></span>
<span data-ttu-id="3ee43-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ee43-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee43-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee43-128">-WhatIf</span></span>
<span data-ttu-id="3ee43-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ee43-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ee43-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ee43-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee43-131">CommonParameters</span></span>
<span data-ttu-id="3ee43-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee43-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee43-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee43-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ee43-134">INPUTS</span></span>

###  
<span data-ttu-id="3ee43-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3ee43-135">System.String</span></span>

## <span data-ttu-id="3ee43-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ee43-136">OUTPUTS</span></span>

### <span data-ttu-id="3ee43-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ee43-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ee43-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ee43-138">NOTES</span></span>

## <span data-ttu-id="3ee43-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ee43-139">RELATED LINKS</span></span>

[<span data-ttu-id="3ee43-140">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ee43-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3ee43-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ee43-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3ee43-142">Neu – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ee43-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3ee43-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ee43-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3ee43-144">Satz-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3ee43-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


