---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996367"
---
# <span data-ttu-id="7322e-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="7322e-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="7322e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7322e-102">SYNOPSIS</span></span>
<span data-ttu-id="7322e-103">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="7322e-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="7322e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7322e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7322e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7322e-105">DESCRIPTION</span></span>
<span data-ttu-id="7322e-106">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="7322e-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="7322e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7322e-107">EXAMPLES</span></span>

### <span data-ttu-id="7322e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7322e-108">Example 1</span></span>
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

<span data-ttu-id="7322e-109">Gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück:</span><span class="sxs-lookup"><span data-stu-id="7322e-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="7322e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7322e-110">PARAMETERS</span></span>

### <span data-ttu-id="7322e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7322e-111">-DefaultProfile</span></span>
<span data-ttu-id="7322e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7322e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7322e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7322e-113">-Name</span></span>
<span data-ttu-id="7322e-114">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="7322e-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="7322e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7322e-115">-ResourceGroupName</span></span>
<span data-ttu-id="7322e-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7322e-116">The resource group name.</span></span>

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

### <span data-ttu-id="7322e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7322e-117">CommonParameters</span></span>
<span data-ttu-id="7322e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7322e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7322e-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7322e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7322e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7322e-120">INPUTS</span></span>

### <span data-ttu-id="7322e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7322e-121">System.String</span></span>

## <span data-ttu-id="7322e-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7322e-122">OUTPUTS</span></span>

### <span data-ttu-id="7322e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7322e-123">System.String</span></span>

## <span data-ttu-id="7322e-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="7322e-124">NOTES</span></span>

## <span data-ttu-id="7322e-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7322e-125">RELATED LINKS</span></span>
