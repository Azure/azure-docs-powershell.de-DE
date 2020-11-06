---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: e2b965800c4f8307edaedf25b032767ca1784049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502269"
---
# <span data-ttu-id="7fb99-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="7fb99-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="7fb99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fb99-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb99-103">Ruft die Ausgabe eines Automatisierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="7fb99-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fb99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fb99-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb99-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fb99-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb99-106">Das Cmdlet " **Get-AzureRmAutomationJobOutput** " Ruft die Ausgabe eines Azure-Automatisierungs Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="7fb99-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="7fb99-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fb99-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb99-108">Beispiel 1: Abrufen der Ausgabe eines Automatisierungs Auftrags</span><span class="sxs-lookup"><span data-stu-id="7fb99-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="7fb99-109">Dieser Befehl ruft alle Ausgaben des Auftrags ab, die die angegebene ID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7fb99-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="7fb99-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fb99-110">PARAMETERS</span></span>

### <span data-ttu-id="7fb99-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7fb99-111">-AutomationAccountName</span></span>
<span data-ttu-id="7fb99-112">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="7fb99-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="7fb99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb99-113">-DefaultProfile</span></span>
<span data-ttu-id="7fb99-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7fb99-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fb99-115">-ID</span><span class="sxs-lookup"><span data-stu-id="7fb99-115">-Id</span></span>
<span data-ttu-id="7fb99-116">Gibt die ID eines Auftrags an, für den dieses Cmdlet eine Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="7fb99-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="7fb99-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb99-117">-ResourceGroupName</span></span>
<span data-ttu-id="7fb99-118">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="7fb99-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="7fb99-119">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="7fb99-119">-StartTime</span></span>
<span data-ttu-id="7fb99-120">Gibt eine Startzeit als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7fb99-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="7fb99-121">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fb99-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="7fb99-122">Das Cmdlet ruft die Ausgabe ab, die nach diesem Zeitpunkt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7fb99-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="7fb99-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="7fb99-123">-Stream</span></span>
<span data-ttu-id="7fb99-124">Gibt den Typ der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="7fb99-124">Specifies the type of output.</span></span>
<span data-ttu-id="7fb99-125">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7fb99-125">Valid values are:</span></span> 
- <span data-ttu-id="7fb99-126">Alle</span><span class="sxs-lookup"><span data-stu-id="7fb99-126">Any</span></span>
- <span data-ttu-id="7fb99-127">Debuggen</span><span class="sxs-lookup"><span data-stu-id="7fb99-127">Debug</span></span>
- <span data-ttu-id="7fb99-128">Fehler</span><span class="sxs-lookup"><span data-stu-id="7fb99-128">Error</span></span>
- <span data-ttu-id="7fb99-129">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7fb99-129">Output</span></span>
- <span data-ttu-id="7fb99-130">Status</span><span class="sxs-lookup"><span data-stu-id="7fb99-130">Progress</span></span>
- <span data-ttu-id="7fb99-131">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="7fb99-131">Verbose</span></span>
- <span data-ttu-id="7fb99-132">Warnung</span><span class="sxs-lookup"><span data-stu-id="7fb99-132">Warning</span></span>

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

### <span data-ttu-id="7fb99-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb99-133">CommonParameters</span></span>
<span data-ttu-id="7fb99-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb99-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb99-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb99-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb99-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fb99-136">INPUTS</span></span>

### <span data-ttu-id="7fb99-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7fb99-137">System.Guid</span></span>

### <span data-ttu-id="7fb99-138">Microsoft. Azure. Commands. Automation. Common. Streamtype</span><span class="sxs-lookup"><span data-stu-id="7fb99-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="7fb99-139">System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7fb99-139">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7fb99-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb99-140">System.String</span></span>

## <span data-ttu-id="7fb99-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fb99-141">OUTPUTS</span></span>

### <span data-ttu-id="7fb99-142">Microsoft. Azure. Commands. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="7fb99-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="7fb99-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fb99-143">NOTES</span></span>

## <span data-ttu-id="7fb99-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fb99-144">RELATED LINKS</span></span>

[<span data-ttu-id="7fb99-145">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7fb99-145">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="7fb99-146">Lebenslauf-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7fb99-146">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="7fb99-147">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7fb99-147">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="7fb99-148">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7fb99-148">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


