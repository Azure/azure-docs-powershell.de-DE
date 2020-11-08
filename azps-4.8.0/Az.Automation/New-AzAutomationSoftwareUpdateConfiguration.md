---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008132"
---
# <span data-ttu-id="d22f6-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d22f6-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d22f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d22f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d22f6-103">Erstellt eine geplante Azure-Automatisierungs-Software Update Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d22f6-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="d22f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d22f6-104">SYNTAX</span></span>

### <span data-ttu-id="d22f6-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="d22f6-105">Windows (Default)</span></span>
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

### <span data-ttu-id="d22f6-106">Linux</span><span class="sxs-lookup"><span data-stu-id="d22f6-106">Linux</span></span>
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

## <span data-ttu-id="d22f6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d22f6-107">DESCRIPTION</span></span>
<span data-ttu-id="d22f6-108">Erstellt eine Software Update Konfiguration, die nach einem Zeitplan ausgeführt wird, um eine Liste der Computer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d22f6-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="d22f6-109">Computer sind sowohl Azure Virtual Machines als auch nicht-AZ-Computer.</span><span class="sxs-lookup"><span data-stu-id="d22f6-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="d22f6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d22f6-110">EXAMPLES</span></span>

### <span data-ttu-id="d22f6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d22f6-111">Example 1</span></span>
<span data-ttu-id="d22f6-112">Erstellt eine Software Update Konfiguration, um wichtige Updates auf zwei virtuellen Windows Azure-Computern einmal jeden Samstag 9PM zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d22f6-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="d22f6-113">Die Aktualisierungsdauer ist in diesem Beispiel auf 2 Stunden eingestellt.</span><span class="sxs-lookup"><span data-stu-id="d22f6-113">Update duration is set to 2 hours in this example.</span></span>

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

## <span data-ttu-id="d22f6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d22f6-114">PARAMETERS</span></span>

### <span data-ttu-id="d22f6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d22f6-115">-AutomationAccountName</span></span>
<span data-ttu-id="d22f6-116">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="d22f6-116">The automation account name.</span></span>

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

### <span data-ttu-id="d22f6-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="d22f6-117">-AzureQuery</span></span>
<span data-ttu-id="d22f6-118">Dynamische Gruppe Azure-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="d22f6-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="d22f6-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="d22f6-119">-AzureVMResourceId</span></span>
<span data-ttu-id="d22f6-120">Ressourcen-IDs für Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="d22f6-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="d22f6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22f6-121">-DefaultProfile</span></span>
<span data-ttu-id="d22f6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d22f6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d22f6-123">-Dauer</span><span class="sxs-lookup"><span data-stu-id="d22f6-123">-Duration</span></span>
<span data-ttu-id="d22f6-124">Maximale Dauer für das Update.</span><span class="sxs-lookup"><span data-stu-id="d22f6-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="d22f6-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="d22f6-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="d22f6-126">KB-Nummern von ausgeschlossenen Updates.</span><span class="sxs-lookup"><span data-stu-id="d22f6-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="d22f6-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="d22f6-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="d22f6-128">Ausgeschlossene Linux-Paket Masken.</span><span class="sxs-lookup"><span data-stu-id="d22f6-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="d22f6-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="d22f6-129">-IncludedKbNumber</span></span>
<span data-ttu-id="d22f6-130">KB-Nummern der enthaltenen Updates.</span><span class="sxs-lookup"><span data-stu-id="d22f6-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="d22f6-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="d22f6-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="d22f6-132">Eingeschlossene Linux-Paket Klassifizierungen.</span><span class="sxs-lookup"><span data-stu-id="d22f6-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="d22f6-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="d22f6-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="d22f6-134">Enthaltene Linux-Paket Masken.</span><span class="sxs-lookup"><span data-stu-id="d22f6-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="d22f6-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="d22f6-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="d22f6-136">Windows Update-Klassifikationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d22f6-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="d22f6-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="d22f6-137">-Linux</span></span>
<span data-ttu-id="d22f6-138">Gibt an, dass die Software Update-Konfiguration auf Linux-Betriebssystem Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="d22f6-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="d22f6-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="d22f6-139">-NonAzureComputer</span></span>
<span data-ttu-id="d22f6-140">Nicht-AZ-Computernamen.</span><span class="sxs-lookup"><span data-stu-id="d22f6-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="d22f6-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="d22f6-141">-NonAzureQuery</span></span>
<span data-ttu-id="d22f6-142">Dynamische Gruppe, nicht Azure-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="d22f6-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="d22f6-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="d22f6-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="d22f6-144">Aufgabe Posten</span><span class="sxs-lookup"><span data-stu-id="d22f6-144">Post task.</span></span>

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

### <span data-ttu-id="d22f6-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="d22f6-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="d22f6-146">Post-Vorgangsparameter</span><span class="sxs-lookup"><span data-stu-id="d22f6-146">Post task parameter.</span></span>

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

### <span data-ttu-id="d22f6-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="d22f6-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="d22f6-148">Pre-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="d22f6-148">Pre task.</span></span>

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

### <span data-ttu-id="d22f6-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="d22f6-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="d22f6-150">Parameter für Pre-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="d22f6-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="d22f6-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="d22f6-151">-RebootOnly</span></span>
<span data-ttu-id="d22f6-152">Gibt an, dass die Software Update Konfiguration nur die Computer neu startet.</span><span class="sxs-lookup"><span data-stu-id="d22f6-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="d22f6-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="d22f6-153">-RebootSetting</span></span>
<span data-ttu-id="d22f6-154">Neustart-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="d22f6-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="d22f6-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d22f6-155">-ResourceGroupName</span></span>
<span data-ttu-id="d22f6-156">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d22f6-156">The resource group name.</span></span>

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

### <span data-ttu-id="d22f6-157">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="d22f6-157">-Schedule</span></span>
<span data-ttu-id="d22f6-158">Schedule-Objekt, das für die Software Update Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d22f6-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="d22f6-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="d22f6-159">-Windows</span></span>
<span data-ttu-id="d22f6-160">Gibt an, dass die Software Update-Konfiguration auf Windows-Betriebssystem Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="d22f6-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="d22f6-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d22f6-161">-Confirm</span></span>
<span data-ttu-id="d22f6-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d22f6-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d22f6-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d22f6-163">-WhatIf</span></span>
<span data-ttu-id="d22f6-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d22f6-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d22f6-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d22f6-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d22f6-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22f6-166">CommonParameters</span></span>
<span data-ttu-id="d22f6-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22f6-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22f6-168">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22f6-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22f6-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d22f6-169">INPUTS</span></span>

### <span data-ttu-id="d22f6-170">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="d22f6-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="d22f6-171">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d22f6-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d22f6-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="d22f6-172">System.String[]</span></span>

### <span data-ttu-id="d22f6-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="d22f6-173">System.TimeSpan</span></span>

### <span data-ttu-id="d22f6-174">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="d22f6-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="d22f6-175">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="d22f6-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="d22f6-176">System. String</span><span class="sxs-lookup"><span data-stu-id="d22f6-176">System.String</span></span>

## <span data-ttu-id="d22f6-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d22f6-177">OUTPUTS</span></span>

### <span data-ttu-id="d22f6-178">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d22f6-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d22f6-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="d22f6-179">NOTES</span></span>

## <span data-ttu-id="d22f6-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d22f6-180">RELATED LINKS</span></span>
