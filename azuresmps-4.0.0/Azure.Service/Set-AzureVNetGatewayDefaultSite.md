---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006619"
---
# <span data-ttu-id="5fd22-101">Set-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5fd22-101">Set-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="5fd22-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5fd22-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd22-103">Legt die Standardwebsite für erzwungenen Tunneling-Datenverkehr fest.</span><span class="sxs-lookup"><span data-stu-id="5fd22-103">Sets the default site for forced tunneling traffic.</span></span>

## <span data-ttu-id="5fd22-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fd22-104">SYNTAX</span></span>

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fd22-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fd22-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd22-106">Das Cmdlet " **Set-AzureVNetGatewayDefaultSite** " legt die Standardroute zur lokalen Website für erzwungenen Tunneling-Datenverkehr fest.</span><span class="sxs-lookup"><span data-stu-id="5fd22-106">The **Set-AzureVNetGatewayDefaultSite** cmdlet sets the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="5fd22-107">Dieser Befehl legt die Route auf einem Azure Virtual Private Network (VPN)-Gateway für ein virtuelles Netzwerk fest.</span><span class="sxs-lookup"><span data-stu-id="5fd22-107">This command sets the route on an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="5fd22-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fd22-108">EXAMPLES</span></span>

## <span data-ttu-id="5fd22-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fd22-109">PARAMETERS</span></span>

### <span data-ttu-id="5fd22-110">-DefaultSite</span><span class="sxs-lookup"><span data-stu-id="5fd22-110">-DefaultSite</span></span>
<span data-ttu-id="5fd22-111">Gibt den Namen der lokalen lokalen Netzwerk Website für erzwungenen Tunneling-Datenverkehr an.</span><span class="sxs-lookup"><span data-stu-id="5fd22-111">Specifies the name of the on-premises local network site for forced tunneling traffic.</span></span>

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

### <span data-ttu-id="5fd22-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="5fd22-112">-Profile</span></span>
<span data-ttu-id="5fd22-113">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5fd22-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fd22-114">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5fd22-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fd22-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="5fd22-115">-VNetName</span></span>
<span data-ttu-id="5fd22-116">Gibt ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="5fd22-116">Specifies a virtual network.</span></span>
<span data-ttu-id="5fd22-117">Mit diesem Cmdlet wird die Standardroute des VPN-Gateways für erzwungenen Tunneling-Datenverkehr für das virtuelle Netzwerk festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5fd22-117">This cmdlet sets the default route of the VPN gateway for forced tunneling traffic for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="5fd22-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd22-118">CommonParameters</span></span>
<span data-ttu-id="5fd22-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd22-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd22-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd22-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd22-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5fd22-121">INPUTS</span></span>

## <span data-ttu-id="5fd22-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5fd22-122">OUTPUTS</span></span>

## <span data-ttu-id="5fd22-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="5fd22-123">NOTES</span></span>

## <span data-ttu-id="5fd22-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5fd22-124">RELATED LINKS</span></span>

[<span data-ttu-id="5fd22-125">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="5fd22-125">Remove-AzureVNetGatewayDefaultSite</span></span>](./Remove-AzureVNetGatewayDefaultSite.md)
