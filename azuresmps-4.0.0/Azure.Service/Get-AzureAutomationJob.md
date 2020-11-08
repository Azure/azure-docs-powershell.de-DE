---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006575"
---
# <span data-ttu-id="38634-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38634-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="38634-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38634-102">SYNOPSIS</span></span>

<span data-ttu-id="38634-103">Ruft einen oder mehrere Azure Automation runbooks-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="38634-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="38634-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38634-104">SYNTAX</span></span>

### <span data-ttu-id="38634-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="38634-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="38634-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="38634-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="38634-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="38634-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="38634-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38634-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="38634-109">Das Cmdlet " **Get-AzureAutomationJob** " Ruft einen oder mehrere runbooks-Aufträge in Microsoft Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="38634-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="38634-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38634-110">EXAMPLES</span></span>

### <span data-ttu-id="38634-111">Beispiel 1: Abrufen eines bestimmten runbooks-Auftrags</span><span class="sxs-lookup"><span data-stu-id="38634-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="38634-112">Dieser Befehl ruft den Auftrag ab, der die angegebene GUID aufweist.</span><span class="sxs-lookup"><span data-stu-id="38634-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="38634-113">Beispiel 2: Abrufen aller Aufträge für eine runbooks</span><span class="sxs-lookup"><span data-stu-id="38634-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="38634-114">Dieser Befehl ruft alle Aufträge ab, die einem runbooks mit dem Namen MyRunbook zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="38634-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="38634-115">Beispiel 2: Abrufen aller ausgeführten Aufträge</span><span class="sxs-lookup"><span data-stu-id="38634-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="38634-116">Dieser Befehl ruft alle ausgeführten Aufträge im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="38634-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="38634-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="38634-117">PARAMETERS</span></span>

### <span data-ttu-id="38634-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38634-118">-AutomationAccountName</span></span>
<span data-ttu-id="38634-119">Gibt den Namen eines Azure Automation-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="38634-119">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="38634-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="38634-120">-EndTime</span></span>
<span data-ttu-id="38634-121">Gibt die Endzeit für einen Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="38634-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38634-122">-ID</span><span class="sxs-lookup"><span data-stu-id="38634-122">-Id</span></span>
<span data-ttu-id="38634-123">Gibt die ID eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="38634-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38634-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="38634-124">-Profile</span></span>
<span data-ttu-id="38634-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="38634-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38634-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="38634-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38634-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="38634-127">-RunbookName</span></span>
<span data-ttu-id="38634-128">Gibt den Namen einer runbooks an.</span><span class="sxs-lookup"><span data-stu-id="38634-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38634-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="38634-129">-StartTime</span></span>
<span data-ttu-id="38634-130">Gibt die Startzeit eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="38634-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38634-131">-Status</span><span class="sxs-lookup"><span data-stu-id="38634-131">-Status</span></span>
<span data-ttu-id="38634-132">Gibt den Status eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="38634-132">Specifies the status of a job.</span></span>
<span data-ttu-id="38634-133">Dieses Cmdlet ruft Aufträge ab, deren Status diesem Parameter entspricht.</span><span class="sxs-lookup"><span data-stu-id="38634-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="38634-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="38634-134">Valid values are:</span></span> 

- <span data-ttu-id="38634-135">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="38634-135">Completed</span></span>
- <span data-ttu-id="38634-136">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="38634-136">Failed</span></span>
- <span data-ttu-id="38634-137">Queued</span><span class="sxs-lookup"><span data-stu-id="38634-137">Queued</span></span>
- <span data-ttu-id="38634-138">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="38634-138">Starting</span></span>
- <span data-ttu-id="38634-139">Wieder</span><span class="sxs-lookup"><span data-stu-id="38634-139">Resuming</span></span>
- <span data-ttu-id="38634-140">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="38634-140">Running</span></span>
- <span data-ttu-id="38634-141">Funktioniert nicht mehr</span><span class="sxs-lookup"><span data-stu-id="38634-141">Stopped</span></span>
- <span data-ttu-id="38634-142">Beenden</span><span class="sxs-lookup"><span data-stu-id="38634-142">Stopping</span></span>
- <span data-ttu-id="38634-143">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="38634-143">Suspended</span></span>
- <span data-ttu-id="38634-144">Suspending</span><span class="sxs-lookup"><span data-stu-id="38634-144">Suspending</span></span>
- <span data-ttu-id="38634-145">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="38634-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38634-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38634-146">CommonParameters</span></span>
<span data-ttu-id="38634-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38634-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38634-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38634-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38634-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38634-149">INPUTS</span></span>

## <span data-ttu-id="38634-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38634-150">OUTPUTS</span></span>

### <span data-ttu-id="38634-151">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="38634-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="38634-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="38634-152">NOTES</span></span>

## <span data-ttu-id="38634-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38634-153">RELATED LINKS</span></span>

[<span data-ttu-id="38634-154">Lebenslauf-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38634-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="38634-155">Stopp-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38634-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="38634-156">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38634-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


