---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482193"
---
# <span data-ttu-id="60d05-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="60d05-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="60d05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60d05-102">SYNOPSIS</span></span>
<span data-ttu-id="60d05-103">Legt den VPN-Client Adresspool für ein virtuelles Netzwerkgateway fest.</span><span class="sxs-lookup"><span data-stu-id="60d05-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60d05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60d05-104">SYNTAX</span></span>

### <span data-ttu-id="60d05-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="60d05-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60d05-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="60d05-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60d05-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60d05-107">DESCRIPTION</span></span>
<span data-ttu-id="60d05-108">Das Cmdlet " **Satz-AzureRmVirtualNetworkVpnClientConfig** " konfiguriert den Client Adresspool für ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="60d05-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="60d05-109">VPN-Clients (virtuelles privates Netzwerk), die eine Verbindung mit diesem Gateway herstellen, wird aus diesem Adresspool eine IP-Adresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="60d05-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="60d05-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60d05-110">EXAMPLES</span></span>

### <span data-ttu-id="60d05-111">Beispiel 1: Zuweisen eines VPN-Client Adresspools zu einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="60d05-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="60d05-112">In diesem Beispiel wird ein VPN-Client Adresspool einem virtuellen Netzwerkgateway namens ContosoVirtualGateway zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="60d05-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="60d05-113">Der erste Befehl erstellt einen Objektverweis auf das Gateway, und das Objekt wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="60d05-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="60d05-114">Der zweite Befehl im Beispiel verwendet dann das Cmdlet " **AzureRmVirtualNetworkGatewayVpnClientConfig** ", um den Adresspool 10.0.0.0/16 zu ContosoVirtualGateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="60d05-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="60d05-115">Beispiel 2: Konfigurieren externer RADIUS-basierter Authentifizierung auf einem vorhandenen Gateway</span><span class="sxs-lookup"><span data-stu-id="60d05-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="60d05-116">In diesem Beispiel wird ein VPN-Client Adresspool einem virtuellen Netzwerkgateway namens ContosoVirtualGateway zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="60d05-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="60d05-117">Der erste Befehl erstellt einen Objektverweis auf das Gateway, und das Objekt wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="60d05-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="60d05-118">Der zweite Befehl im Beispiel verwendet dann das Cmdlet " **AzureRmVirtualNetworkGatewayVpnClientConfig** ", um den Adresspool 10.0.0.0/16 zu ContosoVirtualGateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="60d05-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="60d05-119">Außerdem wird der externe RADIUS-Server "TestRadiusServer" konfiguriert, der für die Authentifizierung für VPN-Clients verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="60d05-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="60d05-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="60d05-120">PARAMETERS</span></span>

### <span data-ttu-id="60d05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d05-121">-DefaultProfile</span></span>
<span data-ttu-id="60d05-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60d05-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60d05-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="60d05-123">-RadiusServerAddress</span></span>
<span data-ttu-id="60d05-124">P2S-externe RADIUS-Serveradresse.</span><span class="sxs-lookup"><span data-stu-id="60d05-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d05-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="60d05-125">-RadiusServerSecret</span></span>
<span data-ttu-id="60d05-126">P2S externer RADIUS-Server-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="60d05-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d05-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60d05-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="60d05-128">Gibt einen Objektverweis auf das virtuelle Netzwerkgateway an, das die VPN-Clientkonfigurationseinstellungen enthält, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="60d05-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="60d05-129">Sie können einen Objektverweis auf ein virtuelles Netzwerkgateway erstellen, indem Sie den Get-AzureRmVirtualNetworkGateway verwenden und den Namen des Gateways angeben.</span><span class="sxs-lookup"><span data-stu-id="60d05-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60d05-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="60d05-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="60d05-131">Gibt die IP-Adressen an, die Clients zugewiesen werden sollen, die mit diesem Gateway verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="60d05-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="60d05-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60d05-132">-Confirm</span></span>
<span data-ttu-id="60d05-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60d05-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60d05-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60d05-134">-WhatIf</span></span>
<span data-ttu-id="60d05-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60d05-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60d05-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60d05-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60d05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d05-137">CommonParameters</span></span>
<span data-ttu-id="60d05-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d05-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60d05-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d05-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60d05-140">INPUTS</span></span>

### <span data-ttu-id="60d05-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60d05-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="60d05-142">Parameter: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60d05-142">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="60d05-143">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="60d05-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="60d05-144">System. String</span><span class="sxs-lookup"><span data-stu-id="60d05-144">System.String</span></span>

### <span data-ttu-id="60d05-145">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="60d05-145">System.Security.SecureString</span></span>

## <span data-ttu-id="60d05-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60d05-146">OUTPUTS</span></span>

### <span data-ttu-id="60d05-147">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60d05-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="60d05-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="60d05-148">NOTES</span></span>

## <span data-ttu-id="60d05-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60d05-149">RELATED LINKS</span></span>

[<span data-ttu-id="60d05-150">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="60d05-150">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="60d05-151">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60d05-151">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="60d05-152">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="60d05-152">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


