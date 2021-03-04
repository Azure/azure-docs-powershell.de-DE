---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 45cb703d6fdc87238f4d1ed35ada90aadeed501b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936763"
---
# <span data-ttu-id="b5f7d-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="b5f7d-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="b5f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f7d-103">Dieses Befehlslet gibt eine Liste der unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zurück.</span><span class="sxs-lookup"><span data-stu-id="b5f7d-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="b5f7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5f7d-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5f7d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f7d-106">Dieses Befehlslet gibt eine Liste der unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zurück.</span><span class="sxs-lookup"><span data-stu-id="b5f7d-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="b5f7d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="b5f7d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5f7d-108">Example 1</span></span>
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

<span data-ttu-id="b5f7d-109">Gibt eine Liste der unterstützten VPN-Gerätemarken, -Modelle und -Firmwareversionen zurück:</span><span class="sxs-lookup"><span data-stu-id="b5f7d-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="b5f7d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5f7d-110">PARAMETERS</span></span>

### <span data-ttu-id="b5f7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f7d-111">-DefaultProfile</span></span>
<span data-ttu-id="b5f7d-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5f7d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5f7d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b5f7d-113">-Name</span></span>
<span data-ttu-id="b5f7d-114">Der Name des Virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="b5f7d-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="b5f7d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f7d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5f7d-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5f7d-116">The resource group name.</span></span>

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

### <span data-ttu-id="b5f7d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f7d-117">CommonParameters</span></span>
<span data-ttu-id="b5f7d-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f7d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f7d-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5f7d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f7d-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5f7d-120">INPUTS</span></span>

### <span data-ttu-id="b5f7d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b5f7d-121">System.String</span></span>

## <span data-ttu-id="b5f7d-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5f7d-122">OUTPUTS</span></span>

### <span data-ttu-id="b5f7d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b5f7d-123">System.String</span></span>

## <span data-ttu-id="b5f7d-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5f7d-124">NOTES</span></span>

## <span data-ttu-id="b5f7d-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5f7d-125">RELATED LINKS</span></span>
