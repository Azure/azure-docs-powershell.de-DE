---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005877"
---
# <span data-ttu-id="5aedc-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5aedc-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="5aedc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5aedc-102">SYNOPSIS</span></span>
<span data-ttu-id="5aedc-103">Ruft ein Azure Affinity Group-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="5aedc-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="5aedc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aedc-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5aedc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5aedc-105">DESCRIPTION</span></span>
<span data-ttu-id="5aedc-106">Das Cmdlet " **Get-AzureAffinityGroup** " Ruft eine Azure-affinitätsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5aedc-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="5aedc-107">Das Affinitätsgruppen Objekt enthält den Namen der affinitätsgruppe, den Speicherort, die Bezeichnung, die Beschreibung und den Speicher und die gehosteten Dienste, die Teil der affinitätsgruppe sind.</span><span class="sxs-lookup"><span data-stu-id="5aedc-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="5aedc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5aedc-108">EXAMPLES</span></span>

### <span data-ttu-id="5aedc-109">Beispiel 1: Abrufen von Eigenschaften einer affinitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="5aedc-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="5aedc-110">Dieser Befehl ruft die Eigenschaften der affinitätsgruppe mit dem Namen South01 ab.</span><span class="sxs-lookup"><span data-stu-id="5aedc-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="5aedc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aedc-111">PARAMETERS</span></span>

### <span data-ttu-id="5aedc-112">-Information</span><span class="sxs-lookup"><span data-stu-id="5aedc-112">-InformationAction</span></span>
<span data-ttu-id="5aedc-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="5aedc-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5aedc-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5aedc-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5aedc-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="5aedc-115">Continue</span></span>
- <span data-ttu-id="5aedc-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="5aedc-116">Ignore</span></span>
- <span data-ttu-id="5aedc-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="5aedc-117">Inquire</span></span>
- <span data-ttu-id="5aedc-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5aedc-118">SilentlyContinue</span></span>
- <span data-ttu-id="5aedc-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="5aedc-119">Stop</span></span>
- <span data-ttu-id="5aedc-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="5aedc-120">Suspend</span></span>

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

### <span data-ttu-id="5aedc-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5aedc-121">-InformationVariable</span></span>
<span data-ttu-id="5aedc-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="5aedc-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5aedc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5aedc-123">-Name</span></span>
<span data-ttu-id="5aedc-124">Gibt den Namen der affinitätsgruppe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5aedc-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="5aedc-125">Namen für Affinity Groups, die über das Verwaltungs Portal erstellt wurden, sind in der Regel GUIDs.</span><span class="sxs-lookup"><span data-stu-id="5aedc-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="5aedc-126">Der Verwaltungs Anschluss zeigt die Beschriftung der affinitätsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="5aedc-126">The Management Port shows the affinity group label.</span></span>

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

### <span data-ttu-id="5aedc-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="5aedc-127">-Profile</span></span>
<span data-ttu-id="5aedc-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5aedc-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5aedc-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5aedc-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5aedc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aedc-130">CommonParameters</span></span>
<span data-ttu-id="5aedc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aedc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aedc-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aedc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aedc-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5aedc-133">INPUTS</span></span>

## <span data-ttu-id="5aedc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5aedc-134">OUTPUTS</span></span>

### <span data-ttu-id="5aedc-135">Affinitäts-Group</span><span class="sxs-lookup"><span data-stu-id="5aedc-135">AffinityGroup</span></span>

## <span data-ttu-id="5aedc-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5aedc-136">NOTES</span></span>

## <span data-ttu-id="5aedc-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5aedc-137">RELATED LINKS</span></span>

[<span data-ttu-id="5aedc-138">Neu – AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5aedc-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="5aedc-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5aedc-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="5aedc-140">Satz-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5aedc-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


