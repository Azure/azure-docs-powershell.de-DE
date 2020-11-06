---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498498"
---
# <span data-ttu-id="59f86-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="59f86-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="59f86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59f86-102">SYNOPSIS</span></span>
<span data-ttu-id="59f86-103">Erstellt eine geplante Azure-Automatisierungs-Software Update Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="59f86-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59f86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59f86-104">SYNTAX</span></span>

### <span data-ttu-id="59f86-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="59f86-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f86-106">Linux</span><span class="sxs-lookup"><span data-stu-id="59f86-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59f86-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59f86-107">DESCRIPTION</span></span>
<span data-ttu-id="59f86-108">Erstellt eine Software Update Konfiguration, die nach einem Zeitplan ausgeführt wird, um eine Liste der Computer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="59f86-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="59f86-109">Computer sind sowohl Azure Virtual Machines als auch nicht-Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="59f86-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="59f86-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59f86-110">EXAMPLES</span></span>

### <span data-ttu-id="59f86-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59f86-111">Example 1</span></span>
<span data-ttu-id="59f86-112">Erstellt eine Software Update Konfiguration, um wichtige Updates auf zwei virtuellen Windows Azure-Computern einmal jeden Samstag 9PM zu installieren.</span><span class="sxs-lookup"><span data-stu-id="59f86-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="59f86-113">Die Aktualisierungsdauer ist in diesem Beispiel auf 2 Stunden eingestellt.</span><span class="sxs-lookup"><span data-stu-id="59f86-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="59f86-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="59f86-114">PARAMETERS</span></span>

### <span data-ttu-id="59f86-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="59f86-115">-AutomationAccountName</span></span>
<span data-ttu-id="59f86-116">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="59f86-116">The automation account name.</span></span>

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

### <span data-ttu-id="59f86-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="59f86-117">-AzureVMResourceId</span></span>
<span data-ttu-id="59f86-118">Ressourcen-IDs für Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="59f86-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="59f86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f86-119">-DefaultProfile</span></span>
<span data-ttu-id="59f86-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59f86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f86-121">-Dauer</span><span class="sxs-lookup"><span data-stu-id="59f86-121">-Duration</span></span>
<span data-ttu-id="59f86-122">Maximale Dauer für das Update.</span><span class="sxs-lookup"><span data-stu-id="59f86-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="59f86-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="59f86-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="59f86-124">KB-Nummern von ausgeschlossenen Updates.</span><span class="sxs-lookup"><span data-stu-id="59f86-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="59f86-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="59f86-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="59f86-126">Ausgeschlossene Linux-Paket Masken.</span><span class="sxs-lookup"><span data-stu-id="59f86-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="59f86-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="59f86-127">-IncludedKbNumber</span></span>
<span data-ttu-id="59f86-128">KB-Nummern der enthaltenen Updates.</span><span class="sxs-lookup"><span data-stu-id="59f86-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="59f86-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="59f86-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="59f86-130">Eingeschlossene Linux-Paket Klassifizierungen.</span><span class="sxs-lookup"><span data-stu-id="59f86-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="59f86-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="59f86-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="59f86-132">Enthaltene Linux-Paket Masken.</span><span class="sxs-lookup"><span data-stu-id="59f86-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="59f86-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="59f86-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="59f86-134">Windows Update-Klassifikationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="59f86-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="59f86-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="59f86-135">-Linux</span></span>
<span data-ttu-id="59f86-136">Gibt an, dass die Software Update-Konfiguration auf Linux-Betriebssystem Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="59f86-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="59f86-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="59f86-137">-NonAzureComputer</span></span>
<span data-ttu-id="59f86-138">Nicht Azure-Computernamen.</span><span class="sxs-lookup"><span data-stu-id="59f86-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="59f86-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f86-139">-ResourceGroupName</span></span>
<span data-ttu-id="59f86-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59f86-140">The resource group name.</span></span>

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

### <span data-ttu-id="59f86-141">-Terminplan</span><span class="sxs-lookup"><span data-stu-id="59f86-141">-Schedule</span></span>
<span data-ttu-id="59f86-142">Schedule-Objekt, das für die Software Update Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="59f86-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="59f86-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="59f86-143">-Windows</span></span>
<span data-ttu-id="59f86-144">Gibt an, dass die Software Update-Konfiguration auf Windows-Betriebssystem Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="59f86-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="59f86-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59f86-145">-Confirm</span></span>
<span data-ttu-id="59f86-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59f86-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f86-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f86-147">-WhatIf</span></span>
<span data-ttu-id="59f86-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59f86-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f86-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59f86-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f86-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f86-150">CommonParameters</span></span>
<span data-ttu-id="59f86-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59f86-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f86-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f86-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f86-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59f86-153">INPUTS</span></span>

### <span data-ttu-id="59f86-154">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="59f86-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="59f86-155">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="59f86-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="59f86-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="59f86-156">System.String[]</span></span>

### <span data-ttu-id="59f86-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="59f86-157">System.TimeSpan</span></span>

### <span data-ttu-id="59f86-158">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="59f86-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="59f86-159">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="59f86-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="59f86-160">System. String</span><span class="sxs-lookup"><span data-stu-id="59f86-160">System.String</span></span>

## <span data-ttu-id="59f86-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59f86-161">OUTPUTS</span></span>

### <span data-ttu-id="59f86-162">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="59f86-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="59f86-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="59f86-163">NOTES</span></span>

## <span data-ttu-id="59f86-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59f86-164">RELATED LINKS</span></span>
