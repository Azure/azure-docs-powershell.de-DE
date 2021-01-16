---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: 6c44a2fc7193acaadcf24ac311b5eb4b4a00b7d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470309"
---
# <span data-ttu-id="f4be1-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="f4be1-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="f4be1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4be1-102">SYNOPSIS</span></span>
<span data-ttu-id="f4be1-103">Aktualisiert den Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="f4be1-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="f4be1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4be1-104">SYNTAX</span></span>

### <span data-ttu-id="f4be1-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4be1-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4be1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4be1-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4be1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4be1-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4be1-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="f4be1-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4be1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4be1-109">DESCRIPTION</span></span>
<span data-ttu-id="f4be1-110">Das Update-AzAvailabilityGroupListener aktualisiert einen Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="f4be1-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="f4be1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4be1-111">EXAMPLES</span></span>

### <span data-ttu-id="f4be1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4be1-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="f4be1-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="f4be1-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="f4be1-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="f4be1-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="f4be1-115">Aktualisiert die Liste SQL virtuellen Computern für den Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="f4be1-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="f4be1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4be1-116">PARAMETERS</span></span>

### <span data-ttu-id="f4be1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4be1-117">-AsJob</span></span>
<span data-ttu-id="f4be1-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="f4be1-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f4be1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4be1-119">-DefaultProfile</span></span>
<span data-ttu-id="f4be1-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4be1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4be1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4be1-121">-InputObject</span></span>
<span data-ttu-id="f4be1-122">Verfügbarkeitsgruppenlistenerobjekt.</span><span class="sxs-lookup"><span data-stu-id="f4be1-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4be1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f4be1-123">-Name</span></span>
<span data-ttu-id="f4be1-124">Name des Listeners der Verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f4be1-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4be1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4be1-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4be1-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4be1-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4be1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4be1-127">-ResourceId</span></span>
<span data-ttu-id="f4be1-128">Ressourcen-ID des Verfügbarkeitsgruppenlisteners</span><span class="sxs-lookup"><span data-stu-id="f4be1-128">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: AvailabilityGroupListenerId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4be1-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f4be1-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="f4be1-130">Liste der Sql VM-Ressourcen-IDs</span><span class="sxs-lookup"><span data-stu-id="f4be1-130">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4be1-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="f4be1-131">-SqlVMGroupName</span></span>
<span data-ttu-id="f4be1-132">SQL gruppenname des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f4be1-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4be1-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="f4be1-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="f4be1-134">SQL virtuellen Computer-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="f4be1-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4be1-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4be1-135">-Confirm</span></span>
<span data-ttu-id="f4be1-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4be1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4be1-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f4be1-137">-WhatIf</span></span>
<span data-ttu-id="f4be1-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4be1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4be1-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4be1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4be1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4be1-140">CommonParameters</span></span>
<span data-ttu-id="f4be1-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4be1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4be1-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4be1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4be1-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4be1-143">INPUTS</span></span>

### <span data-ttu-id="f4be1-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f4be1-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="f4be1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f4be1-145">System.String</span></span>

### <span data-ttu-id="f4be1-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="f4be1-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="f4be1-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4be1-147">OUTPUTS</span></span>

### <span data-ttu-id="f4be1-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="f4be1-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="f4be1-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f4be1-149">NOTES</span></span>

## <span data-ttu-id="f4be1-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f4be1-150">RELATED LINKS</span></span>
