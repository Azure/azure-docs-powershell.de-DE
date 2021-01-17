---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471338"
---
# <span data-ttu-id="f373a-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="f373a-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="f373a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f373a-102">SYNOPSIS</span></span>
<span data-ttu-id="f373a-103">Ruft eine Liste der ausgeführten Azure-Automatisierungssoftwareupdates ab.</span><span class="sxs-lookup"><span data-stu-id="f373a-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="f373a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f373a-104">SYNTAX</span></span>

### <span data-ttu-id="f373a-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="f373a-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f373a-106">ById</span><span class="sxs-lookup"><span data-stu-id="f373a-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f373a-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="f373a-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f373a-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="f373a-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f373a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f373a-109">DESCRIPTION</span></span>
<span data-ttu-id="f373a-110">Das Get-AzAutomationSoftwareUpdateRun-Cmdlet gibt eine Liste der ausgeführten Softwareupdates zurück.</span><span class="sxs-lookup"><span data-stu-id="f373a-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="f373a-111">Da einer Softwareupdatekonfiguration ein Zeitplan zugeordnet ist, kann sie mehrmals ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f373a-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="f373a-112">Jedes Mal, wenn ein Zeitplan ausgelöst wird, wird ein Update ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f373a-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="f373a-113">Die Aktualisierungs ausführung ist ein Aggregat des Ergebnisses aller Computerläufe.</span><span class="sxs-lookup"><span data-stu-id="f373a-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="f373a-114">Sie können für eine bestimmte Softwareupdatekonfiguration ausgeführt werden, indem Sie den Parameter "SoftwareUpdateConfigurationName" übergeben.</span><span class="sxs-lookup"><span data-stu-id="f373a-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="f373a-115">Um bestimmte Ausgeführte zu erhalten, müssen Sie den Namensparameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="f373a-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="f373a-116">Sie können auch Eine Liste mit einem bestimmten Status, für bestimmte Betriebssysteme ausgeführt oder nach einem bestimmten Zeitpunkt gestartet werden, indem Sie den entsprechenden Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="f373a-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="f373a-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f373a-117">EXAMPLES</span></span>

### <span data-ttu-id="f373a-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f373a-118">Example 1</span></span>
<span data-ttu-id="f373a-119">In diesem Beispiel werden alle Updates aufgeführt, die von einer bestimmten Softwareupdatekonfiguration ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="f373a-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="f373a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f373a-120">PARAMETERS</span></span>

### <span data-ttu-id="f373a-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f373a-121">-AutomationAccountName</span></span>
<span data-ttu-id="f373a-122">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="f373a-122">The automation account name.</span></span>

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

### <span data-ttu-id="f373a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f373a-123">-DefaultProfile</span></span>
<span data-ttu-id="f373a-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f373a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f373a-125">-ID</span><span class="sxs-lookup"><span data-stu-id="f373a-125">-Id</span></span>
<span data-ttu-id="f373a-126">ID der ausgeführten Softwareupdatekonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f373a-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f373a-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f373a-127">-OperatingSystem</span></span>
<span data-ttu-id="f373a-128">Das Betriebssystem der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="f373a-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f373a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f373a-129">-ResourceGroupName</span></span>
<span data-ttu-id="f373a-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f373a-130">The resource group name.</span></span>

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

### <span data-ttu-id="f373a-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f373a-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="f373a-132">Die Softwareupdatekonfiguration hat die Ausführung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f373a-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f373a-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f373a-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="f373a-134">Der Name der Softwareupdatekonfiguration hat die Ausführung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f373a-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f373a-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f373a-135">-StartTime</span></span>
<span data-ttu-id="f373a-136">Mindeststartzeit der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="f373a-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f373a-137">-Status</span><span class="sxs-lookup"><span data-stu-id="f373a-137">-Status</span></span>
<span data-ttu-id="f373a-138">Status der Ausführung.</span><span class="sxs-lookup"><span data-stu-id="f373a-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f373a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f373a-139">CommonParameters</span></span>
<span data-ttu-id="f373a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f373a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f373a-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f373a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f373a-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f373a-142">INPUTS</span></span>

### <span data-ttu-id="f373a-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f373a-143">System.Guid</span></span>

### <span data-ttu-id="f373a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f373a-144">System.String</span></span>

### <span data-ttu-id="f373a-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f373a-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="f373a-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f373a-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f373a-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f373a-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f373a-148">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f373a-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="f373a-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f373a-149">OUTPUTS</span></span>

### <span data-ttu-id="f373a-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="f373a-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="f373a-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f373a-151">NOTES</span></span>

## <span data-ttu-id="f373a-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f373a-152">RELATED LINKS</span></span>
