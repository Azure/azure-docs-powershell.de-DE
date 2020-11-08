---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005696"
---
# <span data-ttu-id="c6a5a-101">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c6a5a-101">Remove-AzureVNetGateway</span></span>

## <span data-ttu-id="c6a5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a5a-103">Löscht ein VPN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="c6a5a-103">Deletes a VPN gateway.</span></span>

## <span data-ttu-id="c6a5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6a5a-104">SYNTAX</span></span>

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c6a5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a5a-106">Das Cmdlet **Remove-AzureVNetGateway** löscht ein vorhandenes virtuelles privates Netzwerk (VPN)-Gateway für ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c6a5a-106">The **Remove-AzureVNetGateway** cmdlet deletes an existing virtual private network (VPN) gateway for a virtual network.</span></span>

## <span data-ttu-id="c6a5a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a5a-108">Beispiel 1: Entfernen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="c6a5a-108">Example 1: Remove a virtual network gateway</span></span>
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="c6a5a-109">Dieser Befehl entfernt das virtuelle Netzwerkgateway aus dem virtuellen Netzwerk mit dem Namen ContosoVN07.</span><span class="sxs-lookup"><span data-stu-id="c6a5a-109">This command removes the virtual network gateway from the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="c6a5a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6a5a-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a5a-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="c6a5a-111">-Profile</span></span>
<span data-ttu-id="c6a5a-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c6a5a-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c6a5a-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c6a5a-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6a5a-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c6a5a-114">-VNetName</span></span>
<span data-ttu-id="c6a5a-115">Gibt das virtuelle Netzwerk an, in dem dieses Cmdlet das VPN-Gateway löscht.</span><span class="sxs-lookup"><span data-stu-id="c6a5a-115">Specifies the virtual network in which this cmdlet deletes the VPN gateway.</span></span>

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

### <span data-ttu-id="c6a5a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a5a-116">CommonParameters</span></span>
<span data-ttu-id="c6a5a-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a5a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a5a-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a5a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a5a-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6a5a-119">INPUTS</span></span>

## <span data-ttu-id="c6a5a-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6a5a-120">OUTPUTS</span></span>

## <span data-ttu-id="c6a5a-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6a5a-121">NOTES</span></span>

## <span data-ttu-id="c6a5a-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6a5a-122">RELATED LINKS</span></span>

[<span data-ttu-id="c6a5a-123">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c6a5a-123">Get-AzureVNetGateway</span></span>](./Get-AzureVNetGateway.md)

[<span data-ttu-id="c6a5a-124">Neu – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c6a5a-124">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="c6a5a-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c6a5a-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="c6a5a-126">Größe ändern – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="c6a5a-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="c6a5a-127">Satz-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="c6a5a-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


