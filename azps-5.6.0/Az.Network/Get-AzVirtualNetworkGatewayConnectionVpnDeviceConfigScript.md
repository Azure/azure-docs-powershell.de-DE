---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931760"
---
# <span data-ttu-id="38f44-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="38f44-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="38f44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f44-102">SYNOPSIS</span></span>
<span data-ttu-id="38f44-103">Dieses Befehlslet übernimmt die Verbindungsressource, die Marke des VPN-Geräts, das Modell, die Firmwareversion und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf ihre lokalen VPN-Geräte anwenden können.</span><span class="sxs-lookup"><span data-stu-id="38f44-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="38f44-104">Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter ein, z. B. öffentliche #A0 des Azure-Gateways, Virtuelle Netzwerkadressenpräfixe, vorab freigegebenen VPN-Tunnelschlüssel usw., damit Kunden das Einfügen einfach in ihre #A1 kopieren können.</span><span class="sxs-lookup"><span data-stu-id="38f44-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="38f44-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38f44-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f44-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38f44-106">DESCRIPTION</span></span>
<span data-ttu-id="38f44-107">Dieses Befehlslet übernimmt die Verbindungsressource, die Marke des VPN-Geräts, das Modell, die Firmwareversion und gibt das entsprechende Konfigurationsskript zurück, das Kunden direkt auf ihre lokalen VPN-Geräte anwenden können.</span><span class="sxs-lookup"><span data-stu-id="38f44-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="38f44-108">Das Skript folgt der Syntax des ausgewählten Geräts und fügt die erforderlichen Parameter ein, z. B. öffentliche #A0 des Azure-Gateways, Virtuelle Netzwerkadressenpräfixe, vorab freigegebenen VPN-Tunnelschlüssel usw., damit Kunden das Einfügen einfach in ihre #A1 kopieren können.</span><span class="sxs-lookup"><span data-stu-id="38f44-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="38f44-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38f44-109">EXAMPLES</span></span>

### <span data-ttu-id="38f44-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38f44-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="38f44-111">Im vorstehenden Beispiel werden Get-AzVirtualNetworkGatewaySupportedVpnDevice verwendet, um die unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38f44-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="38f44-112">Anschließend wird eine der zurückgegebenen Modellinformationen verwendet, um ein VPN-Gerätekonfigurationsskript für die VirtualNetworkGatewayConnection "TestConnection" zu generieren.</span><span class="sxs-lookup"><span data-stu-id="38f44-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="38f44-113">Das in diesem Beispiel verwendete Gerät verfügt über DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" und FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="38f44-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="38f44-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="38f44-114">PARAMETERS</span></span>

### <span data-ttu-id="38f44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f44-115">-DefaultProfile</span></span>
<span data-ttu-id="38f44-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38f44-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f44-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="38f44-117">-DeviceFamily</span></span>
<span data-ttu-id="38f44-118">Name des VPN-Gerätemodells/der Familie.</span><span class="sxs-lookup"><span data-stu-id="38f44-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="38f44-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="38f44-119">-DeviceVendor</span></span>
<span data-ttu-id="38f44-120">Name des Anbieters des VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="38f44-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="38f44-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="38f44-121">-FirmwareVersion</span></span>
<span data-ttu-id="38f44-122">Firmwareversion des VPN-Geräts.</span><span class="sxs-lookup"><span data-stu-id="38f44-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="38f44-123">-Name</span><span class="sxs-lookup"><span data-stu-id="38f44-123">-Name</span></span>
<span data-ttu-id="38f44-124">Der Ressourcenname der Verbindung, für die die Konfiguration generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38f44-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="38f44-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f44-125">-ResourceGroupName</span></span>
<span data-ttu-id="38f44-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="38f44-126">The resource group name.</span></span>

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

### <span data-ttu-id="38f44-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38f44-127">-Confirm</span></span>
<span data-ttu-id="38f44-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38f44-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f44-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f44-129">-WhatIf</span></span>
<span data-ttu-id="38f44-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38f44-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f44-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38f44-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f44-132">CommonParameters</span></span>
<span data-ttu-id="38f44-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f44-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38f44-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f44-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38f44-135">INPUTS</span></span>

### <span data-ttu-id="38f44-136">System.String</span><span class="sxs-lookup"><span data-stu-id="38f44-136">System.String</span></span>

## <span data-ttu-id="38f44-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38f44-137">OUTPUTS</span></span>

### <span data-ttu-id="38f44-138">System.String</span><span class="sxs-lookup"><span data-stu-id="38f44-138">System.String</span></span>

## <span data-ttu-id="38f44-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="38f44-139">NOTES</span></span>

## <span data-ttu-id="38f44-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="38f44-140">RELATED LINKS</span></span>
