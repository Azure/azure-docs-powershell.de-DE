---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 378bab1d62d5abcfb1eb2506e41d22bf26b217b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941992"
---
# <span data-ttu-id="43f16-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43f16-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="43f16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43f16-102">SYNOPSIS</span></span>
<span data-ttu-id="43f16-103">Ruft Automatisierungs-Runbookaufträge ab.</span><span class="sxs-lookup"><span data-stu-id="43f16-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="43f16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43f16-104">SYNTAX</span></span>

### <span data-ttu-id="43f16-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="43f16-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43f16-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="43f16-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43f16-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="43f16-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43f16-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43f16-108">DESCRIPTION</span></span>
<span data-ttu-id="43f16-109">Das **Get-AzAutomationJob-Cmdlet** ruft runbook-Aufträge in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="43f16-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="43f16-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43f16-110">EXAMPLES</span></span>

### <span data-ttu-id="43f16-111">Beispiel 1: Erhalten eines bestimmten Runbookauftrags</span><span class="sxs-lookup"><span data-stu-id="43f16-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="43f16-112">Dieser Befehl ruft den Auftrag ab, der über die angegebene GUID verfügt.</span><span class="sxs-lookup"><span data-stu-id="43f16-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="43f16-113">Beispiel 2: Alle Aufträge für ein Runbook erhalten</span><span class="sxs-lookup"><span data-stu-id="43f16-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="43f16-114">Dieser Befehl ruft alle Aufträge ab, die einem Runbook mit dem Namen Runbook02 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="43f16-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="43f16-115">Beispiel 3: Alle ausgeführten Aufträge erhalten</span><span class="sxs-lookup"><span data-stu-id="43f16-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="43f16-116">Dieser Befehl ruft alle ausgeführten Aufträge im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="43f16-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="43f16-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43f16-117">PARAMETERS</span></span>

### <span data-ttu-id="43f16-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43f16-118">-AutomationAccountName</span></span>
<span data-ttu-id="43f16-119">Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="43f16-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="43f16-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f16-120">-DefaultProfile</span></span>
<span data-ttu-id="43f16-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="43f16-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43f16-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="43f16-122">-EndTime</span></span>
<span data-ttu-id="43f16-123">Gibt die Endzeit für einen Auftrag als **DateTimeOffset-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="43f16-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="43f16-124">Sie können eine Zeichenfolge angeben, die in eine gültige **DateTimeOffset konvertiert werden kann.**</span><span class="sxs-lookup"><span data-stu-id="43f16-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="43f16-125">Dieses Cmdlet ruft Aufträge ab, die eine Endzeit zum oder vor dem von diesem Parameter angegebenen Wert haben.</span><span class="sxs-lookup"><span data-stu-id="43f16-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f16-126">-ID</span><span class="sxs-lookup"><span data-stu-id="43f16-126">-Id</span></span>
<span data-ttu-id="43f16-127">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="43f16-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f16-128">-ResourceGroupName</span></span>
<span data-ttu-id="43f16-129">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="43f16-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="43f16-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="43f16-130">-RunbookName</span></span>
<span data-ttu-id="43f16-131">Gibt den Namen eines Runbooks an, für das dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="43f16-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f16-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43f16-132">-StartTime</span></span>
<span data-ttu-id="43f16-133">Gibt die Startzeit eines Auftrags als **DateTimeOffset-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="43f16-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="43f16-134">Dieses Cmdlet ruft Aufträge ab, die eine Startzeit zum oder nach dem von diesem Parameter angegebenen Wert haben.</span><span class="sxs-lookup"><span data-stu-id="43f16-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f16-135">-Status</span><span class="sxs-lookup"><span data-stu-id="43f16-135">-Status</span></span>
<span data-ttu-id="43f16-136">Gibt den Status eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="43f16-136">Specifies the status of a job.</span></span>
<span data-ttu-id="43f16-137">Dieses Cmdlet ruft Aufträge ab, deren Status mit diesem Parameter übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="43f16-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="43f16-138">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="43f16-138">Valid values are:</span></span> 
- <span data-ttu-id="43f16-139">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="43f16-139">Activating</span></span>
- <span data-ttu-id="43f16-140">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="43f16-140">Completed</span></span>
- <span data-ttu-id="43f16-141">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="43f16-141">Failed</span></span>
- <span data-ttu-id="43f16-142">In warteschlangen</span><span class="sxs-lookup"><span data-stu-id="43f16-142">Queued</span></span>
- <span data-ttu-id="43f16-143">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="43f16-143">Resuming</span></span>
- <span data-ttu-id="43f16-144">Ausführen</span><span class="sxs-lookup"><span data-stu-id="43f16-144">Running</span></span>
- <span data-ttu-id="43f16-145">Starten</span><span class="sxs-lookup"><span data-stu-id="43f16-145">Starting</span></span>
- <span data-ttu-id="43f16-146">Beendet</span><span class="sxs-lookup"><span data-stu-id="43f16-146">Stopped</span></span>
- <span data-ttu-id="43f16-147">Beenden</span><span class="sxs-lookup"><span data-stu-id="43f16-147">Stopping</span></span>
- <span data-ttu-id="43f16-148">Angehalten</span><span class="sxs-lookup"><span data-stu-id="43f16-148">Suspended</span></span>
- <span data-ttu-id="43f16-149">Anhalten</span><span class="sxs-lookup"><span data-stu-id="43f16-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43f16-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f16-150">CommonParameters</span></span>
<span data-ttu-id="43f16-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f16-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f16-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f16-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f16-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43f16-153">INPUTS</span></span>

### <span data-ttu-id="43f16-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="43f16-154">System.Guid</span></span>

### <span data-ttu-id="43f16-155">System.String</span><span class="sxs-lookup"><span data-stu-id="43f16-155">System.String</span></span>

## <span data-ttu-id="43f16-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43f16-156">OUTPUTS</span></span>

### <span data-ttu-id="43f16-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="43f16-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="43f16-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43f16-158">NOTES</span></span>

## <span data-ttu-id="43f16-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43f16-159">RELATED LINKS</span></span>

[<span data-ttu-id="43f16-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="43f16-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="43f16-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43f16-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="43f16-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43f16-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="43f16-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="43f16-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


