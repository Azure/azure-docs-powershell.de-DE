---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005695"
---
# <span data-ttu-id="b873b-101">Remove-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b873b-101">Remove-AzureVNetGatewayDefaultSite</span></span>

## <span data-ttu-id="b873b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b873b-102">SYNOPSIS</span></span>
<span data-ttu-id="b873b-103">Entfernt die Standardroute für erzwungenen Tunneling-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="b873b-103">Removes the default route for forced tunneling traffic.</span></span>

## <span data-ttu-id="b873b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b873b-104">SYNTAX</span></span>

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b873b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b873b-105">DESCRIPTION</span></span>
<span data-ttu-id="b873b-106">Das Cmdlet **Remove-AzureVNetGatewayDefaultSite** entfernt die Standardroute zur lokalen Website für erzwungenen Tunneling-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="b873b-106">The **Remove-AzureVNetGatewayDefaultSite** cmdlet removes the default route to the on-premises site for forced tunneling traffic.</span></span>
<span data-ttu-id="b873b-107">Dieses Cmdlet entfernt die Route von einem Azure Virtual Private Network (VPN)-Gateway für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b873b-107">This cmdlet removes the route from an Azure virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="b873b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b873b-108">EXAMPLES</span></span>

### <span data-ttu-id="b873b-109">Beispiel 1: Entfernen einer Route zur Standardwebsite</span><span class="sxs-lookup"><span data-stu-id="b873b-109">Example 1: Remove a route to the default site</span></span>
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

<span data-ttu-id="b873b-110">Dieser Befehl entfernt die Route zur Standardwebsite aus dem VPN des virtuellen Netzwerks mit dem Namen ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="b873b-110">This command removes the route to the default site from the VPN of the virtual network named ContosoVNet01.</span></span>

## <span data-ttu-id="b873b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b873b-111">PARAMETERS</span></span>

### <span data-ttu-id="b873b-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="b873b-112">-Profile</span></span>
<span data-ttu-id="b873b-113">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b873b-113">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b873b-114">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b873b-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b873b-115">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b873b-115">-VNetName</span></span>
<span data-ttu-id="b873b-116">Gibt ein virtuelles Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="b873b-116">Specifies a virtual network.</span></span>
<span data-ttu-id="b873b-117">Dieses Cmdlet entfernt die Standardroute aus dem VPN-Gateway für das virtuelle Netzwerk, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b873b-117">This cmdlet removes the default route from the VPN gateway for the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="b873b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b873b-118">CommonParameters</span></span>
<span data-ttu-id="b873b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b873b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b873b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b873b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b873b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b873b-121">INPUTS</span></span>

## <span data-ttu-id="b873b-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b873b-122">OUTPUTS</span></span>

## <span data-ttu-id="b873b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="b873b-123">NOTES</span></span>

## <span data-ttu-id="b873b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b873b-124">RELATED LINKS</span></span>

[<span data-ttu-id="b873b-125">Satz-AzureVNetGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b873b-125">Set-AzureVNetGatewayDefaultSite</span></span>](./Set-AzureVNetGatewayDefaultSite.md)
