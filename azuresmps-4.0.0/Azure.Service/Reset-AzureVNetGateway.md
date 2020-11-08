---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005671"
---
# <span data-ttu-id="87345-101">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="87345-101">Reset-AzureVNetGateway</span></span>

## <span data-ttu-id="87345-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87345-102">SYNOPSIS</span></span>
<span data-ttu-id="87345-103">Setzt ein virtuelles Netzwerk-VPN-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="87345-103">Resets a virtual network VPN gateway.</span></span>

## <span data-ttu-id="87345-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87345-104">SYNTAX</span></span>

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="87345-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87345-105">DESCRIPTION</span></span>
<span data-ttu-id="87345-106">Mit dem Cmdlet **Reset-AzureVNetGateway** wird ein virtuelles privates Netzwerk (virtuelles privates Netzwerk)-virtuelles Netzwerk-Gateway zurückgesetzt und neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="87345-106">The **Reset-AzureVNetGateway** cmdlet resets and restarts a virtual private network (VPN) virtual network gateway.</span></span>

## <span data-ttu-id="87345-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87345-107">EXAMPLES</span></span>

### <span data-ttu-id="87345-108">Beispiel 1: Zurücksetzen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="87345-108">Example 1: Reset a virtual network gateway</span></span>
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="87345-109">Mit diesem Befehl wird das virtuelle Netzwerkgateway aus dem virtuellen Netzwerk mit dem Namen ContosoVN07 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="87345-109">This command resets the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="87345-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="87345-110">PARAMETERS</span></span>

### <span data-ttu-id="87345-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="87345-111">-Profile</span></span>
<span data-ttu-id="87345-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="87345-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="87345-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="87345-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87345-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="87345-114">-VNetName</span></span>
<span data-ttu-id="87345-115">Gibt das virtuelle Netzwerk an, das das virtuelle Netzwerkgateway enthält, das von diesem Cmdlet zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="87345-115">Specifies the virtual network that contains the virtual network gateway that this cmdlet resets.</span></span>

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

### <span data-ttu-id="87345-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87345-116">CommonParameters</span></span>
<span data-ttu-id="87345-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87345-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87345-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87345-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87345-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87345-119">INPUTS</span></span>

## <span data-ttu-id="87345-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87345-120">OUTPUTS</span></span>

## <span data-ttu-id="87345-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="87345-121">NOTES</span></span>

## <span data-ttu-id="87345-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87345-122">RELATED LINKS</span></span>

[<span data-ttu-id="87345-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="87345-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="87345-124">Neu – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="87345-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="87345-125">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="87345-125">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="87345-126">Größe ändern – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="87345-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="87345-127">Satz-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="87345-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


