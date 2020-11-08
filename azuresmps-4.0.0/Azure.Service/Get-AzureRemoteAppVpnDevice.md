---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005832"
---
# <span data-ttu-id="61081-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="61081-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="61081-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61081-102">SYNOPSIS</span></span>
<span data-ttu-id="61081-103">Ruft Informationen zu einem VPN-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="61081-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="61081-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61081-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="61081-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61081-105">DESCRIPTION</span></span>
<span data-ttu-id="61081-106">Das Cmdlet " **Get-AzureRemoteAppVpnDevice** " Ruft Informationen zu einem VPN-Gerät (virtuelles privates Netzwerk) ab.</span><span class="sxs-lookup"><span data-stu-id="61081-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="61081-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61081-107">EXAMPLES</span></span>

### <span data-ttu-id="61081-108">Beispiel 1: Zurückgeben der verfügbaren VPN-Gerätekonfigurationen für ein virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="61081-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="61081-109">Dieser Befehl gibt die verfügbaren VPN-Gerätekonfigurationen für das angegebene virtuelle Netzwerk zurück.</span><span class="sxs-lookup"><span data-stu-id="61081-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="61081-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61081-110">PARAMETERS</span></span>

### <span data-ttu-id="61081-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="61081-111">-Profile</span></span>
<span data-ttu-id="61081-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="61081-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61081-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="61081-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61081-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="61081-114">-VNetName</span></span>
<span data-ttu-id="61081-115">Gibt den Namen des virtuellen Azure RemoteApp-Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="61081-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61081-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61081-116">CommonParameters</span></span>
<span data-ttu-id="61081-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61081-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61081-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61081-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61081-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61081-119">INPUTS</span></span>

## <span data-ttu-id="61081-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61081-120">OUTPUTS</span></span>

### <span data-ttu-id="61081-121">System. String</span><span class="sxs-lookup"><span data-stu-id="61081-121">System.String</span></span>

## <span data-ttu-id="61081-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="61081-122">NOTES</span></span>

## <span data-ttu-id="61081-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61081-123">RELATED LINKS</span></span>

[<span data-ttu-id="61081-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="61081-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="61081-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="61081-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


