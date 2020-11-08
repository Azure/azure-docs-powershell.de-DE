---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006310"
---
# <span data-ttu-id="15190-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="15190-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="15190-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15190-102">SYNOPSIS</span></span>
<span data-ttu-id="15190-103">Entfernt die statischen virtuellen Netzwerk-IP-Adressinformationen aus einem virtuellen Computerobjekt (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="15190-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="15190-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15190-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="15190-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15190-105">DESCRIPTION</span></span>
<span data-ttu-id="15190-106">Das Cmdlet **Remove-AzureStaticVNetIP** entfernt die IP-Adressinformationen (static Virtual Network, VNet) aus einem virtuellen Computerobjekt (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="15190-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="15190-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15190-107">EXAMPLES</span></span>

### <span data-ttu-id="15190-108">1:</span><span class="sxs-lookup"><span data-stu-id="15190-108">1:</span></span>
```

```

## <span data-ttu-id="15190-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="15190-109">PARAMETERS</span></span>

### <span data-ttu-id="15190-110">-Information</span><span class="sxs-lookup"><span data-stu-id="15190-110">-InformationAction</span></span>
<span data-ttu-id="15190-111">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="15190-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="15190-112">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="15190-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15190-113">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="15190-113">Continue</span></span>
- <span data-ttu-id="15190-114">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="15190-114">Ignore</span></span>
- <span data-ttu-id="15190-115">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="15190-115">Inquire</span></span>
- <span data-ttu-id="15190-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="15190-116">SilentlyContinue</span></span>
- <span data-ttu-id="15190-117">Beenden</span><span class="sxs-lookup"><span data-stu-id="15190-117">Stop</span></span>
- <span data-ttu-id="15190-118">Anhalten</span><span class="sxs-lookup"><span data-stu-id="15190-118">Suspend</span></span>

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

### <span data-ttu-id="15190-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="15190-119">-InformationVariable</span></span>
<span data-ttu-id="15190-120">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="15190-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="15190-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="15190-121">-Profile</span></span>
<span data-ttu-id="15190-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="15190-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="15190-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="15190-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="15190-124">-VM</span><span class="sxs-lookup"><span data-stu-id="15190-124">-VM</span></span>
<span data-ttu-id="15190-125">Gibt ein persistentes Virtual Machine-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="15190-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="15190-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15190-126">CommonParameters</span></span>
<span data-ttu-id="15190-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15190-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15190-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15190-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15190-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15190-129">INPUTS</span></span>

## <span data-ttu-id="15190-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15190-130">OUTPUTS</span></span>

## <span data-ttu-id="15190-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="15190-131">NOTES</span></span>

## <span data-ttu-id="15190-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15190-132">RELATED LINKS</span></span>

[<span data-ttu-id="15190-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="15190-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="15190-134">Satz-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="15190-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


