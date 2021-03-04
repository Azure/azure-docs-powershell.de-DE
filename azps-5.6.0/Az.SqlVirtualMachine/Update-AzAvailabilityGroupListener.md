---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/update-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Update-AzAvailabilityGroupListener.md
ms.openlocfilehash: c94f1e842697a64dd95f7d5ccb90e389484a61e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926240"
---
# <span data-ttu-id="25665-101">Update-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="25665-101">Update-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="25665-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25665-102">SYNOPSIS</span></span>
<span data-ttu-id="25665-103">Aktualisiert den Listener der Verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="25665-103">Updates the Availability Group Listener.</span></span>

## <span data-ttu-id="25665-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25665-104">SYNTAX</span></span>

### <span data-ttu-id="25665-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="25665-105">Name (Default)</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25665-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="25665-106">InputObject</span></span>
```
Update-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel>
 [-SqlVirtualMachineId <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25665-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="25665-107">ResourceId</span></span>
```
Update-AzAvailabilityGroupListener [-ResourceId] <String> [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25665-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="25665-108">SqlVmGroupObject</span></span>
```
Update-AzAvailabilityGroupListener [-SqlVirtualMachineId <String[]>] [-AsJob]
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25665-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25665-109">DESCRIPTION</span></span>
<span data-ttu-id="25665-110">Das Update-AzAvailabilityGroupListener cmdlet aktualisiert einen Availability Group Listener.</span><span class="sxs-lookup"><span data-stu-id="25665-110">The Update-AzAvailabilityGroupListener cmdlet updates an Availability Group Listener.</span></span>

## <span data-ttu-id="25665-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25665-111">EXAMPLES</span></span>

### <span data-ttu-id="25665-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25665-112">Example 1</span></span>
```powershell
PS C:\> Update-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01 -SqlVirtualMachineId $VmResourceId01,$VmResourceId02
```

<span data-ttu-id="25665-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="25665-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="25665-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="25665-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="25665-115">Aktualisiert die Liste SQL virtuellen Computer für den Listener der Verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="25665-115">Updates the list SQL Virtual Machines for the Availability Group Listener.</span></span>

## <span data-ttu-id="25665-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="25665-116">PARAMETERS</span></span>

### <span data-ttu-id="25665-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25665-117">-AsJob</span></span>
<span data-ttu-id="25665-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="25665-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="25665-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25665-119">-DefaultProfile</span></span>
<span data-ttu-id="25665-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25665-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25665-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25665-121">-InputObject</span></span>
<span data-ttu-id="25665-122">Availability Group Listener-Objekt.</span><span class="sxs-lookup"><span data-stu-id="25665-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="25665-123">-Name</span><span class="sxs-lookup"><span data-stu-id="25665-123">-Name</span></span>
<span data-ttu-id="25665-124">Name des Verfügbarkeitsgruppenlisteners.</span><span class="sxs-lookup"><span data-stu-id="25665-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="25665-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25665-125">-ResourceGroupName</span></span>
<span data-ttu-id="25665-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25665-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="25665-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25665-127">-ResourceId</span></span>
<span data-ttu-id="25665-128">Availability Group Listener Resource Id</span><span class="sxs-lookup"><span data-stu-id="25665-128">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="25665-129">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="25665-129">-SqlVirtualMachineId</span></span>
<span data-ttu-id="25665-130">Liste der Sql VM-Ressourcen-IDs</span><span class="sxs-lookup"><span data-stu-id="25665-130">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="25665-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="25665-131">-SqlVMGroupName</span></span>
<span data-ttu-id="25665-132">SQL namen der Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="25665-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="25665-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="25665-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="25665-134">SQL virtuellen Computer-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="25665-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="25665-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25665-135">-Confirm</span></span>
<span data-ttu-id="25665-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25665-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25665-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25665-137">-WhatIf</span></span>
<span data-ttu-id="25665-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25665-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25665-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25665-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25665-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25665-140">CommonParameters</span></span>
<span data-ttu-id="25665-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25665-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25665-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25665-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25665-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25665-143">INPUTS</span></span>

### <span data-ttu-id="25665-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="25665-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="25665-145">System.String</span><span class="sxs-lookup"><span data-stu-id="25665-145">System.String</span></span>

### <span data-ttu-id="25665-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="25665-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="25665-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25665-147">OUTPUTS</span></span>

### <span data-ttu-id="25665-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="25665-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="25665-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="25665-149">NOTES</span></span>

## <span data-ttu-id="25665-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="25665-150">RELATED LINKS</span></span>
