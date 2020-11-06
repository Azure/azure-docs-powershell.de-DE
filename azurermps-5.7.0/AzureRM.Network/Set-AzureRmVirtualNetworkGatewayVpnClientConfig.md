---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 9ec81a9cf82851905d308fa0e0dd1fa45aeb7af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481098"
---
# <span data-ttu-id="2d5c7-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="2d5c7-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="2d5c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d5c7-103">Legt den VPN-Client Adresspool für ein virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d5c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d5c7-104">SYNTAX</span></span>

### <span data-ttu-id="2d5c7-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d5c7-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d5c7-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d5c7-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d5c7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d5c7-107">DESCRIPTION</span></span>
<span data-ttu-id="2d5c7-108">Das Cmdlet " **Satz-AzureRmVirtualNetworkVpnClientConfig** " konfiguriert den Client Adresspool für ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="2d5c7-109">VPN-Clients (virtuelles privates Netzwerk), die eine Verbindung mit diesem Gateway herstellen, wird aus diesem Adresspool eine IP-Adresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="2d5c7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d5c7-110">EXAMPLES</span></span>

### <span data-ttu-id="2d5c7-111">Beispiel 1: Zuweisen eines VPN-Client Adresspools zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="2d5c7-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="2d5c7-112">In diesem Beispiel wird ein VPN-Client Adresspool einem virtuellen Netzwerkgateway namens ContosoVirtualGateway zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="2d5c7-113">Der erste Befehl erstellt einen Objektverweis auf das Gateway, und das Objekt wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="2d5c7-114">Der zweite Befehl im Beispiel verwendet dann das Cmdlet " **AzureRmVirtualNetworkGatewayVpnClientConfig** ", um den Adresspool 10.0.0.0/16 zu ContosoVirtualGateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="2d5c7-115">Beispiel 2: Konfigurieren externer RADIUS-basierter Authentifizierung auf einem vorhandenen Gateway</span><span class="sxs-lookup"><span data-stu-id="2d5c7-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="2d5c7-116">In diesem Beispiel wird ein VPN-Client Adresspool einem virtuellen Netzwerkgateway namens ContosoVirtualGateway zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="2d5c7-117">Der erste Befehl erstellt einen Objektverweis auf das Gateway, und das Objekt wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="2d5c7-118">Der zweite Befehl im Beispiel verwendet dann das Cmdlet " **AzureRmVirtualNetworkGatewayVpnClientConfig** ", um den Adresspool 10.0.0.0/16 zu ContosoVirtualGateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="2d5c7-119">Außerdem wird der externe RADIUS-Server "TestRadiusServer" konfiguriert, der für die Authentifizierung für VPN-Clients verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="2d5c7-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d5c7-120">PARAMETERS</span></span>

### <span data-ttu-id="2d5c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d5c7-121">-DefaultProfile</span></span>
<span data-ttu-id="2d5c7-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d5c7-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2d5c7-123">-RadiusServerAddress</span></span>
<span data-ttu-id="2d5c7-124">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-124">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d5c7-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2d5c7-125">-RadiusServerSecret</span></span>
<span data-ttu-id="2d5c7-126">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-126">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d5c7-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d5c7-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="2d5c7-128">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, das die VPN-Clientkonfigurationseinstellungen enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="2d5c7-129">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den Get-AzureRmVirtualNetworkGateway verwenden und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d5c7-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="2d5c7-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="2d5c7-131">Gibt die IP-Adressen an, die Clients zugewiesen werden sollen, die mit diesem Gateway verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d5c7-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d5c7-132">-Confirm</span></span>
<span data-ttu-id="2d5c7-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d5c7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d5c7-134">-WhatIf</span></span>
<span data-ttu-id="2d5c7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d5c7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d5c7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d5c7-137">CommonParameters</span></span>
<span data-ttu-id="2d5c7-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d5c7-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d5c7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d5c7-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d5c7-140">INPUTS</span></span>

###  
<span data-ttu-id="2d5c7-141">Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="2d5c7-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d5c7-142">OUTPUTS</span></span>

###  
<span data-ttu-id="2d5c7-143">Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2d5c7-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="2d5c7-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d5c7-144">NOTES</span></span>

## <span data-ttu-id="2d5c7-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d5c7-145">RELATED LINKS</span></span>

[<span data-ttu-id="2d5c7-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="2d5c7-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="2d5c7-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d5c7-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2d5c7-148">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d5c7-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


