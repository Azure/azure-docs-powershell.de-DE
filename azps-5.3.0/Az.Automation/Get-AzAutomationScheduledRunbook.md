---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471345"
---
# <span data-ttu-id="9e20b-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9e20b-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="9e20b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e20b-102">SYNOPSIS</span></span>
<span data-ttu-id="9e20b-103">Ruft Automatisierungslaufbücher und zugehörige Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="9e20b-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="9e20b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e20b-104">SYNTAX</span></span>

### <span data-ttu-id="9e20b-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e20b-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e20b-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9e20b-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e20b-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="9e20b-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e20b-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="9e20b-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e20b-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="9e20b-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e20b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e20b-110">DESCRIPTION</span></span>
<span data-ttu-id="9e20b-111">Das **Cmdlet "Get-AzAutomationScheduledRunbook"** ruft mindestens ein Azure Automation Runbooks und zugeordnete Zeitpläne ab.</span><span class="sxs-lookup"><span data-stu-id="9e20b-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="9e20b-112">Dieses Cmdlet ruft standardmäßig alle geplanten Runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="9e20b-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="9e20b-113">Geben Sie den Namen eines Runbooks oder eines Zeitplans oder beides an, um bestimmte Runbookzeitpläne zu sehen.</span><span class="sxs-lookup"><span data-stu-id="9e20b-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="9e20b-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e20b-114">EXAMPLES</span></span>

### <span data-ttu-id="9e20b-115">Beispiel 1: Alle geplanten Runbooks erhalten</span><span class="sxs-lookup"><span data-stu-id="9e20b-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9e20b-116">Dieser Befehl ruft alle geplanten Runbooks im Azure-Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="9e20b-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="9e20b-117">Beispiel 2: Erhalten aller Zeitpläne, die einem Runbook zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="9e20b-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="9e20b-118">Dieser Befehl ruft alle geplanten Runbooks für das Runbook "Runbk01" im Azure-Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="9e20b-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="9e20b-119">Beispiel 3: Erhalten aller Runbooks, die einem Zeitplan zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="9e20b-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="9e20b-120">Dieser Befehl ruft alle geplanten Runbooks für den Zeitplan "Schedule01" im Azure-Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="9e20b-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9e20b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e20b-121">PARAMETERS</span></span>

### <span data-ttu-id="9e20b-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e20b-122">-AutomationAccountName</span></span>
<span data-ttu-id="9e20b-123">Gibt ein Automatisierungskonto für das Runbook an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e20b-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9e20b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e20b-124">-DefaultProfile</span></span>
<span data-ttu-id="9e20b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9e20b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e20b-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9e20b-126">-JobScheduleId</span></span>
<span data-ttu-id="9e20b-127">Gibt die ID eines geplanten Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9e20b-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e20b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e20b-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e20b-129">Gibt den Namen einer Ressourcengruppe für geplante Runbooks an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9e20b-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e20b-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="9e20b-130">-RunbookName</span></span>
<span data-ttu-id="9e20b-131">Gibt den Namen eines Runbooks an, für das dieses Cmdlet geplante Runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="9e20b-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="9e20b-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="9e20b-132">-ScheduleName</span></span>
<span data-ttu-id="9e20b-133">Gibt den Namen eines Zeitplans an, für den dieses Cmdlet geplante Runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="9e20b-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="9e20b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e20b-134">CommonParameters</span></span>
<span data-ttu-id="9e20b-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e20b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e20b-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e20b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e20b-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e20b-137">INPUTS</span></span>

### <span data-ttu-id="9e20b-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e20b-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e20b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9e20b-139">System.String</span></span>

## <span data-ttu-id="9e20b-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e20b-140">OUTPUTS</span></span>

### <span data-ttu-id="9e20b-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="9e20b-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="9e20b-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e20b-142">NOTES</span></span>

## <span data-ttu-id="9e20b-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e20b-143">RELATED LINKS</span></span>

[<span data-ttu-id="9e20b-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9e20b-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="9e20b-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9e20b-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


