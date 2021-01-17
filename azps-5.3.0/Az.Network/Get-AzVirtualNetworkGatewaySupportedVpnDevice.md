---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380987"
---
# <span data-ttu-id="c40d6-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="c40d6-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="c40d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c40d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c40d6-103">Dieses Befehlslet gibt eine Liste der unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zurück.</span><span class="sxs-lookup"><span data-stu-id="c40d6-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="c40d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c40d6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c40d6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c40d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c40d6-106">Dieses Befehlslet gibt eine Liste der unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zurück.</span><span class="sxs-lookup"><span data-stu-id="c40d6-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="c40d6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c40d6-107">EXAMPLES</span></span>

### <span data-ttu-id="c40d6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c40d6-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="c40d6-109">Gibt eine Liste der unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zurück:</span><span class="sxs-lookup"><span data-stu-id="c40d6-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="c40d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c40d6-110">PARAMETERS</span></span>

### <span data-ttu-id="c40d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40d6-111">-DefaultProfile</span></span>
<span data-ttu-id="c40d6-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c40d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c40d6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c40d6-113">-Name</span></span>
<span data-ttu-id="c40d6-114">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="c40d6-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="c40d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c40d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="c40d6-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c40d6-116">The resource group name.</span></span>

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

### <span data-ttu-id="c40d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40d6-117">CommonParameters</span></span>
<span data-ttu-id="c40d6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40d6-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c40d6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40d6-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c40d6-120">INPUTS</span></span>

### <span data-ttu-id="c40d6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c40d6-121">System.String</span></span>

## <span data-ttu-id="c40d6-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c40d6-122">OUTPUTS</span></span>

### <span data-ttu-id="c40d6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c40d6-123">System.String</span></span>

## <span data-ttu-id="c40d6-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c40d6-124">NOTES</span></span>

## <span data-ttu-id="c40d6-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c40d6-125">RELATED LINKS</span></span>
