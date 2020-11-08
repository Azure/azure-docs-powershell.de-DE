---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008707"
---
# <span data-ttu-id="9a8e7-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9a8e7-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="9a8e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8e7-103">Entfernt eine Zuordnung zwischen einer runbooks und einem Terminplan.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="9a8e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a8e7-104">SYNTAX</span></span>

### <span data-ttu-id="9a8e7-105">ByJobScheduleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a8e7-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a8e7-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="9a8e7-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a8e7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a8e7-107">DESCRIPTION</span></span>
<span data-ttu-id="9a8e7-108">Das Cmdlet " **Unregister-AzAutomationScheduledRunbook** " entfernt die Zuordnung zwischen einem Azure Automation-runbooks und einem Terminplan.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="9a8e7-109">Der Terminplan startet nicht mehr das runbooks.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="9a8e7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a8e7-110">EXAMPLES</span></span>

### <span data-ttu-id="9a8e7-111">Beispiel 1: Entfernen der Zuordnung zwischen einer runbooks und einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="9a8e7-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="9a8e7-112">Dieser Befehl entfernt die Zuordnung zwischen dem runbooks mit dem Namen Runbk01 und dem Zeitplan mit dem Namen Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="9a8e7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a8e7-113">PARAMETERS</span></span>

### <span data-ttu-id="9a8e7-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a8e7-114">-AutomationAccountName</span></span>
<span data-ttu-id="9a8e7-115">Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9a8e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a8e7-116">-DefaultProfile</span></span>
<span data-ttu-id="9a8e7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9a8e7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a8e7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9a8e7-118">-Force</span></span>
<span data-ttu-id="9a8e7-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="9a8e7-119">ps_force</span></span>

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

### <span data-ttu-id="9a8e7-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9a8e7-120">-JobScheduleId</span></span>
<span data-ttu-id="9a8e7-121">Gibt die ID einer geplanten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="9a8e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a8e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="9a8e7-123">Gibt den Namen einer Ressourcengruppe für den geplanten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="9a8e7-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="9a8e7-124">-RunbookName</span></span>
<span data-ttu-id="9a8e7-125">Gibt den Namen der runbooks an, die dieses Cmdlet von einem Terminplan distanziert.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="9a8e7-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="9a8e7-126">-ScheduleName</span></span>
<span data-ttu-id="9a8e7-127">Gibt den Namen des Zeitplans an, aus dem dieses Cmdlet eine runbooks distanziert.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="9a8e7-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a8e7-128">-Confirm</span></span>
<span data-ttu-id="9a8e7-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a8e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a8e7-130">-WhatIf</span></span>
<span data-ttu-id="9a8e7-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a8e7-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a8e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8e7-133">CommonParameters</span></span>
<span data-ttu-id="9a8e7-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8e7-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a8e7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8e7-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a8e7-136">INPUTS</span></span>

### <span data-ttu-id="9a8e7-137">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9a8e7-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9a8e7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9a8e7-138">System.String</span></span>

## <span data-ttu-id="9a8e7-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a8e7-139">OUTPUTS</span></span>

### <span data-ttu-id="9a8e7-140">System. void</span><span class="sxs-lookup"><span data-stu-id="9a8e7-140">System.Void</span></span>

## <span data-ttu-id="9a8e7-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a8e7-141">NOTES</span></span>

## <span data-ttu-id="9a8e7-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a8e7-142">RELATED LINKS</span></span>

[<span data-ttu-id="9a8e7-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9a8e7-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="9a8e7-144">Registrieren-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9a8e7-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


