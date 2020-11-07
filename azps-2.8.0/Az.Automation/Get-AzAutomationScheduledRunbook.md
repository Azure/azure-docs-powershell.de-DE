---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 2444579c8a155cc2957ab8432eb63cc28300bfe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658040"
---
# <span data-ttu-id="d2e77-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d2e77-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="d2e77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2e77-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e77-103">Ruft Automatisierungs runbooks und zugeordnete Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="d2e77-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="d2e77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2e77-104">SYNTAX</span></span>

### <span data-ttu-id="d2e77-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2e77-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e77-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d2e77-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e77-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="d2e77-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e77-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="d2e77-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2e77-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="d2e77-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e77-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2e77-110">DESCRIPTION</span></span>
<span data-ttu-id="d2e77-111">Das Cmdlet " **Get-AzAutomationScheduledRunbook** " Ruft einen oder mehrere Azure Automation-runbooks und zugeordnete Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="d2e77-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="d2e77-112">Standardmäßig ruft dieses Cmdlet alle geplanten runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="d2e77-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="d2e77-113">Geben Sie den Namen eines runbooks oder einen Terminplan oder beides an, um bestimmte runbooks-Zeitpläne anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d2e77-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="d2e77-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2e77-114">EXAMPLES</span></span>

### <span data-ttu-id="d2e77-115">Beispiel 1: Abrufen aller geplanten runbooks</span><span class="sxs-lookup"><span data-stu-id="d2e77-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d2e77-116">Dieser Befehl ruft alle geplanten runbooks im Azure Automation-Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="d2e77-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="d2e77-117">Beispiel 2: Abrufen aller einem runbooks zugeordneten Zeitpläne</span><span class="sxs-lookup"><span data-stu-id="d2e77-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="d2e77-118">Dieser Befehl ruft alle geplanten runbooks für das runbooks-Runbk01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="d2e77-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="d2e77-119">Beispiel 3: Abrufen aller runbooks, die einem Terminplan zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="d2e77-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="d2e77-120">Dieser Befehl ruft alle geplanten runbooks für den Terminplan-Schedule01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="d2e77-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d2e77-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2e77-121">PARAMETERS</span></span>

### <span data-ttu-id="d2e77-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d2e77-122">-AutomationAccountName</span></span>
<span data-ttu-id="d2e77-123">Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2e77-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d2e77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e77-124">-DefaultProfile</span></span>
<span data-ttu-id="d2e77-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d2e77-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2e77-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d2e77-126">-JobScheduleId</span></span>
<span data-ttu-id="d2e77-127">Gibt die ID eines geplanten Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d2e77-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e77-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e77-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2e77-129">Gibt den Namen einer Ressourcengruppe für geplante runbooks an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d2e77-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d2e77-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d2e77-130">-RunbookName</span></span>
<span data-ttu-id="d2e77-131">Gibt den Namen einer runbooks an, für die dieses Cmdlet geplante runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="d2e77-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e77-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="d2e77-132">-ScheduleName</span></span>
<span data-ttu-id="d2e77-133">Gibt den Namen eines Zeitplans an, für den dieses Cmdlet geplante runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="d2e77-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e77-134">CommonParameters</span></span>
<span data-ttu-id="d2e77-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e77-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e77-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e77-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2e77-137">INPUTS</span></span>

### <span data-ttu-id="d2e77-138">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d2e77-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d2e77-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e77-139">System.String</span></span>

## <span data-ttu-id="d2e77-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2e77-140">OUTPUTS</span></span>

### <span data-ttu-id="d2e77-141">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="d2e77-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="d2e77-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2e77-142">NOTES</span></span>

## <span data-ttu-id="d2e77-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2e77-143">RELATED LINKS</span></span>

[<span data-ttu-id="d2e77-144">Registrieren-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d2e77-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="d2e77-145">Registrierung aufheben-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d2e77-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


