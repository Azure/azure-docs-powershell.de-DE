---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373846"
---
# <span data-ttu-id="7d1e2-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="7d1e2-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="7d1e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1e2-103">Ruft die Ausgabe eines Automatisierungsauftrags ab.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="7d1e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d1e2-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d1e2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d1e2-105">DESCRIPTION</span></span>
<span data-ttu-id="7d1e2-106">Das **Cmdlet "Get-AzAutomationJobOutput"** ruft die Ausgabe eines Azure-Automatisierungsauftrags ab.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="7d1e2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d1e2-107">EXAMPLES</span></span>

### <span data-ttu-id="7d1e2-108">Beispiel 1: Erhalten der Ausgabe eines Automatisierungsauftrags</span><span class="sxs-lookup"><span data-stu-id="7d1e2-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="7d1e2-109">Dieser Befehl ruft die Ausgabe des Auftrags ab, der die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="7d1e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d1e2-110">PARAMETERS</span></span>

### <span data-ttu-id="7d1e2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7d1e2-111">-AutomationAccountName</span></span>
<span data-ttu-id="7d1e2-112">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet die Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="7d1e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1e2-113">-DefaultProfile</span></span>
<span data-ttu-id="7d1e2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7d1e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d1e2-115">-ID</span><span class="sxs-lookup"><span data-stu-id="7d1e2-115">-Id</span></span>
<span data-ttu-id="7d1e2-116">Gibt die ID eines Auftrags an, für den dieses Cmdlet die Ausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="7d1e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d1e2-118">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet die Auftragsausgabe erhält.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="7d1e2-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7d1e2-119">-StartTime</span></span>
<span data-ttu-id="7d1e2-120">Gibt eine Startzeit als **"DateTimeOffset"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="7d1e2-121">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset konvertiert werden kann.**</span><span class="sxs-lookup"><span data-stu-id="7d1e2-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="7d1e2-122">Das Cmdlet ruft die nach diesem Zeitpunkt erstellte Ausgabe ab.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="7d1e2-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="7d1e2-123">-Stream</span></span>
<span data-ttu-id="7d1e2-124">Gibt den Ausgabetyp an.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-124">Specifies the type of output.</span></span>
<span data-ttu-id="7d1e2-125">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7d1e2-125">Valid values are:</span></span> 
- <span data-ttu-id="7d1e2-126">Any</span><span class="sxs-lookup"><span data-stu-id="7d1e2-126">Any</span></span>
- <span data-ttu-id="7d1e2-127">Debuggen</span><span class="sxs-lookup"><span data-stu-id="7d1e2-127">Debug</span></span>
- <span data-ttu-id="7d1e2-128">Fehler</span><span class="sxs-lookup"><span data-stu-id="7d1e2-128">Error</span></span>
- <span data-ttu-id="7d1e2-129">Ausgabe</span><span class="sxs-lookup"><span data-stu-id="7d1e2-129">Output</span></span>
- <span data-ttu-id="7d1e2-130">Status</span><span class="sxs-lookup"><span data-stu-id="7d1e2-130">Progress</span></span>
- <span data-ttu-id="7d1e2-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="7d1e2-131">Verbose</span></span>
- <span data-ttu-id="7d1e2-132">Warnung</span><span class="sxs-lookup"><span data-stu-id="7d1e2-132">Warning</span></span>

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

### <span data-ttu-id="7d1e2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1e2-133">CommonParameters</span></span>
<span data-ttu-id="7d1e2-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1e2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1e2-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1e2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1e2-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d1e2-136">INPUTS</span></span>

### <span data-ttu-id="7d1e2-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7d1e2-137">System.Guid</span></span>

### <span data-ttu-id="7d1e2-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="7d1e2-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="7d1e2-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d1e2-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7d1e2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7d1e2-140">System.String</span></span>

## <span data-ttu-id="7d1e2-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d1e2-141">OUTPUTS</span></span>

### <span data-ttu-id="7d1e2-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="7d1e2-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="7d1e2-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d1e2-143">NOTES</span></span>

## <span data-ttu-id="7d1e2-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d1e2-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d1e2-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7d1e2-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="7d1e2-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7d1e2-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="7d1e2-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7d1e2-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="7d1e2-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="7d1e2-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


