---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: f49c0bbf17ed87d782b03052d9caeb5aba51eeff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941995"
---
# <span data-ttu-id="a255b-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a255b-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="a255b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a255b-102">SYNOPSIS</span></span>
<span data-ttu-id="a255b-103">Ruft die Ausgabe eines Automatisierungsauftrags ab.</span><span class="sxs-lookup"><span data-stu-id="a255b-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="a255b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a255b-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a255b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a255b-105">DESCRIPTION</span></span>
<span data-ttu-id="a255b-106">Das **Get-AzAutomationJobOutput-Cmdlet** ruft die Ausgabe eines Azure-Automatisierungsauftrags ab.</span><span class="sxs-lookup"><span data-stu-id="a255b-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="a255b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a255b-107">EXAMPLES</span></span>

### <span data-ttu-id="a255b-108">Beispiel 1: Erhalten der Ausgabe eines Automatisierungsauftrags</span><span class="sxs-lookup"><span data-stu-id="a255b-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="a255b-109">Dieser Befehl ruft alle Ausgaben des Auftrags ab, der die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="a255b-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="a255b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a255b-110">PARAMETERS</span></span>

### <span data-ttu-id="a255b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a255b-111">-AutomationAccountName</span></span>
<span data-ttu-id="a255b-112">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="a255b-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="a255b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a255b-113">-DefaultProfile</span></span>
<span data-ttu-id="a255b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a255b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a255b-115">-ID</span><span class="sxs-lookup"><span data-stu-id="a255b-115">-Id</span></span>
<span data-ttu-id="a255b-116">Gibt die ID eines Auftrags an, für den dieses Cmdlet die Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="a255b-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="a255b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a255b-117">-ResourceGroupName</span></span>
<span data-ttu-id="a255b-118">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet die Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="a255b-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="a255b-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a255b-119">-StartTime</span></span>
<span data-ttu-id="a255b-120">Gibt eine Startzeit als **DateTimeOffset-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="a255b-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a255b-121">Sie können eine Zeichenfolge angeben, die in eine gültige **DateTimeOffset konvertiert werden kann.**</span><span class="sxs-lookup"><span data-stu-id="a255b-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="a255b-122">Das Cmdlet ruft die nach diesem Zeitpunkt erstellte Ausgabe ab.</span><span class="sxs-lookup"><span data-stu-id="a255b-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="a255b-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="a255b-123">-Stream</span></span>
<span data-ttu-id="a255b-124">Gibt den Ausgabetyp an.</span><span class="sxs-lookup"><span data-stu-id="a255b-124">Specifies the type of output.</span></span>
<span data-ttu-id="a255b-125">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a255b-125">Valid values are:</span></span> 
- <span data-ttu-id="a255b-126">Any</span><span class="sxs-lookup"><span data-stu-id="a255b-126">Any</span></span>
- <span data-ttu-id="a255b-127">Debuggen</span><span class="sxs-lookup"><span data-stu-id="a255b-127">Debug</span></span>
- <span data-ttu-id="a255b-128">Fehler</span><span class="sxs-lookup"><span data-stu-id="a255b-128">Error</span></span>
- <span data-ttu-id="a255b-129">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a255b-129">Output</span></span>
- <span data-ttu-id="a255b-130">Fortschritt</span><span class="sxs-lookup"><span data-stu-id="a255b-130">Progress</span></span>
- <span data-ttu-id="a255b-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="a255b-131">Verbose</span></span>
- <span data-ttu-id="a255b-132">Warnung</span><span class="sxs-lookup"><span data-stu-id="a255b-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a255b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a255b-133">CommonParameters</span></span>
<span data-ttu-id="a255b-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a255b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a255b-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a255b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a255b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a255b-136">INPUTS</span></span>

### <span data-ttu-id="a255b-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a255b-137">System.Guid</span></span>

### <span data-ttu-id="a255b-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="a255b-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="a255b-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a255b-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a255b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a255b-140">System.String</span></span>

## <span data-ttu-id="a255b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a255b-141">OUTPUTS</span></span>

### <span data-ttu-id="a255b-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="a255b-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="a255b-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a255b-143">NOTES</span></span>

## <span data-ttu-id="a255b-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a255b-144">RELATED LINKS</span></span>

[<span data-ttu-id="a255b-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a255b-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="a255b-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a255b-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="a255b-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a255b-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="a255b-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a255b-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


