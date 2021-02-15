---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151876"
---
# <span data-ttu-id="d508f-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="d508f-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="d508f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d508f-102">SYNOPSIS</span></span>
<span data-ttu-id="d508f-103">Dieses Befehlslet übernimmt die Verbindungsressource, die Marke eines VPN-Geräts, das Modell und die Firmwareversion und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf ihre lokalen VPN-Geräte anwenden können.</span><span class="sxs-lookup"><span data-stu-id="d508f-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="d508f-104">Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter ein, z. B. öffentliche IP-Adressen des Azure-Gateways, Präfixe virtueller Netzwerkadressen, vorab freigegebenen #A0 usw. damit Kunden die #A1 einfach kopieren und einfügen können.</span><span class="sxs-lookup"><span data-stu-id="d508f-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="d508f-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d508f-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d508f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d508f-106">DESCRIPTION</span></span>
<span data-ttu-id="d508f-107">Dieses Befehlslet übernimmt die Verbindungsressource, die Marke eines VPN-Geräts, das Modell und die Firmwareversion und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf ihre lokalen VPN-Geräte anwenden können.</span><span class="sxs-lookup"><span data-stu-id="d508f-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="d508f-108">Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter ein, z. B. öffentliche IP-Adressen des Azure-Gateways, Präfixe virtueller Netzwerkadressen, vorab freigegebenen #A0 usw. damit Kunden die #A1 einfach kopieren und einfügen können.</span><span class="sxs-lookup"><span data-stu-id="d508f-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="d508f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d508f-109">EXAMPLES</span></span>

### <span data-ttu-id="d508f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d508f-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="d508f-111">Im vorstehenden Beispiel werden Get-AzVirtualNetworkGatewaySupportedVpnDevice verwendet, um die unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d508f-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="d508f-112">Anschließend wird eines der zurückgegebenen Modellinformationen verwendet, um ein VPN-Gerätekonfigurationsskript für das VirtualNetworkGatewayConnection-"TestConnection"-Skript zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d508f-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="d508f-113">Das in diesem Beispiel verwendete Gerät verfügt über DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" und FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="d508f-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="d508f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d508f-114">PARAMETERS</span></span>

### <span data-ttu-id="d508f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d508f-115">-DefaultProfile</span></span>
<span data-ttu-id="d508f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d508f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d508f-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="d508f-117">-DeviceFamily</span></span>
<span data-ttu-id="d508f-118">Name des MODELLS/der Familie des VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="d508f-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="d508f-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="d508f-119">-DeviceVendor</span></span>
<span data-ttu-id="d508f-120">Name des Vpn-Geräteanbieters.</span><span class="sxs-lookup"><span data-stu-id="d508f-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="d508f-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="d508f-121">-FirmwareVersion</span></span>
<span data-ttu-id="d508f-122">Firmwareversion des VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="d508f-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="d508f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d508f-123">-Name</span></span>
<span data-ttu-id="d508f-124">Der Ressourcenname der Verbindung, für die die Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d508f-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="d508f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d508f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d508f-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d508f-126">The resource group name.</span></span>

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

### <span data-ttu-id="d508f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d508f-127">-Confirm</span></span>
<span data-ttu-id="d508f-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d508f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d508f-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d508f-129">-WhatIf</span></span>
<span data-ttu-id="d508f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d508f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d508f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d508f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d508f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d508f-132">CommonParameters</span></span>
<span data-ttu-id="d508f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d508f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d508f-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d508f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d508f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d508f-135">INPUTS</span></span>

### <span data-ttu-id="d508f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d508f-136">System.String</span></span>

## <span data-ttu-id="d508f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d508f-137">OUTPUTS</span></span>

### <span data-ttu-id="d508f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d508f-138">System.String</span></span>

## <span data-ttu-id="d508f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d508f-139">NOTES</span></span>

## <span data-ttu-id="d508f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d508f-140">RELATED LINKS</span></span>
