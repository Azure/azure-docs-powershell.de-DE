---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: ab55201ab2566c814455b6b0f6fe3c2ddf6b3a57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502257"
---
# <span data-ttu-id="646ce-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="646ce-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="646ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="646ce-102">SYNOPSIS</span></span>
<span data-ttu-id="646ce-103">Entfernt eine Zuordnung zwischen einer runbooks und einem Terminplan.</span><span class="sxs-lookup"><span data-stu-id="646ce-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="646ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="646ce-104">SYNTAX</span></span>

### <span data-ttu-id="646ce-105">ByJobScheduleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="646ce-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="646ce-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="646ce-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="646ce-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="646ce-107">DESCRIPTION</span></span>
<span data-ttu-id="646ce-108">Das Cmdlet " **Unregister-AzureRmAutomationScheduledRunbook** " entfernt die Zuordnung zwischen einem Azure Automation-runbooks und einem Terminplan.</span><span class="sxs-lookup"><span data-stu-id="646ce-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="646ce-109">Der Terminplan startet nicht mehr das runbooks.</span><span class="sxs-lookup"><span data-stu-id="646ce-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="646ce-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="646ce-110">EXAMPLES</span></span>

### <span data-ttu-id="646ce-111">Beispiel 1: Entfernen der Zuordnung zwischen einer runbooks und einem Terminplan</span><span class="sxs-lookup"><span data-stu-id="646ce-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="646ce-112">Dieser Befehl entfernt die Zuordnung zwischen dem runbooks mit dem Namen Runbk01 und dem Zeitplan mit dem Namen Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="646ce-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="646ce-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="646ce-113">PARAMETERS</span></span>

### <span data-ttu-id="646ce-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="646ce-114">-AutomationAccountName</span></span>
<span data-ttu-id="646ce-115">Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="646ce-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="646ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646ce-116">-DefaultProfile</span></span>
<span data-ttu-id="646ce-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="646ce-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="646ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="646ce-118">-Force</span></span>
<span data-ttu-id="646ce-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="646ce-119">ps_force</span></span>

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

### <span data-ttu-id="646ce-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="646ce-120">-JobScheduleId</span></span>
<span data-ttu-id="646ce-121">Gibt die ID einer geplanten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="646ce-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="646ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="646ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="646ce-123">Gibt den Namen einer Ressourcengruppe für den geplanten runbooks an.</span><span class="sxs-lookup"><span data-stu-id="646ce-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="646ce-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="646ce-124">-RunbookName</span></span>
<span data-ttu-id="646ce-125">Gibt den Namen der runbooks an, die dieses Cmdlet von einem Terminplan distanziert.</span><span class="sxs-lookup"><span data-stu-id="646ce-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="646ce-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="646ce-126">-ScheduleName</span></span>
<span data-ttu-id="646ce-127">Gibt den Namen des Zeitplans an, aus dem dieses Cmdlet eine runbooks distanziert.</span><span class="sxs-lookup"><span data-stu-id="646ce-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="646ce-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="646ce-128">-Confirm</span></span>
<span data-ttu-id="646ce-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="646ce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="646ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="646ce-130">-WhatIf</span></span>
<span data-ttu-id="646ce-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="646ce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="646ce-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="646ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="646ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646ce-133">CommonParameters</span></span>
<span data-ttu-id="646ce-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646ce-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="646ce-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646ce-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="646ce-136">INPUTS</span></span>

### <span data-ttu-id="646ce-137">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="646ce-137">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="646ce-138">System. String</span><span class="sxs-lookup"><span data-stu-id="646ce-138">System.String</span></span>

## <span data-ttu-id="646ce-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="646ce-139">OUTPUTS</span></span>

### <span data-ttu-id="646ce-140">System. void</span><span class="sxs-lookup"><span data-stu-id="646ce-140">System.Void</span></span>

## <span data-ttu-id="646ce-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="646ce-141">NOTES</span></span>

## <span data-ttu-id="646ce-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="646ce-142">RELATED LINKS</span></span>

[<span data-ttu-id="646ce-143">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="646ce-143">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="646ce-144">Registrieren-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="646ce-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


