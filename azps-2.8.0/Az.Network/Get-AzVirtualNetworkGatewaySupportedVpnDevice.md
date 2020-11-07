---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 0ff95b3e212e61b3d8c9d01b0ad745963d7b24e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821724"
---
# <span data-ttu-id="7bd81-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="7bd81-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="7bd81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bd81-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd81-103">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="7bd81-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="7bd81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bd81-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bd81-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bd81-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd81-106">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="7bd81-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="7bd81-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bd81-107">EXAMPLES</span></span>

### <span data-ttu-id="7bd81-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bd81-108">Example 1</span></span>
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

<span data-ttu-id="7bd81-109">Gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück:</span><span class="sxs-lookup"><span data-stu-id="7bd81-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="7bd81-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bd81-110">PARAMETERS</span></span>

### <span data-ttu-id="7bd81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd81-111">-DefaultProfile</span></span>
<span data-ttu-id="7bd81-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bd81-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bd81-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd81-113">-Name</span></span>
<span data-ttu-id="7bd81-114">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="7bd81-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="7bd81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd81-115">-ResourceGroupName</span></span>
<span data-ttu-id="7bd81-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7bd81-116">The resource group name.</span></span>

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

### <span data-ttu-id="7bd81-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd81-117">CommonParameters</span></span>
<span data-ttu-id="7bd81-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd81-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd81-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bd81-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd81-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bd81-120">INPUTS</span></span>

### <span data-ttu-id="7bd81-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7bd81-121">System.String</span></span>

## <span data-ttu-id="7bd81-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bd81-122">OUTPUTS</span></span>

### <span data-ttu-id="7bd81-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7bd81-123">System.String</span></span>

## <span data-ttu-id="7bd81-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bd81-124">NOTES</span></span>

## <span data-ttu-id="7bd81-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bd81-125">RELATED LINKS</span></span>
