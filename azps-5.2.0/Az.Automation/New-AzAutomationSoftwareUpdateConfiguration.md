---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373455"
---
# <span data-ttu-id="5f42d-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f42d-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="5f42d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f42d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f42d-103">Erstellt eine geplante Konfiguration der Softwareupdatekonfiguration für die Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="5f42d-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="5f42d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f42d-104">SYNTAX</span></span>

### <span data-ttu-id="5f42d-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f42d-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f42d-106">Linux</span><span class="sxs-lookup"><span data-stu-id="5f42d-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f42d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f42d-107">DESCRIPTION</span></span>
<span data-ttu-id="5f42d-108">Erstellt eine Softwareupdatekonfiguration, die nach einem Zeitplan zum Aktualisieren einer Liste von Computern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f42d-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="5f42d-109">Computer umfassen sowohl virtuelle Azure-Computer als auch Nicht-Az-Computer.</span><span class="sxs-lookup"><span data-stu-id="5f42d-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="5f42d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f42d-110">EXAMPLES</span></span>

### <span data-ttu-id="5f42d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f42d-111">Example 1</span></span>
<span data-ttu-id="5f42d-112">Erstellt einmal am Samstag 21:00 Uhr eine Softwareupdatekonfiguration, um wichtige Updates auf zwei virtuellen Windows Azure-Computern zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5f42d-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="5f42d-113">In diesem Beispiel ist die Aktualisierungsdauer auf 2 Stunden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5f42d-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="5f42d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f42d-114">PARAMETERS</span></span>

### <span data-ttu-id="5f42d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f42d-115">-AutomationAccountName</span></span>
<span data-ttu-id="5f42d-116">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="5f42d-116">The automation account name.</span></span>

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

### <span data-ttu-id="5f42d-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="5f42d-117">-AzureQuery</span></span>
<span data-ttu-id="5f42d-118">Dynamische Gruppen-Azure-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5f42d-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="5f42d-119">-AzureVMResourceId</span></span>
<span data-ttu-id="5f42d-120">Ressourcen-IDs für virtuelle Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="5f42d-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f42d-121">-DefaultProfile</span></span>
<span data-ttu-id="5f42d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f42d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-123">-Duration</span><span class="sxs-lookup"><span data-stu-id="5f42d-123">-Duration</span></span>
<span data-ttu-id="5f42d-124">Maximale Dauer für das Update.</span><span class="sxs-lookup"><span data-stu-id="5f42d-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="5f42d-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="5f42d-126">KB-Nummern ausgeschlossener Aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="5f42d-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="5f42d-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="5f42d-128">Ausgeschlossene Linux-Paketmasken.</span><span class="sxs-lookup"><span data-stu-id="5f42d-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="5f42d-129">-IncludedKbNumber</span></span>
<span data-ttu-id="5f42d-130">KB-Nummern enthaltener Updates.</span><span class="sxs-lookup"><span data-stu-id="5f42d-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="5f42d-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="5f42d-132">Enthaltene Linux-Paketklassifizierungen.</span><span class="sxs-lookup"><span data-stu-id="5f42d-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="5f42d-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="5f42d-134">Enthaltene Linux-Paketmasken.</span><span class="sxs-lookup"><span data-stu-id="5f42d-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="5f42d-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="5f42d-136">Windows Update-Klassifizierungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f42d-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="5f42d-137">-Linux</span></span>
<span data-ttu-id="5f42d-138">Gibt an, dass die Softwareupdatekonfiguration für die Computer des Betriebssystems Linux verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f42d-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="5f42d-139">-NonAzureComputer</span></span>
<span data-ttu-id="5f42d-140">Nicht-Az-Computernamen.</span><span class="sxs-lookup"><span data-stu-id="5f42d-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="5f42d-141">-NonAzureQuery</span></span>
<span data-ttu-id="5f42d-142">Dynamische Gruppe, nicht Azure-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5f42d-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="5f42d-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="5f42d-144">Aufgabe posten</span><span class="sxs-lookup"><span data-stu-id="5f42d-144">Post task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="5f42d-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="5f42d-146">Parameter "Aufgabe posten" aus.</span><span class="sxs-lookup"><span data-stu-id="5f42d-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="5f42d-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="5f42d-148">"Voraufgabe" aus.</span><span class="sxs-lookup"><span data-stu-id="5f42d-148">Pre task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="5f42d-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="5f42d-150">Parameter für die Voraufgabe.</span><span class="sxs-lookup"><span data-stu-id="5f42d-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="5f42d-151">-RebootOnly</span></span>
<span data-ttu-id="5f42d-152">Gibt an, dass die Softwareupdatekonfiguration nur die Computer neu startet.</span><span class="sxs-lookup"><span data-stu-id="5f42d-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="5f42d-153">-RebootSetting</span></span>
<span data-ttu-id="5f42d-154">Neustarteinstellung.</span><span class="sxs-lookup"><span data-stu-id="5f42d-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f42d-155">-ResourceGroupName</span></span>
<span data-ttu-id="5f42d-156">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5f42d-156">The resource group name.</span></span>

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

### <span data-ttu-id="5f42d-157">-Schedule</span><span class="sxs-lookup"><span data-stu-id="5f42d-157">-Schedule</span></span>
<span data-ttu-id="5f42d-158">Planen sie das Objekt, das für die Softwareupdatekonfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f42d-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="5f42d-159">-Windows</span></span>
<span data-ttu-id="5f42d-160">Gibt an, dass die Softwareupdatekonfiguration für Die Computer des Betriebssystems Windows verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f42d-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f42d-161">-Confirm</span></span>
<span data-ttu-id="5f42d-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f42d-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-163">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5f42d-163">-WhatIf</span></span>
<span data-ttu-id="5f42d-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f42d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f42d-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f42d-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f42d-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f42d-166">CommonParameters</span></span>
<span data-ttu-id="5f42d-167">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f42d-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f42d-168">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f42d-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f42d-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f42d-169">INPUTS</span></span>

### <span data-ttu-id="5f42d-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="5f42d-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="5f42d-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f42d-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5f42d-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5f42d-172">System.String[]</span></span>

### <span data-ttu-id="5f42d-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="5f42d-173">System.TimeSpan</span></span>

### <span data-ttu-id="5f42d-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="5f42d-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="5f42d-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="5f42d-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="5f42d-176">System.String</span><span class="sxs-lookup"><span data-stu-id="5f42d-176">System.String</span></span>

## <span data-ttu-id="5f42d-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f42d-177">OUTPUTS</span></span>

### <span data-ttu-id="5f42d-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f42d-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="5f42d-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5f42d-179">NOTES</span></span>

## <span data-ttu-id="5f42d-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5f42d-180">RELATED LINKS</span></span>
