---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 794f432b06c693d6758603975a98ca6b2f5e3511
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841487"
---
# <span data-ttu-id="e3822-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="e3822-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="e3822-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3822-102">SYNOPSIS</span></span>
<span data-ttu-id="e3822-103">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="e3822-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="e3822-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3822-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3822-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3822-105">DESCRIPTION</span></span>
<span data-ttu-id="e3822-106">Dieser Unifiedgroup gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück.</span><span class="sxs-lookup"><span data-stu-id="e3822-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="e3822-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3822-107">EXAMPLES</span></span>

### <span data-ttu-id="e3822-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3822-108">Example 1</span></span>
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

<span data-ttu-id="e3822-109">Gibt eine Liste der unterstützten VPN-Gerätemarken,-Modelle und-Firmware-Versionen zurück:</span><span class="sxs-lookup"><span data-stu-id="e3822-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="e3822-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3822-110">PARAMETERS</span></span>

### <span data-ttu-id="e3822-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3822-111">-DefaultProfile</span></span>
<span data-ttu-id="e3822-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3822-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3822-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e3822-113">-Name</span></span>
<span data-ttu-id="e3822-114">Der Name des virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="e3822-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="e3822-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3822-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3822-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3822-116">The resource group name.</span></span>

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

### <span data-ttu-id="e3822-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3822-117">CommonParameters</span></span>
<span data-ttu-id="e3822-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3822-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3822-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3822-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3822-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3822-120">INPUTS</span></span>

### <span data-ttu-id="e3822-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e3822-121">System.String</span></span>

## <span data-ttu-id="e3822-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3822-122">OUTPUTS</span></span>

### <span data-ttu-id="e3822-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e3822-123">System.String</span></span>

## <span data-ttu-id="e3822-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3822-124">NOTES</span></span>

## <span data-ttu-id="e3822-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3822-125">RELATED LINKS</span></span>

