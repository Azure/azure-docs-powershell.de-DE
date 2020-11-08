---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997381"
---
# <span data-ttu-id="8baab-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8baab-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="8baab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8baab-102">SYNOPSIS</span></span>
<span data-ttu-id="8baab-103">Ruft Automatisierungs runbooks Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="8baab-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="8baab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8baab-104">SYNTAX</span></span>

### <span data-ttu-id="8baab-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="8baab-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8baab-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="8baab-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8baab-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="8baab-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8baab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8baab-108">DESCRIPTION</span></span>
<span data-ttu-id="8baab-109">Das Cmdlet " **Get-AzAutomationJob** " ruft runbooks-Aufträge in Azure-Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="8baab-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="8baab-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8baab-110">EXAMPLES</span></span>

### <span data-ttu-id="8baab-111">Beispiel 1: Abrufen eines bestimmten runbooks-Auftrags</span><span class="sxs-lookup"><span data-stu-id="8baab-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="8baab-112">Dieser Befehl ruft den Auftrag ab, der die angegebene GUID aufweist.</span><span class="sxs-lookup"><span data-stu-id="8baab-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="8baab-113">Beispiel 2: Abrufen aller Aufträge für eine runbooks</span><span class="sxs-lookup"><span data-stu-id="8baab-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="8baab-114">Dieser Befehl ruft alle Aufträge ab, die einem runbooks mit dem Namen Runbook02 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8baab-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="8baab-115">Beispiel 3: Abrufen aller ausgeführten Aufträge</span><span class="sxs-lookup"><span data-stu-id="8baab-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="8baab-116">Dieser Befehl ruft alle ausgeführten Aufträge im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8baab-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8baab-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8baab-117">PARAMETERS</span></span>

### <span data-ttu-id="8baab-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8baab-118">-AutomationAccountName</span></span>
<span data-ttu-id="8baab-119">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="8baab-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="8baab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8baab-120">-DefaultProfile</span></span>
<span data-ttu-id="8baab-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8baab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8baab-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8baab-122">-EndTime</span></span>
<span data-ttu-id="8baab-123">Gibt die Endzeit für einen Auftrag als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8baab-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="8baab-124">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8baab-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="8baab-125">Dieses Cmdlet ruft Aufträge ab, die eine Endzeit am oder vor dem Wert aufweisen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8baab-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="8baab-126">-ID</span><span class="sxs-lookup"><span data-stu-id="8baab-126">-Id</span></span>
<span data-ttu-id="8baab-127">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="8baab-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8baab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8baab-128">-ResourceGroupName</span></span>
<span data-ttu-id="8baab-129">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="8baab-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="8baab-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="8baab-130">-RunbookName</span></span>
<span data-ttu-id="8baab-131">Gibt den Namen einer runbooks an, für die dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="8baab-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="8baab-132">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="8baab-132">-StartTime</span></span>
<span data-ttu-id="8baab-133">Gibt die Startzeit eines Auftrags als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8baab-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="8baab-134">Dieses Cmdlet ruft Aufträge ab, die eine Startzeit am oder hinter dem Wert haben, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8baab-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="8baab-135">-Status</span><span class="sxs-lookup"><span data-stu-id="8baab-135">-Status</span></span>
<span data-ttu-id="8baab-136">Gibt den Status eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="8baab-136">Specifies the status of a job.</span></span>
<span data-ttu-id="8baab-137">Dieses Cmdlet ruft Aufträge ab, deren Status diesem Parameter entspricht.</span><span class="sxs-lookup"><span data-stu-id="8baab-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="8baab-138">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8baab-138">Valid values are:</span></span> 
- <span data-ttu-id="8baab-139">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="8baab-139">Activating</span></span>
- <span data-ttu-id="8baab-140">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="8baab-140">Completed</span></span>
- <span data-ttu-id="8baab-141">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="8baab-141">Failed</span></span>
- <span data-ttu-id="8baab-142">Queued</span><span class="sxs-lookup"><span data-stu-id="8baab-142">Queued</span></span>
- <span data-ttu-id="8baab-143">Wieder</span><span class="sxs-lookup"><span data-stu-id="8baab-143">Resuming</span></span>
- <span data-ttu-id="8baab-144">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="8baab-144">Running</span></span>
- <span data-ttu-id="8baab-145">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="8baab-145">Starting</span></span>
- <span data-ttu-id="8baab-146">Funktioniert nicht mehr</span><span class="sxs-lookup"><span data-stu-id="8baab-146">Stopped</span></span>
- <span data-ttu-id="8baab-147">Beenden</span><span class="sxs-lookup"><span data-stu-id="8baab-147">Stopping</span></span>
- <span data-ttu-id="8baab-148">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="8baab-148">Suspended</span></span>
- <span data-ttu-id="8baab-149">Suspending</span><span class="sxs-lookup"><span data-stu-id="8baab-149">Suspending</span></span>

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

### <span data-ttu-id="8baab-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8baab-150">CommonParameters</span></span>
<span data-ttu-id="8baab-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8baab-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8baab-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8baab-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8baab-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8baab-153">INPUTS</span></span>

### <span data-ttu-id="8baab-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8baab-154">System.Guid</span></span>

### <span data-ttu-id="8baab-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8baab-155">System.String</span></span>

## <span data-ttu-id="8baab-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8baab-156">OUTPUTS</span></span>

### <span data-ttu-id="8baab-157">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="8baab-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="8baab-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="8baab-158">NOTES</span></span>

## <span data-ttu-id="8baab-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8baab-159">RELATED LINKS</span></span>

[<span data-ttu-id="8baab-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="8baab-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="8baab-161">Lebenslauf-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8baab-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="8baab-162">Stopp-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8baab-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="8baab-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8baab-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


