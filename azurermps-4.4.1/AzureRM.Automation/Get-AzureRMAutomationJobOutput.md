---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665275"
---
# <span data-ttu-id="782ef-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="782ef-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="782ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="782ef-102">SYNOPSIS</span></span>
<span data-ttu-id="782ef-103">Ruft die Ausgabe eines Automatisierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="782ef-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="782ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="782ef-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="782ef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="782ef-105">DESCRIPTION</span></span>
<span data-ttu-id="782ef-106">Das Cmdlet " **Get-AzureRmAutomationJobOutput** " Ruft die Ausgabe eines Azure-Automatisierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="782ef-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="782ef-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="782ef-107">EXAMPLES</span></span>

### <span data-ttu-id="782ef-108">Beispiel 1: Abrufen der Ausgabe eines Automatisierungs Auftrags</span><span class="sxs-lookup"><span data-stu-id="782ef-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="782ef-109">Dieser Befehl ruft alle Ausgaben des Auftrags ab, die die angegebene ID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="782ef-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="782ef-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="782ef-110">PARAMETERS</span></span>

### <span data-ttu-id="782ef-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="782ef-111">-AutomationAccountName</span></span>
<span data-ttu-id="782ef-112">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="782ef-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782ef-113">-ID</span><span class="sxs-lookup"><span data-stu-id="782ef-113">-Id</span></span>
<span data-ttu-id="782ef-114">Gibt die ID eines Auftrags an, für den dieses Cmdlet eine Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="782ef-114">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782ef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782ef-115">-ResourceGroupName</span></span>
<span data-ttu-id="782ef-116">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="782ef-116">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782ef-117">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="782ef-117">-StartTime</span></span>
<span data-ttu-id="782ef-118">Gibt eine Startzeit als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="782ef-118">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="782ef-119">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="782ef-119">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="782ef-120">Das Cmdlet ruft die Ausgabe ab, die nach diesem Zeitpunkt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="782ef-120">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782ef-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="782ef-121">-Stream</span></span>
<span data-ttu-id="782ef-122">Gibt den Typ der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="782ef-122">Specifies the type of output.</span></span>
<span data-ttu-id="782ef-123">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="782ef-123">Valid values are:</span></span> 

- <span data-ttu-id="782ef-124">Alle</span><span class="sxs-lookup"><span data-stu-id="782ef-124">Any</span></span>
- <span data-ttu-id="782ef-125">Debuggen</span><span class="sxs-lookup"><span data-stu-id="782ef-125">Debug</span></span>
- <span data-ttu-id="782ef-126">Fehler</span><span class="sxs-lookup"><span data-stu-id="782ef-126">Error</span></span>
- <span data-ttu-id="782ef-127">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="782ef-127">Output</span></span>
- <span data-ttu-id="782ef-128">Status</span><span class="sxs-lookup"><span data-stu-id="782ef-128">Progress</span></span>
- <span data-ttu-id="782ef-129">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="782ef-129">Verbose</span></span>
- <span data-ttu-id="782ef-130">Warnung</span><span class="sxs-lookup"><span data-stu-id="782ef-130">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782ef-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782ef-131">-DefaultProfile</span></span>
<span data-ttu-id="782ef-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="782ef-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="782ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782ef-133">CommonParameters</span></span>
<span data-ttu-id="782ef-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782ef-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="782ef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782ef-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="782ef-136">INPUTS</span></span>

## <span data-ttu-id="782ef-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="782ef-137">OUTPUTS</span></span>

### <span data-ttu-id="782ef-138">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="782ef-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="782ef-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="782ef-139">NOTES</span></span>

## <span data-ttu-id="782ef-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="782ef-140">RELATED LINKS</span></span>

[<span data-ttu-id="782ef-141">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="782ef-141">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="782ef-142">Lebenslauf-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="782ef-142">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="782ef-143">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="782ef-143">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="782ef-144">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="782ef-144">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


