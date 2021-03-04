---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: 56891d1dae20f89289b9c2f72bf87bfeed7bd347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931640"
---
# <span data-ttu-id="54f3d-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="54f3d-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="54f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="54f3d-103">Löscht einen Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="54f3d-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="54f3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54f3d-104">SYNTAX</span></span>

### <span data-ttu-id="54f3d-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="54f3d-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54f3d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="54f3d-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f3d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="54f3d-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f3d-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="54f3d-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54f3d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54f3d-109">DESCRIPTION</span></span>
<span data-ttu-id="54f3d-110">Das Remove-AzAvailabilityGroupListener cmdlet löscht einen Availability Group Listener.</span><span class="sxs-lookup"><span data-stu-id="54f3d-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="54f3d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54f3d-111">EXAMPLES</span></span>

### <span data-ttu-id="54f3d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54f3d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="54f3d-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="54f3d-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="54f3d-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="54f3d-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="54f3d-115">Löscht die Availability Group Listener AgListener01 in der Availability Group AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="54f3d-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="54f3d-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54f3d-116">PARAMETERS</span></span>

### <span data-ttu-id="54f3d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54f3d-117">-AsJob</span></span>
<span data-ttu-id="54f3d-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="54f3d-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="54f3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f3d-119">-DefaultProfile</span></span>
<span data-ttu-id="54f3d-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54f3d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54f3d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54f3d-121">-InputObject</span></span>
<span data-ttu-id="54f3d-122">Availability Group Listener-Objekt.</span><span class="sxs-lookup"><span data-stu-id="54f3d-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="54f3d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="54f3d-123">-Name</span></span>
<span data-ttu-id="54f3d-124">Name des Verfügbarkeitsgruppenlisteners.</span><span class="sxs-lookup"><span data-stu-id="54f3d-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="54f3d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54f3d-125">-PassThru</span></span>
<span data-ttu-id="54f3d-126">Gibt an, ob die gelöschte Ressource am Ende der Cmdletausführung ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="54f3d-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="54f3d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f3d-127">-ResourceGroupName</span></span>
<span data-ttu-id="54f3d-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54f3d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="54f3d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54f3d-129">-ResourceId</span></span>
<span data-ttu-id="54f3d-130">Availability Group Listener Resource Id</span><span class="sxs-lookup"><span data-stu-id="54f3d-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f3d-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="54f3d-131">-SqlVMGroupName</span></span>
<span data-ttu-id="54f3d-132">SQL namen der Gruppe virtueller Computer.</span><span class="sxs-lookup"><span data-stu-id="54f3d-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="54f3d-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="54f3d-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="54f3d-134">SQL virtuellen Computer-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="54f3d-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="54f3d-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54f3d-135">-Confirm</span></span>
<span data-ttu-id="54f3d-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54f3d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f3d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f3d-137">-WhatIf</span></span>
<span data-ttu-id="54f3d-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54f3d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54f3d-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54f3d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f3d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f3d-140">CommonParameters</span></span>
<span data-ttu-id="54f3d-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f3d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f3d-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54f3d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f3d-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54f3d-143">INPUTS</span></span>

### <span data-ttu-id="54f3d-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="54f3d-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="54f3d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="54f3d-145">System.String</span></span>

### <span data-ttu-id="54f3d-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="54f3d-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="54f3d-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54f3d-147">OUTPUTS</span></span>

### <span data-ttu-id="54f3d-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="54f3d-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="54f3d-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54f3d-149">NOTES</span></span>

## <span data-ttu-id="54f3d-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54f3d-150">RELATED LINKS</span></span>
