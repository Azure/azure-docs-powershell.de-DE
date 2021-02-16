---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150476"
---
# <span data-ttu-id="b7cea-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="b7cea-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="b7cea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7cea-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cea-103">Löscht einen Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="b7cea-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="b7cea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7cea-104">SYNTAX</span></span>

### <span data-ttu-id="b7cea-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7cea-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7cea-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7cea-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7cea-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7cea-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7cea-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="b7cea-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7cea-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7cea-109">DESCRIPTION</span></span>
<span data-ttu-id="b7cea-110">Das Remove-AzAvailabilityGroupListener cmdlet löscht einen Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="b7cea-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="b7cea-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7cea-111">EXAMPLES</span></span>

### <span data-ttu-id="b7cea-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7cea-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="b7cea-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cea-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="b7cea-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="b7cea-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="b7cea-115">Löscht den Availability Group Listener AgListener01 in der Availability Group AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="b7cea-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="b7cea-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7cea-116">PARAMETERS</span></span>

### <span data-ttu-id="b7cea-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7cea-117">-AsJob</span></span>
<span data-ttu-id="b7cea-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="b7cea-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b7cea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cea-119">-DefaultProfile</span></span>
<span data-ttu-id="b7cea-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7cea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7cea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7cea-121">-InputObject</span></span>
<span data-ttu-id="b7cea-122">Verfügbarkeitsgruppenlistenerobjekt.</span><span class="sxs-lookup"><span data-stu-id="b7cea-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="b7cea-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b7cea-123">-Name</span></span>
<span data-ttu-id="b7cea-124">Name des Listeners der Verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b7cea-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="b7cea-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7cea-125">-PassThru</span></span>
<span data-ttu-id="b7cea-126">Gibt an, ob die gelöschte Ressource am Ende der Ausführung des Cmdlets ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7cea-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="b7cea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cea-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7cea-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b7cea-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7cea-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7cea-129">-ResourceId</span></span>
<span data-ttu-id="b7cea-130">Ressourcen-ID des Verfügbarkeitsgruppenlisteners</span><span class="sxs-lookup"><span data-stu-id="b7cea-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="b7cea-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cea-131">-SqlVMGroupName</span></span>
<span data-ttu-id="b7cea-132">SQL gruppenname des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b7cea-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="b7cea-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="b7cea-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="b7cea-134">SQL virtuellen Computer-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="b7cea-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="b7cea-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7cea-135">-Confirm</span></span>
<span data-ttu-id="b7cea-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7cea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7cea-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b7cea-137">-WhatIf</span></span>
<span data-ttu-id="b7cea-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7cea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7cea-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7cea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7cea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cea-140">CommonParameters</span></span>
<span data-ttu-id="b7cea-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cea-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7cea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cea-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7cea-143">INPUTS</span></span>

### <span data-ttu-id="b7cea-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="b7cea-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="b7cea-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b7cea-145">System.String</span></span>

### <span data-ttu-id="b7cea-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="b7cea-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="b7cea-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7cea-147">OUTPUTS</span></span>

### <span data-ttu-id="b7cea-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="b7cea-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="b7cea-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b7cea-149">NOTES</span></span>

## <span data-ttu-id="b7cea-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b7cea-150">RELATED LINKS</span></span>
