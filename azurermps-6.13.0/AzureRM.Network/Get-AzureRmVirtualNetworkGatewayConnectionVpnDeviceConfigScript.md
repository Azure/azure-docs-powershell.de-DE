---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: abaaaf7d9f430bd1b7850f3141b651ac02821257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479498"
---
# <span data-ttu-id="1678b-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="1678b-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="1678b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1678b-102">SYNOPSIS</span></span>
<span data-ttu-id="1678b-103">Dieser Unifiedgroup übernimmt die Verbindungsressource, die Marke für das VPN-Gerät, das Modell, die Firmwareversion, und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf Ihren lokalen VPN-Geräten anwenden können.</span><span class="sxs-lookup"><span data-stu-id="1678b-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="1678b-104">Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter wie öffentliche IP-Adressen des Azure-Gateways, virtuelle Netzwerk Adresspräfixe, VPN-Tunnel-vorinstallierter Schlüssel usw. ein, sodass Kunden einfach in Ihre VPN-Gerätekonfigurationen kopieren können.</span><span class="sxs-lookup"><span data-stu-id="1678b-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1678b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1678b-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1678b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1678b-106">DESCRIPTION</span></span>
<span data-ttu-id="1678b-107">Dieser Unifiedgroup übernimmt die Verbindungsressource, die Marke für das VPN-Gerät, das Modell, die Firmwareversion, und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf Ihren lokalen VPN-Geräten anwenden können.</span><span class="sxs-lookup"><span data-stu-id="1678b-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="1678b-108">Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter wie öffentliche IP-Adressen des Azure-Gateways, virtuelle Netzwerk Adresspräfixe, VPN-Tunnel-vorinstallierter Schlüssel usw. ein, sodass Kunden einfach in Ihre VPN-Gerätekonfigurationen kopieren können.</span><span class="sxs-lookup"><span data-stu-id="1678b-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="1678b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1678b-109">EXAMPLES</span></span>

### <span data-ttu-id="1678b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1678b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="1678b-111">Im obigen Beispiel wird Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice verwendet, um die unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1678b-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="1678b-112">Verwendet dann eine der zurückgegebenen Modellinformationen, um ein VPN-Geräte Konfigurationsskript für das VirtualNetworkGatewayConnection "TestConnection" zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1678b-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="1678b-113">Das Gerät, das in diesem Beispiel verwendet wird, hat DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" und FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="1678b-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="1678b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1678b-114">PARAMETERS</span></span>

### <span data-ttu-id="1678b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1678b-115">-DefaultProfile</span></span>
<span data-ttu-id="1678b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1678b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1678b-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="1678b-117">-DeviceFamily</span></span>
<span data-ttu-id="1678b-118">Name des VPN-Gerätemodells/-Familie.</span><span class="sxs-lookup"><span data-stu-id="1678b-118">Name of the VPN device model/family.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1678b-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="1678b-119">-DeviceVendor</span></span>
<span data-ttu-id="1678b-120">Der Name des Anbieters für VPN-Geräte.</span><span class="sxs-lookup"><span data-stu-id="1678b-120">Name of the VPN device vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1678b-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="1678b-121">-FirmwareVersion</span></span>
<span data-ttu-id="1678b-122">Firmware-Version des VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="1678b-122">Firmware version of the VPN device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1678b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1678b-123">-Name</span></span>
<span data-ttu-id="1678b-124">Der Ressourcenname der Verbindung, für die die Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1678b-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1678b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1678b-125">-ResourceGroupName</span></span>
<span data-ttu-id="1678b-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1678b-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1678b-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1678b-127">-Confirm</span></span>
<span data-ttu-id="1678b-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1678b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1678b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1678b-129">-WhatIf</span></span>
<span data-ttu-id="1678b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1678b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1678b-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1678b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1678b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1678b-132">CommonParameters</span></span>
<span data-ttu-id="1678b-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1678b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1678b-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1678b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1678b-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1678b-135">INPUTS</span></span>

### <span data-ttu-id="1678b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1678b-136">System.String</span></span>

## <span data-ttu-id="1678b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1678b-137">OUTPUTS</span></span>

### <span data-ttu-id="1678b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1678b-138">System.String</span></span>

## <span data-ttu-id="1678b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="1678b-139">NOTES</span></span>

## <span data-ttu-id="1678b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1678b-140">RELATED LINKS</span></span>
