---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005824"
---
# <span data-ttu-id="fb6cd-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="fb6cd-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="fb6cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6cd-103">Ruft eine reservierte IP-Adresse anhand ihres Namens ab oder listet alle reservierten IP-Adressen im Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="fb6cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb6cd-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fb6cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb6cd-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6cd-106">Das Cmdlet " **Get-AzureReservedIP** " Ruft eine reservierte IP-Adresse mit dem Namen ab oder listet alle reservierten IP-Adressen im Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="fb6cd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb6cd-107">EXAMPLES</span></span>

### <span data-ttu-id="fb6cd-108">Beispiel 1: Abrufen aller reservierten IP-Adressen</span><span class="sxs-lookup"><span data-stu-id="fb6cd-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="fb6cd-109">Dieser Befehl ruft alle reservierten IP-Adressen ab.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="fb6cd-110">Beispiel 2: Abrufen einer reservierten IP-Adresse mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="fb6cd-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="fb6cd-111">Dieser Befehl ruft die reservierte IP-Adresse mit dem durch die $IpName-Variable angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="fb6cd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb6cd-112">PARAMETERS</span></span>

### <span data-ttu-id="fb6cd-113">-Information</span><span class="sxs-lookup"><span data-stu-id="fb6cd-113">-InformationAction</span></span>
<span data-ttu-id="fb6cd-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fb6cd-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fb6cd-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb6cd-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="fb6cd-116">Continue</span></span>
- <span data-ttu-id="fb6cd-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="fb6cd-117">Ignore</span></span>
- <span data-ttu-id="fb6cd-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="fb6cd-118">Inquire</span></span>
- <span data-ttu-id="fb6cd-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fb6cd-119">SilentlyContinue</span></span>
- <span data-ttu-id="fb6cd-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="fb6cd-120">Stop</span></span>
- <span data-ttu-id="fb6cd-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="fb6cd-121">Suspend</span></span>

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

### <span data-ttu-id="fb6cd-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fb6cd-122">-InformationVariable</span></span>
<span data-ttu-id="fb6cd-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fb6cd-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="fb6cd-124">-Profile</span></span>
<span data-ttu-id="fb6cd-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb6cd-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb6cd-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="fb6cd-127">-ReservedIPName</span></span>
<span data-ttu-id="fb6cd-128">Gibt den reservierten IP-Namen an.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-128">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6cd-129">CommonParameters</span></span>
<span data-ttu-id="fb6cd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6cd-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6cd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6cd-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb6cd-132">INPUTS</span></span>

## <span data-ttu-id="fb6cd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb6cd-133">OUTPUTS</span></span>

## <span data-ttu-id="fb6cd-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb6cd-134">NOTES</span></span>

## <span data-ttu-id="fb6cd-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb6cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="fb6cd-136">Neu – AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="fb6cd-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="fb6cd-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="fb6cd-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


