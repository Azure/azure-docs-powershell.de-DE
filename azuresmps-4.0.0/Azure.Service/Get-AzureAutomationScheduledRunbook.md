---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006563"
---
# <span data-ttu-id="19e02-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="19e02-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="19e02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19e02-102">SYNOPSIS</span></span>

<span data-ttu-id="19e02-103">Ruft Azure Automation runbooks und zugeordnete Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="19e02-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="19e02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19e02-104">SYNTAX</span></span>

### <span data-ttu-id="19e02-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="19e02-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="19e02-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="19e02-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19e02-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="19e02-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19e02-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="19e02-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19e02-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="19e02-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19e02-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19e02-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="19e02-111">Der **Get-AzureAutomationScheduledRunbook** ruft mindestens ein Azure Automation-runbooks und zugeordnete Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="19e02-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="19e02-112">Standardmäßig werden alle geplanten runbooks zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="19e02-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="19e02-113">Um einen bestimmten geplanten runbooks abzurufen, geben Sie den runbooks-Namen und den Terminplan Namen an.</span><span class="sxs-lookup"><span data-stu-id="19e02-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="19e02-114">Um alle einem runbooks zugeordneten Zeitpläne abzurufen, geben Sie nur den runbooks-Namen ein.</span><span class="sxs-lookup"><span data-stu-id="19e02-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="19e02-115">Um alle runbooks zu erhalten, die einem Terminplan zugeordnet sind, geben Sie nur den Terminplan Namen an.</span><span class="sxs-lookup"><span data-stu-id="19e02-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="19e02-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19e02-116">EXAMPLES</span></span>

### <span data-ttu-id="19e02-117">Beispiel 1: Abrufen aller geplanten runbooks</span><span class="sxs-lookup"><span data-stu-id="19e02-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="19e02-118">Dieser Befehl ruft alle geplanten runbooks im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="19e02-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="19e02-119">Beispiel 2: Abrufen aller einem runbooks zugeordneten Zeitpläne</span><span class="sxs-lookup"><span data-stu-id="19e02-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="19e02-120">Dieser Befehl ruft alle geplanten runbooks für das runbooks-Runbk01 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="19e02-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="19e02-121">Beispiel 3: Abrufen aller runbooks, die einem Terminplan zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="19e02-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="19e02-122">Dieser Befehl ruft alle geplanten runbooks für den Terminplan Schedule01 im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="19e02-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="19e02-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="19e02-123">PARAMETERS</span></span>

### <span data-ttu-id="19e02-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19e02-124">-AutomationAccountName</span></span>
<span data-ttu-id="19e02-125">Gibt den Namen eines Azure Automation-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="19e02-125">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="19e02-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="19e02-126">-JobScheduleId</span></span>
<span data-ttu-id="19e02-127">Gibt die ID eines geplanten Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="19e02-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19e02-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="19e02-128">-Profile</span></span>
<span data-ttu-id="19e02-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="19e02-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19e02-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="19e02-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19e02-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="19e02-131">-RunbookName</span></span>
<span data-ttu-id="19e02-132">Gibt den Namen einer runbooks an.</span><span class="sxs-lookup"><span data-stu-id="19e02-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19e02-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="19e02-133">-ScheduleName</span></span>
<span data-ttu-id="19e02-134">Gibt den Namen eines Zeitplans an.</span><span class="sxs-lookup"><span data-stu-id="19e02-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19e02-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e02-135">CommonParameters</span></span>
<span data-ttu-id="19e02-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e02-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e02-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e02-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e02-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19e02-138">INPUTS</span></span>

## <span data-ttu-id="19e02-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19e02-139">OUTPUTS</span></span>

### <span data-ttu-id="19e02-140">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="19e02-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="19e02-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="19e02-141">NOTES</span></span>

## <span data-ttu-id="19e02-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19e02-142">RELATED LINKS</span></span>

[<span data-ttu-id="19e02-143">Registrieren-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="19e02-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="19e02-144">Registrierung aufheben-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="19e02-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


