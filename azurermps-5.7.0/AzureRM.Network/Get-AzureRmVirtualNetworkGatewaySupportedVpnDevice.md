---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 30937c856d1961a1f342c73588aa00c74790ec81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662839"
---
# <span data-ttu-id="80cee-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="80cee-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="80cee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80cee-102">SYNOPSIS</span></span>
<span data-ttu-id="80cee-103">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="80cee-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80cee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80cee-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80cee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80cee-105">DESCRIPTION</span></span>
<span data-ttu-id="80cee-106">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="80cee-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="80cee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80cee-107">EXAMPLES</span></span>

### <span data-ttu-id="80cee-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80cee-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="80cee-109">Gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück:</span><span class="sxs-lookup"><span data-stu-id="80cee-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="80cee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80cee-110">PARAMETERS</span></span>

### <span data-ttu-id="80cee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80cee-111">-DefaultProfile</span></span>
<span data-ttu-id="80cee-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80cee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80cee-113">-Name</span><span class="sxs-lookup"><span data-stu-id="80cee-113">-Name</span></span>
<span data-ttu-id="80cee-114">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="80cee-114">The virtual network gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80cee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80cee-115">-ResourceGroupName</span></span>
<span data-ttu-id="80cee-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="80cee-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80cee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80cee-117">CommonParameters</span></span>
<span data-ttu-id="80cee-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80cee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80cee-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80cee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80cee-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80cee-120">INPUTS</span></span>

### <span data-ttu-id="80cee-121">System. String</span><span class="sxs-lookup"><span data-stu-id="80cee-121">System.String</span></span>

## <span data-ttu-id="80cee-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80cee-122">OUTPUTS</span></span>

### <span data-ttu-id="80cee-123">System. String</span><span class="sxs-lookup"><span data-stu-id="80cee-123">System.String</span></span>

## <span data-ttu-id="80cee-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="80cee-124">NOTES</span></span>

## <span data-ttu-id="80cee-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80cee-125">RELATED LINKS</span></span>

