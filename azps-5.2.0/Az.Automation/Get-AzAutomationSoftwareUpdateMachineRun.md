---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373720"
---
# <span data-ttu-id="b2ea5-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="b2ea5-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="b2ea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ea5-103">Ruft eine Liste des ausgeführten Konfigurationscomputers für die Softwareupdatekonfiguration für die Azure-Automatisierungssoftware ab.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="b2ea5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2ea5-104">SYNTAX</span></span>

### <span data-ttu-id="b2ea5-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2ea5-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2ea5-106">ById</span><span class="sxs-lookup"><span data-stu-id="b2ea5-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ea5-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="b2ea5-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ea5-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="b2ea5-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2ea5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2ea5-109">DESCRIPTION</span></span>
<span data-ttu-id="b2ea5-110">Dieses Cmdlet gibt eine Liste der ausgeführten Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="b2ea5-111">Jede Ausführung eines Softwareupdates löst eine Ausführung eines Computers für jeden Zielcomputer für die Softwareupdatekonfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="b2ea5-112">Übergeben Sie zum Ausführen eines bestimmten Computers den Id-Parameter.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="b2ea5-113">Sie können alle Ausgeführten des Computers auflisten, alle werden für einen bestimmten Computer ausgeführt, alle werden mit einem bestimmten Status ausgeführt, indem sie die entsprechenden Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="b2ea5-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2ea5-114">EXAMPLES</span></span>

### <span data-ttu-id="b2ea5-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2ea5-115">Example 1</span></span>
<span data-ttu-id="b2ea5-116">Dieses Beispiel gibt alle fehlgeschlagenen Computer zurück, die für den angegebenen virtuellen Azure-Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="b2ea5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2ea5-117">PARAMETERS</span></span>

### <span data-ttu-id="b2ea5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2ea5-118">-AutomationAccountName</span></span>
<span data-ttu-id="b2ea5-119">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-119">The automation account name.</span></span>

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

### <span data-ttu-id="b2ea5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ea5-120">-DefaultProfile</span></span>
<span data-ttu-id="b2ea5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2ea5-122">-ID</span><span class="sxs-lookup"><span data-stu-id="b2ea5-122">-Id</span></span>
<span data-ttu-id="b2ea5-123">ID des ausgeführten Softwareupdatecomputers.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="b2ea5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ea5-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2ea5-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-125">The resource group name.</span></span>

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

### <span data-ttu-id="b2ea5-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="b2ea5-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="b2ea5-127">Das Softwareupdate wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ea5-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="b2ea5-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="b2ea5-129">ID des ausgeführten Softwareupdates.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ea5-130">-Status</span><span class="sxs-lookup"><span data-stu-id="b2ea5-130">-Status</span></span>
<span data-ttu-id="b2ea5-131">Status des ausgeführten Computers.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ea5-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="b2ea5-132">-TargetComputer</span></span>
<span data-ttu-id="b2ea5-133">zielcomputer für den ausgeführten Computer.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-133">target computer for the machine run.</span></span>
<span data-ttu-id="b2ea5-134">Kann entweder ein Nicht-Computername oder eine Azure VM-Ressourcen-ID sein.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2ea5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ea5-135">CommonParameters</span></span>
<span data-ttu-id="b2ea5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2ea5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ea5-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ea5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ea5-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2ea5-138">INPUTS</span></span>

### <span data-ttu-id="b2ea5-139">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b2ea5-139">System.Guid</span></span>

### <span data-ttu-id="b2ea5-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="b2ea5-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="b2ea5-141">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b2ea5-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b2ea5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b2ea5-142">System.String</span></span>

## <span data-ttu-id="b2ea5-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2ea5-143">OUTPUTS</span></span>

### <span data-ttu-id="b2ea5-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="b2ea5-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="b2ea5-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2ea5-145">NOTES</span></span>

## <span data-ttu-id="b2ea5-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2ea5-146">RELATED LINKS</span></span>
