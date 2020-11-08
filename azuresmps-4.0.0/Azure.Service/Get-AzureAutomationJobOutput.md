---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005864"
---
# <span data-ttu-id="4d9fc-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="4d9fc-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="4d9fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d9fc-102">SYNOPSIS</span></span>

<span data-ttu-id="4d9fc-103">Ruft die Ausgabe eines Azure-Automatisierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="4d9fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d9fc-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4d9fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d9fc-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4d9fc-106">Das Cmdlet " **Get-AzureAutomationJobOutput** " Ruft die Ausgabe eines Microsoft Azure-Automatisierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="4d9fc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d9fc-107">EXAMPLES</span></span>

### <span data-ttu-id="4d9fc-108">Beispiel 1: Abrufen der Ausgabe eines Azure Automation-Auftrags</span><span class="sxs-lookup"><span data-stu-id="4d9fc-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="4d9fc-109">Dieser Befehl ruft alle Ausgaben des Auftrags ab, die die angegebene ID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="4d9fc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d9fc-110">PARAMETERS</span></span>

### <span data-ttu-id="4d9fc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4d9fc-111">-AutomationAccountName</span></span>
<span data-ttu-id="4d9fc-112">Gibt den Namen eines Azure Automation-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-112">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-113">-ID</span><span class="sxs-lookup"><span data-stu-id="4d9fc-113">-Id</span></span>
<span data-ttu-id="4d9fc-114">Gibt die ID eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="4d9fc-115">-Profile</span></span>
<span data-ttu-id="4d9fc-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4d9fc-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4d9fc-118">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="4d9fc-118">-StartTime</span></span>
<span data-ttu-id="4d9fc-119">Gibt eine Startzeit an.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="4d9fc-120">-Stream</span></span>
<span data-ttu-id="4d9fc-121">Gibt den Typ der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-121">Specifies the type of output.</span></span>
<span data-ttu-id="4d9fc-122">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4d9fc-122">Valid values are:</span></span> 

- <span data-ttu-id="4d9fc-123">Alle</span><span class="sxs-lookup"><span data-stu-id="4d9fc-123">Any</span></span>
- <span data-ttu-id="4d9fc-124">Debuggen</span><span class="sxs-lookup"><span data-stu-id="4d9fc-124">Debug</span></span>
- <span data-ttu-id="4d9fc-125">Fehler</span><span class="sxs-lookup"><span data-stu-id="4d9fc-125">Error</span></span>
- <span data-ttu-id="4d9fc-126">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="4d9fc-126">Output</span></span>
- <span data-ttu-id="4d9fc-127">Status</span><span class="sxs-lookup"><span data-stu-id="4d9fc-127">Progress</span></span>
- <span data-ttu-id="4d9fc-128">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="4d9fc-128">Verbose</span></span>
- <span data-ttu-id="4d9fc-129">Warnung</span><span class="sxs-lookup"><span data-stu-id="4d9fc-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d9fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9fc-130">CommonParameters</span></span>
<span data-ttu-id="4d9fc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d9fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9fc-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d9fc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9fc-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d9fc-133">INPUTS</span></span>

## <span data-ttu-id="4d9fc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d9fc-134">OUTPUTS</span></span>

## <span data-ttu-id="4d9fc-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d9fc-135">NOTES</span></span>

## <span data-ttu-id="4d9fc-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d9fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d9fc-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4d9fc-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="4d9fc-138">Lebenslauf-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4d9fc-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="4d9fc-139">Stopp-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4d9fc-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="4d9fc-140">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="4d9fc-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


