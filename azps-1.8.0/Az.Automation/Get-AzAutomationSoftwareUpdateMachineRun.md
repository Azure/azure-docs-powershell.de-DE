---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 80bba3309c0c23862fdb5efbbe6f373b8d1a964a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661802"
---
# <span data-ttu-id="75d19-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="75d19-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="75d19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75d19-102">SYNOPSIS</span></span>
<span data-ttu-id="75d19-103">Ruft eine Liste der Azure Automation Software Update-Konfigurations Maschine wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75d19-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="75d19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75d19-104">SYNTAX</span></span>

### <span data-ttu-id="75d19-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="75d19-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75d19-106">ById</span><span class="sxs-lookup"><span data-stu-id="75d19-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d19-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="75d19-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d19-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="75d19-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d19-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75d19-109">DESCRIPTION</span></span>
<span data-ttu-id="75d19-110">Dieses Cmdlet gibt eine Liste der Computer Läufe zurück.</span><span class="sxs-lookup"><span data-stu-id="75d19-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="75d19-111">Bei jedem Software Update-Testlauf wird für jeden der Software Update-Konfigurations Zielcomputer ein Computer Lauf ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="75d19-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="75d19-112">Wenn Sie einen bestimmten Computer ausführen möchten, übergeben Sie den ID-Parameter.</span><span class="sxs-lookup"><span data-stu-id="75d19-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="75d19-113">Sie können alle Maschinen Läufe auflisten, alle Läufe für einen bestimmten Computer, alle werden mit einem bestimmten Status ausgeführt, indem Sie die entsprechenden Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="75d19-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="75d19-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75d19-114">EXAMPLES</span></span>

### <span data-ttu-id="75d19-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75d19-115">Example 1</span></span>
<span data-ttu-id="75d19-116">In diesem Beispiel werden alle fehlerhaften Computer Läufe für den angegebenen Azure Virtual Machine zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75d19-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


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

## <span data-ttu-id="75d19-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="75d19-117">PARAMETERS</span></span>

### <span data-ttu-id="75d19-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="75d19-118">-AutomationAccountName</span></span>
<span data-ttu-id="75d19-119">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="75d19-119">The automation account name.</span></span>

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

### <span data-ttu-id="75d19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d19-120">-DefaultProfile</span></span>
<span data-ttu-id="75d19-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75d19-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d19-122">-ID</span><span class="sxs-lookup"><span data-stu-id="75d19-122">-Id</span></span>
<span data-ttu-id="75d19-123">Die ID des ausgeführten Software Update Computers.</span><span class="sxs-lookup"><span data-stu-id="75d19-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="75d19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d19-124">-ResourceGroupName</span></span>
<span data-ttu-id="75d19-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75d19-125">The resource group name.</span></span>

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

### <span data-ttu-id="75d19-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="75d19-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="75d19-127">Das Software Update wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75d19-127">The software update run.</span></span>

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

### <span data-ttu-id="75d19-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="75d19-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="75d19-129">Die ID des ausgeführten Softwareupdates.</span><span class="sxs-lookup"><span data-stu-id="75d19-129">Id of the software update run.</span></span>

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

### <span data-ttu-id="75d19-130">-Status</span><span class="sxs-lookup"><span data-stu-id="75d19-130">-Status</span></span>
<span data-ttu-id="75d19-131">Der Status des Computer Laufs.</span><span class="sxs-lookup"><span data-stu-id="75d19-131">Status of the machine run.</span></span>

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

### <span data-ttu-id="75d19-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="75d19-132">-TargetComputer</span></span>
<span data-ttu-id="75d19-133">Zielcomputer für den Computerbetrieb.</span><span class="sxs-lookup"><span data-stu-id="75d19-133">target computer for the machine run.</span></span>
<span data-ttu-id="75d19-134">Kann entweder ein nicht-AZ-Computername oder eine Azure VM-Ressourcen-ID sein.</span><span class="sxs-lookup"><span data-stu-id="75d19-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

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

### <span data-ttu-id="75d19-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d19-135">CommonParameters</span></span>
<span data-ttu-id="75d19-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d19-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d19-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d19-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d19-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75d19-138">INPUTS</span></span>

### <span data-ttu-id="75d19-139">System. GUID</span><span class="sxs-lookup"><span data-stu-id="75d19-139">System.Guid</span></span>

### <span data-ttu-id="75d19-140">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="75d19-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="75d19-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRunStatus, Microsoft. Azure. PowerShell. Cmdlets. Automation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="75d19-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="75d19-142">System. String</span><span class="sxs-lookup"><span data-stu-id="75d19-142">System.String</span></span>

## <span data-ttu-id="75d19-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75d19-143">OUTPUTS</span></span>

### <span data-ttu-id="75d19-144">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="75d19-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="75d19-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="75d19-145">NOTES</span></span>

## <span data-ttu-id="75d19-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75d19-146">RELATED LINKS</span></span>
