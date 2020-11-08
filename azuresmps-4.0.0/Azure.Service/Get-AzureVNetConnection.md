---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7B749B29-9820-4E23-B5AF-F5535251629A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec94df29fb23dd7c82d79304c2e48aab225ed224
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006493"
---
# <span data-ttu-id="e74d4-101">Get-AzureVNetConnection</span><span class="sxs-lookup"><span data-stu-id="e74d4-101">Get-AzureVNetConnection</span></span>

## <span data-ttu-id="e74d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e74d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e74d4-103">Ruft Verbindungen mit einem virtuellen Azure-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="e74d4-103">Gets connections to an Azure virtual network.</span></span>

## <span data-ttu-id="e74d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e74d4-104">SYNTAX</span></span>

```
Get-AzureVNetConnection -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e74d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e74d4-105">DESCRIPTION</span></span>
<span data-ttu-id="e74d4-106">Das Cmdlet " **Get-AzureVNetConnection** " gibt ein Objekt zurück, das alle aktiven VPN-Verbindungen (virtuelles privates Netzwerk) mit einem virtuellen Azure-Netzwerk angibt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-106">The **Get-AzureVNetConnection** cmdlet returns an object that specifies all active virtual private network (VPN) connections to an Azure virtual network.</span></span>
<span data-ttu-id="e74d4-107">Zu den VPN-Verbindungen gehören Orts-zu-Standort-VPNs und virtuelles Netzwerk zu virtuellen Netzwerkverbindungen.</span><span class="sxs-lookup"><span data-stu-id="e74d4-107">VPN connections include cross premises site-to-site VPNs and virtual network to virtual network connections.</span></span>

## <span data-ttu-id="e74d4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e74d4-108">EXAMPLES</span></span>

## <span data-ttu-id="e74d4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e74d4-109">PARAMETERS</span></span>

### <span data-ttu-id="e74d4-110">-Profil</span><span class="sxs-lookup"><span data-stu-id="e74d4-110">-Profile</span></span>
<span data-ttu-id="e74d4-111">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e74d4-111">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e74d4-112">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e74d4-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e74d4-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e74d4-113">-VNetName</span></span>
<span data-ttu-id="e74d4-114">Gibt den Namen des virtuellen Netzwerks an, von dem dieses Cmdlet Verbindungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e74d4-114">Specifies the name of the virtual network from which this cmdlet returns connections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e74d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e74d4-115">CommonParameters</span></span>
<span data-ttu-id="e74d4-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e74d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e74d4-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e74d4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e74d4-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e74d4-118">INPUTS</span></span>

## <span data-ttu-id="e74d4-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e74d4-119">OUTPUTS</span></span>

## <span data-ttu-id="e74d4-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="e74d4-120">NOTES</span></span>

## <span data-ttu-id="e74d4-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e74d4-121">RELATED LINKS</span></span>

