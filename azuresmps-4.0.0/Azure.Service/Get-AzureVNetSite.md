---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006733"
---
# <span data-ttu-id="d7fd7-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="d7fd7-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="d7fd7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fd7-103">Ruft ein Listenobjekt mit Informationen zu Azure Virtual Networks ab.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="d7fd7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7fd7-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7fd7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="d7fd7-106">Das Cmdlet " **Get-AzureVNetSite** " Ruft ein Listenobjekt mit Informationen zu Azure Virtual Networks für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="d7fd7-107">Wenn Sie einen virtuellen Netzwerknamen angeben, werden nur Informationen für dieses virtuelle Netzwerk zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="d7fd7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7fd7-108">EXAMPLES</span></span>

### <span data-ttu-id="d7fd7-109">Beispiel 1: Abrufen von Informationen zu allen virtuellen Netzwerken im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7fd7-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="d7fd7-110">Dieser Befehl ruft Informationen zu allen virtuellen Netzwerken im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="d7fd7-111">Beispiel 2: Abrufen von Informationen zu einem bestimmten virtuellen Netzwerk im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7fd7-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="d7fd7-112">Dieser Befehl ruft nur Informationen im virtuellen MyProductionNetwork-Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="d7fd7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7fd7-113">PARAMETERS</span></span>

### <span data-ttu-id="d7fd7-114">-Information</span><span class="sxs-lookup"><span data-stu-id="d7fd7-114">-InformationAction</span></span>
<span data-ttu-id="d7fd7-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d7fd7-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d7fd7-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7fd7-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d7fd7-117">Continue</span></span>
- <span data-ttu-id="d7fd7-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d7fd7-118">Ignore</span></span>
- <span data-ttu-id="d7fd7-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d7fd7-119">Inquire</span></span>
- <span data-ttu-id="d7fd7-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d7fd7-120">SilentlyContinue</span></span>
- <span data-ttu-id="d7fd7-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="d7fd7-121">Stop</span></span>
- <span data-ttu-id="d7fd7-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d7fd7-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fd7-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d7fd7-123">-InformationVariable</span></span>
<span data-ttu-id="d7fd7-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fd7-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="d7fd7-125">-Profile</span></span>
<span data-ttu-id="d7fd7-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7fd7-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7fd7-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d7fd7-128">-VNetName</span></span>
<span data-ttu-id="d7fd7-129">Gibt einen virtuellen Netzwerknamen an, zu dem Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fd7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fd7-130">CommonParameters</span></span>
<span data-ttu-id="d7fd7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7fd7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fd7-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7fd7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fd7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7fd7-133">INPUTS</span></span>

## <span data-ttu-id="d7fd7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7fd7-134">OUTPUTS</span></span>

## <span data-ttu-id="d7fd7-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7fd7-135">NOTES</span></span>

## <span data-ttu-id="d7fd7-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7fd7-136">RELATED LINKS</span></span>

[<span data-ttu-id="d7fd7-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="d7fd7-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="d7fd7-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="d7fd7-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="d7fd7-139">Satz-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="d7fd7-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


