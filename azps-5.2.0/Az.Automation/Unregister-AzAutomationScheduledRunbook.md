---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297017"
---
# <span data-ttu-id="108af-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="108af-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="108af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="108af-102">SYNOPSIS</span></span>
<span data-ttu-id="108af-103">Entfernt eine Zuordnung zwischen einem Runbook und einem Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="108af-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="108af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="108af-104">SYNTAX</span></span>

### <span data-ttu-id="108af-105">ByJobScheduleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="108af-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="108af-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="108af-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="108af-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="108af-107">DESCRIPTION</span></span>
<span data-ttu-id="108af-108">Das **Cmdlet "Unregister-AzAutomationScheduledRunbook"** entfernt die Zuordnung zwischen einem Azure Automation Runbook und einem Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="108af-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="108af-109">Der Zeitplan startet das Runbook nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="108af-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="108af-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="108af-110">EXAMPLES</span></span>

### <span data-ttu-id="108af-111">Beispiel 1: Entfernen der Zuordnung zwischen einem Runbook und einem Zeitplan</span><span class="sxs-lookup"><span data-stu-id="108af-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="108af-112">Mit diesem Befehl wird die Zuordnung zwischen dem Runbook mit dem Namen "Runbk01" und dem Zeitplan "Runbk01Sched" entfernt.</span><span class="sxs-lookup"><span data-stu-id="108af-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="108af-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="108af-113">PARAMETERS</span></span>

### <span data-ttu-id="108af-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="108af-114">-AutomationAccountName</span></span>
<span data-ttu-id="108af-115">Gibt ein Automatisierungskonto für das Runbook an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="108af-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="108af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108af-116">-DefaultProfile</span></span>
<span data-ttu-id="108af-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="108af-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="108af-118">-Force</span><span class="sxs-lookup"><span data-stu-id="108af-118">-Force</span></span>
<span data-ttu-id="108af-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="108af-119">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108af-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="108af-120">-JobScheduleId</span></span>
<span data-ttu-id="108af-121">Gibt die ID eines geplanten Runbook an.</span><span class="sxs-lookup"><span data-stu-id="108af-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="108af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="108af-122">-ResourceGroupName</span></span>
<span data-ttu-id="108af-123">Gibt den Namen einer Ressourcengruppe für das geplante Runbook an.</span><span class="sxs-lookup"><span data-stu-id="108af-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="108af-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="108af-124">-RunbookName</span></span>
<span data-ttu-id="108af-125">Gibt den Namen des Runbook an, das dieses Cmdlet von einem Zeitplan entfernt.</span><span class="sxs-lookup"><span data-stu-id="108af-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108af-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="108af-126">-ScheduleName</span></span>
<span data-ttu-id="108af-127">Gibt den Namen des Zeitplans an, aus dem dieses Cmdlet ein Runbook entfernt.</span><span class="sxs-lookup"><span data-stu-id="108af-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108af-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="108af-128">-Confirm</span></span>
<span data-ttu-id="108af-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="108af-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108af-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="108af-130">-WhatIf</span></span>
<span data-ttu-id="108af-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="108af-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="108af-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="108af-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108af-133">CommonParameters</span></span>
<span data-ttu-id="108af-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108af-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="108af-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108af-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="108af-136">INPUTS</span></span>

### <span data-ttu-id="108af-137">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="108af-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="108af-138">System.String</span><span class="sxs-lookup"><span data-stu-id="108af-138">System.String</span></span>

## <span data-ttu-id="108af-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="108af-139">OUTPUTS</span></span>

### <span data-ttu-id="108af-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="108af-140">System.Void</span></span>

## <span data-ttu-id="108af-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="108af-141">NOTES</span></span>

## <span data-ttu-id="108af-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="108af-142">RELATED LINKS</span></span>

[<span data-ttu-id="108af-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="108af-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="108af-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="108af-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


