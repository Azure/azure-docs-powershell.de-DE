---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006374"
---
# <span data-ttu-id="29f01-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="29f01-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="29f01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29f01-102">SYNOPSIS</span></span>
<span data-ttu-id="29f01-103">Entfernt einen Verfügbarkeits Satz von einem Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="29f01-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="29f01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29f01-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="29f01-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29f01-105">DESCRIPTION</span></span>
<span data-ttu-id="29f01-106">Das Cmdlet **Remove-AzureAvailabilitySet** entfernt einen Verfügbarkeits Satz von einem Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="29f01-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="29f01-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29f01-107">EXAMPLES</span></span>

### <span data-ttu-id="29f01-108">1:</span><span class="sxs-lookup"><span data-stu-id="29f01-108">1:</span></span>
```

```

## <span data-ttu-id="29f01-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29f01-109">PARAMETERS</span></span>

### <span data-ttu-id="29f01-110">-Information</span><span class="sxs-lookup"><span data-stu-id="29f01-110">-InformationAction</span></span>
<span data-ttu-id="29f01-111">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="29f01-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="29f01-112">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29f01-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29f01-113">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="29f01-113">Continue</span></span>
- <span data-ttu-id="29f01-114">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="29f01-114">Ignore</span></span>
- <span data-ttu-id="29f01-115">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="29f01-115">Inquire</span></span>
- <span data-ttu-id="29f01-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="29f01-116">SilentlyContinue</span></span>
- <span data-ttu-id="29f01-117">Beenden</span><span class="sxs-lookup"><span data-stu-id="29f01-117">Stop</span></span>
- <span data-ttu-id="29f01-118">Anhalten</span><span class="sxs-lookup"><span data-stu-id="29f01-118">Suspend</span></span>

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

### <span data-ttu-id="29f01-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="29f01-119">-InformationVariable</span></span>
<span data-ttu-id="29f01-120">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="29f01-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="29f01-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="29f01-121">-Profile</span></span>
<span data-ttu-id="29f01-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="29f01-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="29f01-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="29f01-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="29f01-124">-VM</span><span class="sxs-lookup"><span data-stu-id="29f01-124">-VM</span></span>
<span data-ttu-id="29f01-125">Gibt den virtuellen Computer an, auf dem dieses Cmdlet einen Verfügbarkeits Satz entfernt.</span><span class="sxs-lookup"><span data-stu-id="29f01-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29f01-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f01-126">CommonParameters</span></span>
<span data-ttu-id="29f01-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f01-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f01-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f01-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f01-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29f01-129">INPUTS</span></span>

## <span data-ttu-id="29f01-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29f01-130">OUTPUTS</span></span>

## <span data-ttu-id="29f01-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="29f01-131">NOTES</span></span>

## <span data-ttu-id="29f01-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29f01-132">RELATED LINKS</span></span>

[<span data-ttu-id="29f01-133">Satz-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="29f01-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


