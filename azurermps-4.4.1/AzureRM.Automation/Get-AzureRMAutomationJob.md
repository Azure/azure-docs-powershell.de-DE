---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505682"
---
# <span data-ttu-id="f564a-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f564a-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="f564a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f564a-102">SYNOPSIS</span></span>
<span data-ttu-id="f564a-103">Ruft Automatisierungs runbooks Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="f564a-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f564a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f564a-104">SYNTAX</span></span>

### <span data-ttu-id="f564a-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="f564a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f564a-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="f564a-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f564a-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="f564a-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f564a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f564a-108">DESCRIPTION</span></span>
<span data-ttu-id="f564a-109">Das Cmdlet " **Get-AzureRmAutomationJob** " ruft runbooks-Aufträge in Azure-Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="f564a-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="f564a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f564a-110">EXAMPLES</span></span>

### <span data-ttu-id="f564a-111">Beispiel 1: Abrufen eines bestimmten runbooks-Auftrags</span><span class="sxs-lookup"><span data-stu-id="f564a-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="f564a-112">Dieser Befehl ruft den Auftrag ab, der die angegebene GUID aufweist.</span><span class="sxs-lookup"><span data-stu-id="f564a-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="f564a-113">Beispiel 2: Abrufen aller Aufträge für eine runbooks</span><span class="sxs-lookup"><span data-stu-id="f564a-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="f564a-114">Dieser Befehl ruft alle Aufträge ab, die einem runbooks mit dem Namen Runbook02 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f564a-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="f564a-115">Beispiel 3: Abrufen aller ausgeführten Aufträge</span><span class="sxs-lookup"><span data-stu-id="f564a-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="f564a-116">Dieser Befehl ruft alle ausgeführten Aufträge im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="f564a-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f564a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f564a-117">PARAMETERS</span></span>

### <span data-ttu-id="f564a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f564a-118">-AutomationAccountName</span></span>
<span data-ttu-id="f564a-119">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="f564a-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="f564a-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f564a-120">-EndTime</span></span>
<span data-ttu-id="f564a-121">Gibt die Endzeit für einen Auftrag als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f564a-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="f564a-122">Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f564a-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="f564a-123">Dieses Cmdlet ruft Aufträge ab, die eine Endzeit am oder vor dem Wert aufweisen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f564a-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="f564a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f564a-124">-Id</span></span>
<span data-ttu-id="f564a-125">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f564a-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f564a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f564a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f564a-127">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="f564a-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="f564a-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="f564a-128">-RunbookName</span></span>
<span data-ttu-id="f564a-129">Gibt den Namen einer runbooks an, für die dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="f564a-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="f564a-130">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="f564a-130">-StartTime</span></span>
<span data-ttu-id="f564a-131">Gibt die Startzeit eines Auftrags als **DateTimeOffset** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f564a-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="f564a-132">Dieses Cmdlet ruft Aufträge ab, die eine Startzeit am oder hinter dem Wert haben, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f564a-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="f564a-133">-Status</span><span class="sxs-lookup"><span data-stu-id="f564a-133">-Status</span></span>
<span data-ttu-id="f564a-134">Gibt den Status eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="f564a-134">Specifies the status of a job.</span></span>
<span data-ttu-id="f564a-135">Dieses Cmdlet ruft Aufträge ab, deren Status diesem Parameter entspricht.</span><span class="sxs-lookup"><span data-stu-id="f564a-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="f564a-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f564a-136">Valid values are:</span></span> 

- <span data-ttu-id="f564a-137">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="f564a-137">Activating</span></span>
- <span data-ttu-id="f564a-138">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="f564a-138">Completed</span></span>
- <span data-ttu-id="f564a-139">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="f564a-139">Failed</span></span>
- <span data-ttu-id="f564a-140">Queued</span><span class="sxs-lookup"><span data-stu-id="f564a-140">Queued</span></span>
- <span data-ttu-id="f564a-141">Wieder</span><span class="sxs-lookup"><span data-stu-id="f564a-141">Resuming</span></span>
- <span data-ttu-id="f564a-142">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="f564a-142">Running</span></span>
- <span data-ttu-id="f564a-143">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="f564a-143">Starting</span></span>
- <span data-ttu-id="f564a-144">Funktioniert nicht mehr</span><span class="sxs-lookup"><span data-stu-id="f564a-144">Stopped</span></span>
- <span data-ttu-id="f564a-145">Beenden</span><span class="sxs-lookup"><span data-stu-id="f564a-145">Stopping</span></span>
- <span data-ttu-id="f564a-146">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="f564a-146">Suspended</span></span>
- <span data-ttu-id="f564a-147">Suspending</span><span class="sxs-lookup"><span data-stu-id="f564a-147">Suspending</span></span>

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

### <span data-ttu-id="f564a-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f564a-148">-DefaultProfile</span></span>
<span data-ttu-id="f564a-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f564a-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f564a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f564a-150">CommonParameters</span></span>
<span data-ttu-id="f564a-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f564a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f564a-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f564a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f564a-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f564a-153">INPUTS</span></span>

## <span data-ttu-id="f564a-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f564a-154">OUTPUTS</span></span>

### <span data-ttu-id="f564a-155">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="f564a-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="f564a-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="f564a-156">NOTES</span></span>

## <span data-ttu-id="f564a-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f564a-157">RELATED LINKS</span></span>

[<span data-ttu-id="f564a-158">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f564a-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="f564a-159">Lebenslauf-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f564a-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="f564a-160">Stopp-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f564a-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="f564a-161">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="f564a-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


