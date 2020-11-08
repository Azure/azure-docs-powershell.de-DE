---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006433"
---
# <span data-ttu-id="ccbcc-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ccbcc-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="ccbcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccbcc-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbcc-103">Erstellt eine affinitätsgruppe im aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="ccbcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccbcc-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccbcc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccbcc-105">DESCRIPTION</span></span>
<span data-ttu-id="ccbcc-106">Das Cmdlet **New-AzureAffinityGroup** erstellt eine Azure-affinitätsgruppe im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="ccbcc-107">Eine affinitätsgruppe fügt ihre Dienste und ihre Ressourcen in einem Azure Datacenter zusammen.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="ccbcc-108">Die affinitätsgruppe gruppiert Mitglieder zusammen, um eine optimale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="ccbcc-109">Definieren von Affinitätsgruppen auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="ccbcc-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="ccbcc-110">Ihre Affinitätsgruppen sind für alle nachfolgenden Cloud-Dienste oder Speicherkonten verfügbar, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="ccbcc-111">Sie können einer affinitätsgruppe nur dann Dienste hinzufügen, wenn Sie Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="ccbcc-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccbcc-112">EXAMPLES</span></span>

### <span data-ttu-id="ccbcc-113">Beispiel 1: Erstellen einer affinitätsgruppe</span><span class="sxs-lookup"><span data-stu-id="ccbcc-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="ccbcc-114">Mit diesem Befehl wird eine affinitätsgruppe namens South01 in der Region Süd-Zentralamerika erstellt.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="ccbcc-115">Der Befehl gibt eine Bezeichnung und eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="ccbcc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccbcc-116">PARAMETERS</span></span>

### <span data-ttu-id="ccbcc-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccbcc-117">-Description</span></span>
<span data-ttu-id="ccbcc-118">Gibt eine Beschreibung für die affinitätsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="ccbcc-119">Die Beschreibung kann bis zu 1024 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-119">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="ccbcc-120">-Information</span><span class="sxs-lookup"><span data-stu-id="ccbcc-120">-InformationAction</span></span>
<span data-ttu-id="ccbcc-121">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ccbcc-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ccbcc-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccbcc-123">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ccbcc-123">Continue</span></span>
- <span data-ttu-id="ccbcc-124">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ccbcc-124">Ignore</span></span>
- <span data-ttu-id="ccbcc-125">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ccbcc-125">Inquire</span></span>
- <span data-ttu-id="ccbcc-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ccbcc-126">SilentlyContinue</span></span>
- <span data-ttu-id="ccbcc-127">Beenden</span><span class="sxs-lookup"><span data-stu-id="ccbcc-127">Stop</span></span>
- <span data-ttu-id="ccbcc-128">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ccbcc-128">Suspend</span></span>

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

### <span data-ttu-id="ccbcc-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ccbcc-129">-InformationVariable</span></span>
<span data-ttu-id="ccbcc-130">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ccbcc-131">-Label</span><span class="sxs-lookup"><span data-stu-id="ccbcc-131">-Label</span></span>
<span data-ttu-id="ccbcc-132">Gibt eine Bezeichnung für die affinitätsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="ccbcc-133">Die Beschriftung kann bis zu 100 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-133">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="ccbcc-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="ccbcc-134">-Location</span></span>
<span data-ttu-id="ccbcc-135">Gibt den geografischen Standort des Azure Datacenter an, in dem dieses Cmdlet die affinitätsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

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

### <span data-ttu-id="ccbcc-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ccbcc-136">-Name</span></span>
<span data-ttu-id="ccbcc-137">Gibt einen Namen für die affinitätsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="ccbcc-138">Der Name muss für das Abonnement eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="ccbcc-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="ccbcc-139">-Profile</span></span>
<span data-ttu-id="ccbcc-140">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ccbcc-141">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ccbcc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbcc-142">CommonParameters</span></span>
<span data-ttu-id="ccbcc-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbcc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbcc-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbcc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbcc-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccbcc-145">INPUTS</span></span>

## <span data-ttu-id="ccbcc-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccbcc-146">OUTPUTS</span></span>

## <span data-ttu-id="ccbcc-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccbcc-147">NOTES</span></span>

## <span data-ttu-id="ccbcc-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccbcc-148">RELATED LINKS</span></span>

[<span data-ttu-id="ccbcc-149">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ccbcc-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="ccbcc-150">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ccbcc-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="ccbcc-151">Satz-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ccbcc-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


