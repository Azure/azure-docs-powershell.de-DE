---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4024D20D-46DF-4ED8-A091-E6E17F840E40
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c6ba8827906fbfc51b121e4500dea3ec4555d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006485"
---
# <span data-ttu-id="9c070-101">Get-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9c070-101">Get-AzureVNetGateway</span></span>

## <span data-ttu-id="9c070-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c070-102">SYNOPSIS</span></span>
<span data-ttu-id="9c070-103">Ruft den Status eines virtuellen Netzwerkgateways ab.</span><span class="sxs-lookup"><span data-stu-id="9c070-103">Gets the status of a virtual network gateway.</span></span>

## <span data-ttu-id="9c070-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c070-104">SYNTAX</span></span>

```
Get-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c070-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c070-105">DESCRIPTION</span></span>
<span data-ttu-id="9c070-106">Das Cmdlet " **Get-AzureVNetGateway** " Ruft den Status eines vorhandenen virtuellen Netzwerkgateways ab.</span><span class="sxs-lookup"><span data-stu-id="9c070-106">The **Get-AzureVNetGateway** cmdlet gets the status of an existing virtual network gateway.</span></span>

## <span data-ttu-id="9c070-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c070-107">EXAMPLES</span></span>

### <span data-ttu-id="9c070-108">Beispiel 1: Abrufen des Status eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="9c070-108">Example 1: Get the status of a virtual network gateway</span></span>
```
PS C:\> Get-AzureVNetGateway -VNetName "ContosoVN07"
```

<span data-ttu-id="9c070-109">Dieser Befehl ruft diesen Status des virtuellen Netzwerkgateways für das virtuelle Netzwerk mit dem Namen ContosoVN07 ab.</span><span class="sxs-lookup"><span data-stu-id="9c070-109">This command gets that status of the virtual network gateway for the virtual network named ContosoVN07.</span></span>

## <span data-ttu-id="9c070-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c070-110">PARAMETERS</span></span>

### <span data-ttu-id="9c070-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="9c070-111">-Profile</span></span>
<span data-ttu-id="9c070-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9c070-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9c070-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9c070-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c070-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9c070-114">-VNetName</span></span>
<span data-ttu-id="9c070-115">Gibt das virtuelle Netzwerk an, das das virtuelle Netzwerkgateway enthält, für das dieses Cmdlet den Status erhält.</span><span class="sxs-lookup"><span data-stu-id="9c070-115">Specifies the virtual network that contains the virtual network gateway for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="9c070-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c070-116">CommonParameters</span></span>
<span data-ttu-id="9c070-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c070-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c070-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c070-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c070-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c070-119">INPUTS</span></span>

## <span data-ttu-id="9c070-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c070-120">OUTPUTS</span></span>

## <span data-ttu-id="9c070-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c070-121">NOTES</span></span>

## <span data-ttu-id="9c070-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c070-122">RELATED LINKS</span></span>

[<span data-ttu-id="9c070-123">Neu – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9c070-123">New-AzureVNetGateway</span></span>](./New-AzureVNetGateway.md)

[<span data-ttu-id="9c070-124">Remove-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9c070-124">Remove-AzureVNetGateway</span></span>](./Remove-AzureVNetGateway.md)

[<span data-ttu-id="9c070-125">Reset-AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9c070-125">Reset-AzureVNetGateway</span></span>](./Reset-AzureVNetGateway.md)

[<span data-ttu-id="9c070-126">Größe ändern – AzureVNetGateway</span><span class="sxs-lookup"><span data-stu-id="9c070-126">Resize-AzureVNetGateway</span></span>](./Resize-AzureVNetGateway.md)

[<span data-ttu-id="9c070-127">Satz-AzureVNetGatewayKey</span><span class="sxs-lookup"><span data-stu-id="9c070-127">Set-AzureVNetGatewayKey</span></span>](./Set-AzureVNetGatewayKey.md)


