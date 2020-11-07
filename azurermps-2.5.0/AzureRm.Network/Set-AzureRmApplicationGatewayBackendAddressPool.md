---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 66ca482f2b284118ccf5095ec833a5278a5ea73d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850579"
---
# <span data-ttu-id="b4954-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4954-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b4954-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4954-102">SYNOPSIS</span></span>
<span data-ttu-id="b4954-103">Aktualisiert einen Back-End-Adresspool für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b4954-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4954-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4954-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4954-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4954-105">DESCRIPTION</span></span>
<span data-ttu-id="b4954-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayBackendAddressPool** " aktualisiert einen Back-End-Adresspool für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="b4954-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="b4954-107">Back-End-Adressen können als IP-Adressen, vollqualifizierte Domänennamen (Fully Qualified Domain Name, FQDN) oder IP-Konfigurations-IDs angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b4954-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="b4954-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4954-108">EXAMPLES</span></span>

### <span data-ttu-id="b4954-109">Beispiel 1: Festlegen eines Back-End-Adresspools mithilfe von FQDNs</span><span class="sxs-lookup"><span data-stu-id="b4954-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="b4954-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="b4954-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b4954-111">Der zweite Befehl aktualisiert den Back-End-Adresspool des Anwendungs Gateways in $AppGw mithilfe von FQDNs.</span><span class="sxs-lookup"><span data-stu-id="b4954-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="b4954-112">Beispiel 2: Festlegen eines Back-End-Adresspools mithilfe von Back-End-Server-IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="b4954-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="b4954-113">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="b4954-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b4954-114">Der zweite Befehl aktualisiert den Back-End-Adresspool des Anwendungs Gateways in $AppGw mithilfe von IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="b4954-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="b4954-115">Beispiel 3: Festlegen eines Back-End-Adresspools mithilfe der ID der IP-Adresse des Back-End-Servers</span><span class="sxs-lookup"><span data-stu-id="b4954-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="b4954-116">Der erste Befehl ruft ein Netzwerkschnittstellenobjekt mit dem Namen Nic01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $NIC 01-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b4954-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="b4954-117">Der zweite Befehl ruft ein Netzwerkschnittstellenobjekt mit dem Namen Nic02 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup02 gehört, und speichert es in der Variablen $NIC 02.</span><span class="sxs-lookup"><span data-stu-id="b4954-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="b4954-118">Der dritte Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="b4954-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b4954-119">Der Befehl Forth verwendet die IDs der Back-End-IP-Konfiguration aus $NIC 01 und $NIC 02, um den Back-End-Adresspool des Anwendungs Gateways in $AppGw zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b4954-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="b4954-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4954-120">PARAMETERS</span></span>

### <span data-ttu-id="b4954-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4954-121">-ApplicationGateway</span></span>
<span data-ttu-id="b4954-122">Gibt das Anwendungsgateway an, mit dem dieses Cmdlet den Back-End-Adresspool verknüpft.</span><span class="sxs-lookup"><span data-stu-id="b4954-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="b4954-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="b4954-123">-BackendFqdns</span></span>
<span data-ttu-id="b4954-124">Gibt eine Liste der Back-End-IP-Adressen an, die als Back-End-Serverpool verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4954-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="b4954-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="b4954-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="b4954-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4954-126">-DefaultProfile</span></span>
<span data-ttu-id="b4954-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4954-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4954-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b4954-128">-Name</span></span>
<span data-ttu-id="b4954-129">Gibt den Namen des Back-End-Adresspools an.</span><span class="sxs-lookup"><span data-stu-id="b4954-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="b4954-130">Dieser Back-End-Adresspool muss im Application Gateway vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b4954-130">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="b4954-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4954-131">-Confirm</span></span>
<span data-ttu-id="b4954-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4954-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4954-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4954-133">-WhatIf</span></span>
<span data-ttu-id="b4954-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4954-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4954-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4954-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4954-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4954-136">CommonParameters</span></span>
<span data-ttu-id="b4954-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4954-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4954-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4954-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4954-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4954-139">INPUTS</span></span>

### <span data-ttu-id="b4954-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b4954-140">System.String</span></span>

## <span data-ttu-id="b4954-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4954-141">OUTPUTS</span></span>

### <span data-ttu-id="b4954-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4954-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4954-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4954-143">NOTES</span></span>

## <span data-ttu-id="b4954-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4954-144">RELATED LINKS</span></span>

[<span data-ttu-id="b4954-145">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4954-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b4954-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4954-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b4954-147">Neu – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4954-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b4954-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4954-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


