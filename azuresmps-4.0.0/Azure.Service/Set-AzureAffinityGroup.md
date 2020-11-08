---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006637"
---
# <span data-ttu-id="0779f-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="0779f-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="0779f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0779f-102">SYNOPSIS</span></span>
<span data-ttu-id="0779f-103">Ändert die Eigenschaften einer affinitätsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0779f-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="0779f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0779f-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0779f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0779f-105">DESCRIPTION</span></span>
<span data-ttu-id="0779f-106">Das Cmdlet " **Satz-AzureAffinityGroup** " ändert die Eigenschaften einer Azure-affinitätsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0779f-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="0779f-107">Sie können die Beschriftung und die Beschreibung ändern.</span><span class="sxs-lookup"><span data-stu-id="0779f-107">You can change the label and the description.</span></span>

## <span data-ttu-id="0779f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0779f-108">EXAMPLES</span></span>

### <span data-ttu-id="0779f-109">Beispiel 1: Ändern einer affinitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="0779f-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="0779f-110">Mit diesem Befehl wird die Bezeichnung der affinitätsgruppe mit dem Namen South01 so geändert, dass der Befehl auch die Beschreibung ändert.</span><span class="sxs-lookup"><span data-stu-id="0779f-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="0779f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0779f-111">PARAMETERS</span></span>

### <span data-ttu-id="0779f-112">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0779f-112">-Description</span></span>
<span data-ttu-id="0779f-113">Gibt die Beschreibung der affinitätsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="0779f-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="0779f-114">Die Beschreibung kann bis zu 1024 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="0779f-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0779f-115">-Information</span><span class="sxs-lookup"><span data-stu-id="0779f-115">-InformationAction</span></span>
<span data-ttu-id="0779f-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="0779f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0779f-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0779f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0779f-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="0779f-118">Continue</span></span>
- <span data-ttu-id="0779f-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0779f-119">Ignore</span></span>
- <span data-ttu-id="0779f-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="0779f-120">Inquire</span></span>
- <span data-ttu-id="0779f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0779f-121">SilentlyContinue</span></span>
- <span data-ttu-id="0779f-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="0779f-122">Stop</span></span>
- <span data-ttu-id="0779f-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="0779f-123">Suspend</span></span>

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

### <span data-ttu-id="0779f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0779f-124">-InformationVariable</span></span>
<span data-ttu-id="0779f-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="0779f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0779f-126">-Label</span><span class="sxs-lookup"><span data-stu-id="0779f-126">-Label</span></span>
<span data-ttu-id="0779f-127">Gibt eine Bezeichnung für die affinitätsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="0779f-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="0779f-128">Die Beschriftung kann bis zu 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="0779f-128">The label can be up to 100 characters long.</span></span>

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

### <span data-ttu-id="0779f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0779f-129">-Name</span></span>
<span data-ttu-id="0779f-130">Gibt den Namen der affinitätsgruppe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0779f-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0779f-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="0779f-131">-Profile</span></span>
<span data-ttu-id="0779f-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0779f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0779f-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0779f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0779f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0779f-134">CommonParameters</span></span>
<span data-ttu-id="0779f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0779f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0779f-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0779f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0779f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0779f-137">INPUTS</span></span>

## <span data-ttu-id="0779f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0779f-138">OUTPUTS</span></span>

## <span data-ttu-id="0779f-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0779f-139">NOTES</span></span>

## <span data-ttu-id="0779f-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0779f-140">RELATED LINKS</span></span>

[<span data-ttu-id="0779f-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="0779f-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="0779f-142">Neu – AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="0779f-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="0779f-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="0779f-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


