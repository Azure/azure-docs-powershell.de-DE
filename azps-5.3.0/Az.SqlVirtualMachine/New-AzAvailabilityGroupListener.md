---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470325"
---
# <span data-ttu-id="a3910-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="a3910-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="a3910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3910-102">SYNOPSIS</span></span>
<span data-ttu-id="a3910-103">Erstellt einen neuen Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="a3910-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="a3910-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3910-104">SYNTAX</span></span>

### <span data-ttu-id="a3910-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3910-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3910-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="a3910-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3910-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3910-107">DESCRIPTION</span></span>
<span data-ttu-id="a3910-108">Das New-AzAvailabilityGroupListener erstellt einen neuen Verfügbarkeitsgruppenlistener.</span><span class="sxs-lookup"><span data-stu-id="a3910-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="a3910-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3910-109">EXAMPLES</span></span>

### <span data-ttu-id="a3910-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3910-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="a3910-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a3910-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a3910-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a3910-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="a3910-113">Erstellt einen neuen Verfügbarkeitsgruppenlistener01 für die Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span><span class="sxs-lookup"><span data-stu-id="a3910-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="a3910-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3910-114">PARAMETERS</span></span>

### <span data-ttu-id="a3910-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3910-115">-AsJob</span></span>
<span data-ttu-id="a3910-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="a3910-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a3910-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a3910-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="a3910-118">Name der Verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a3910-118">Availability Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3910-119">-DefaultProfile</span></span>
<span data-ttu-id="a3910-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3910-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3910-121">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a3910-121">-IpAddress</span></span>
<span data-ttu-id="a3910-122">Private Ip Address</span><span class="sxs-lookup"><span data-stu-id="a3910-122">Private Ip Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="a3910-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="a3910-124">Load Balancer-ID</span><span class="sxs-lookup"><span data-stu-id="a3910-124">Load Balancer Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a3910-125">-Name</span></span>
<span data-ttu-id="a3910-126">Name des Listeners der Verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a3910-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-127">-Port</span><span class="sxs-lookup"><span data-stu-id="a3910-127">-Port</span></span>
<span data-ttu-id="a3910-128">Portnummer des AG-Listeners.</span><span class="sxs-lookup"><span data-stu-id="a3910-128">Port number of AG Listener.</span></span> <span data-ttu-id="a3910-129">Der Standardwert ist 1433.</span><span class="sxs-lookup"><span data-stu-id="a3910-129">Default Value is 1433.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="a3910-130">-ProbePort</span></span>
<span data-ttu-id="a3910-131">Probeport</span><span class="sxs-lookup"><span data-stu-id="a3910-131">Probe Port</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="a3910-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="a3910-133">Ressourcen-ID der öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="a3910-133">Public Ip Address Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3910-134">-ResourceGroupName</span></span>
<span data-ttu-id="a3910-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3910-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3910-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a3910-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="a3910-137">Liste der Sql VM-Ressourcen-IDs</span><span class="sxs-lookup"><span data-stu-id="a3910-137">List of Sql VM Resource IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="a3910-138">-SqlVMGroupName</span></span>
<span data-ttu-id="a3910-139">SQL gruppenname des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="a3910-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="a3910-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="a3910-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="a3910-141">SQL virtuellen Computer-Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="a3910-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="a3910-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a3910-142">-SubnetId</span></span>
<span data-ttu-id="a3910-143">Subnetzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a3910-143">Subnet Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3910-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3910-144">-Confirm</span></span>
<span data-ttu-id="a3910-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3910-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3910-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3910-146">-WhatIf</span></span>
<span data-ttu-id="a3910-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3910-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3910-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3910-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3910-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3910-149">CommonParameters</span></span>
<span data-ttu-id="a3910-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3910-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3910-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3910-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3910-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3910-152">INPUTS</span></span>

### <span data-ttu-id="a3910-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="a3910-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="a3910-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3910-154">OUTPUTS</span></span>

### <span data-ttu-id="a3910-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="a3910-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="a3910-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3910-156">NOTES</span></span>

## <span data-ttu-id="a3910-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3910-157">RELATED LINKS</span></span>
