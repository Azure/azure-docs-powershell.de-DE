---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006763"
---
# <span data-ttu-id="fc4f0-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="fc4f0-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="fc4f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4f0-103">Ruft die statischen VNet-IP-Adressinformationen aus einem virtuellen Computerobjekt ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="fc4f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc4f0-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fc4f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc4f0-105">DESCRIPTION</span></span>
<span data-ttu-id="fc4f0-106">Das Cmdlet " **Get-AzureStaticVNetIP** " Ruft die IP-Adressinformationen (static Virtual Network, VNet) von einem virtuellen Computerobjekt ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="fc4f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc4f0-107">EXAMPLES</span></span>

### <span data-ttu-id="fc4f0-108">1:</span><span class="sxs-lookup"><span data-stu-id="fc4f0-108">1:</span></span>
```

```

## <span data-ttu-id="fc4f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc4f0-109">PARAMETERS</span></span>

### <span data-ttu-id="fc4f0-110">-Information</span><span class="sxs-lookup"><span data-stu-id="fc4f0-110">-InformationAction</span></span>
<span data-ttu-id="fc4f0-111">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fc4f0-112">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fc4f0-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc4f0-113">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="fc4f0-113">Continue</span></span>
- <span data-ttu-id="fc4f0-114">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="fc4f0-114">Ignore</span></span>
- <span data-ttu-id="fc4f0-115">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="fc4f0-115">Inquire</span></span>
- <span data-ttu-id="fc4f0-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fc4f0-116">SilentlyContinue</span></span>
- <span data-ttu-id="fc4f0-117">Beenden</span><span class="sxs-lookup"><span data-stu-id="fc4f0-117">Stop</span></span>
- <span data-ttu-id="fc4f0-118">Anhalten</span><span class="sxs-lookup"><span data-stu-id="fc4f0-118">Suspend</span></span>

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

### <span data-ttu-id="fc4f0-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fc4f0-119">-InformationVariable</span></span>
<span data-ttu-id="fc4f0-120">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fc4f0-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="fc4f0-121">-Profile</span></span>
<span data-ttu-id="fc4f0-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc4f0-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc4f0-124">-VM</span><span class="sxs-lookup"><span data-stu-id="fc4f0-124">-VM</span></span>
<span data-ttu-id="fc4f0-125">Gibt ein persistentes Virtual Machine-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fc4f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4f0-126">CommonParameters</span></span>
<span data-ttu-id="fc4f0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4f0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc4f0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4f0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc4f0-129">INPUTS</span></span>

## <span data-ttu-id="fc4f0-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc4f0-130">OUTPUTS</span></span>

## <span data-ttu-id="fc4f0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc4f0-131">NOTES</span></span>

## <span data-ttu-id="fc4f0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc4f0-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc4f0-133">Satz-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="fc4f0-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


