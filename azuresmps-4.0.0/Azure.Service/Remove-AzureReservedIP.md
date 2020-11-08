---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006351"
---
# <span data-ttu-id="448d4-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="448d4-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="448d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="448d4-102">SYNOPSIS</span></span>
<span data-ttu-id="448d4-103">Entfernt eine reservierte IP-Adresse mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="448d4-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="448d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="448d4-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="448d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="448d4-105">DESCRIPTION</span></span>
<span data-ttu-id="448d4-106">Das Cmdlet **Remove-AzureReservedIP** entfernt eine reservierte IP-Adresse mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="448d4-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="448d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="448d4-107">EXAMPLES</span></span>

### <span data-ttu-id="448d4-108">Beispiel 1: Entfernen einer reservierten IP-Adresse mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="448d4-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="448d4-109">Mit diesem Befehl wird eine reservierte IP-Adresse mit dem Namen entfernt.</span><span class="sxs-lookup"><span data-stu-id="448d4-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="448d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="448d4-110">PARAMETERS</span></span>

### <span data-ttu-id="448d4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="448d4-111">-Force</span></span>
<span data-ttu-id="448d4-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="448d4-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448d4-113">-Information</span><span class="sxs-lookup"><span data-stu-id="448d4-113">-InformationAction</span></span>
<span data-ttu-id="448d4-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="448d4-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="448d4-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="448d4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="448d4-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="448d4-116">Continue</span></span>
- <span data-ttu-id="448d4-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="448d4-117">Ignore</span></span>
- <span data-ttu-id="448d4-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="448d4-118">Inquire</span></span>
- <span data-ttu-id="448d4-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="448d4-119">SilentlyContinue</span></span>
- <span data-ttu-id="448d4-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="448d4-120">Stop</span></span>
- <span data-ttu-id="448d4-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="448d4-121">Suspend</span></span>

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

### <span data-ttu-id="448d4-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="448d4-122">-InformationVariable</span></span>
<span data-ttu-id="448d4-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="448d4-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="448d4-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="448d4-124">-Profile</span></span>
<span data-ttu-id="448d4-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="448d4-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="448d4-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="448d4-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="448d4-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="448d4-127">-ReservedIPName</span></span>
<span data-ttu-id="448d4-128">Gibt den Namen der reservierten IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="448d4-128">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448d4-129">CommonParameters</span></span>
<span data-ttu-id="448d4-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="448d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448d4-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448d4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448d4-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="448d4-132">INPUTS</span></span>

## <span data-ttu-id="448d4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="448d4-133">OUTPUTS</span></span>

## <span data-ttu-id="448d4-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="448d4-134">NOTES</span></span>

## <span data-ttu-id="448d4-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="448d4-135">RELATED LINKS</span></span>

[<span data-ttu-id="448d4-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="448d4-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="448d4-137">Neu – AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="448d4-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="448d4-138">Satz-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="448d4-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


