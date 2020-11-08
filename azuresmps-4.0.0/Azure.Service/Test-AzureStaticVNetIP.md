---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006142"
---
# <span data-ttu-id="3f26f-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="3f26f-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="3f26f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f26f-102">SYNOPSIS</span></span>
<span data-ttu-id="3f26f-103">Testet die Verfügbarkeit einer statischen virtuellen Netzwerk-IP-Adresse und ruft eine Liste mit Vorschlägen ab, wenn die abgefragte Adresse nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f26f-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="3f26f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f26f-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3f26f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f26f-105">DESCRIPTION</span></span>
<span data-ttu-id="3f26f-106">Das Cmdlet **Test-AzureStaticVNetIP** testet die Verfügbarkeit einer statischen virtuellen Netzwerk-IP-Adresse und ruft eine Liste mit Vorschlägen ab, wenn die abgefragte Adresse nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f26f-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="3f26f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f26f-107">EXAMPLES</span></span>

### <span data-ttu-id="3f26f-108">1:</span><span class="sxs-lookup"><span data-stu-id="3f26f-108">1:</span></span>
```

```

## <span data-ttu-id="3f26f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f26f-109">PARAMETERS</span></span>

### <span data-ttu-id="3f26f-110">-Information</span><span class="sxs-lookup"><span data-stu-id="3f26f-110">-InformationAction</span></span>
<span data-ttu-id="3f26f-111">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="3f26f-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f26f-112">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3f26f-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f26f-113">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="3f26f-113">Continue</span></span>
- <span data-ttu-id="3f26f-114">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="3f26f-114">Ignore</span></span>
- <span data-ttu-id="3f26f-115">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="3f26f-115">Inquire</span></span>
- <span data-ttu-id="3f26f-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f26f-116">SilentlyContinue</span></span>
- <span data-ttu-id="3f26f-117">Beenden</span><span class="sxs-lookup"><span data-stu-id="3f26f-117">Stop</span></span>
- <span data-ttu-id="3f26f-118">Anhalten</span><span class="sxs-lookup"><span data-stu-id="3f26f-118">Suspend</span></span>

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

### <span data-ttu-id="3f26f-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f26f-119">-InformationVariable</span></span>
<span data-ttu-id="3f26f-120">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="3f26f-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3f26f-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="3f26f-121">-IPAddress</span></span>
<span data-ttu-id="3f26f-122">Gibt die statische IP-Adresse des virtuellen Netzwerks an, die abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f26f-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f26f-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f26f-123">-Profile</span></span>
<span data-ttu-id="3f26f-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3f26f-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f26f-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3f26f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f26f-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="3f26f-126">-VNetName</span></span>
<span data-ttu-id="3f26f-127">Gibt den Namen des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="3f26f-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f26f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f26f-128">CommonParameters</span></span>
<span data-ttu-id="3f26f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f26f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f26f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f26f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f26f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f26f-131">INPUTS</span></span>

## <span data-ttu-id="3f26f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f26f-132">OUTPUTS</span></span>

## <span data-ttu-id="3f26f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f26f-133">NOTES</span></span>

## <span data-ttu-id="3f26f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f26f-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f26f-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="3f26f-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="3f26f-136">Satz-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="3f26f-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


