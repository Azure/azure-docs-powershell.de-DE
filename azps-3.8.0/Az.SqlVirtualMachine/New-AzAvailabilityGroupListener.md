---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzAvailabilityGroupListener.md
ms.openlocfilehash: af36c7cae36cb3d6bdb9bf2760b9a8299463e877
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846471"
---
# <span data-ttu-id="d46a2-101">New-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="d46a2-101">New-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="d46a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d46a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d46a2-103">Erstellt einen neuen Verfügbarkeitsgruppen-Listener.</span><span class="sxs-lookup"><span data-stu-id="d46a2-103">Creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="d46a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d46a2-104">SYNTAX</span></span>

### <span data-ttu-id="d46a2-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="d46a2-105">Name (Default)</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]> [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d46a2-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="d46a2-106">SqlVmGroupObject</span></span>
```
New-AzAvailabilityGroupListener -AvailabilityGroupName <String> [-Port <Int32>]
 -LoadBalancerResourceId <String> [-IpAddress <String>] [-SubnetId <String>] -ProbePort <Int32>
 [-PublicIpAddressResourceId <String>] [-AsJob] -SqlVirtualMachineId <String[]>
 [-SqlVMGroupObject] <AzureSqlVMGroupModel> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46a2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d46a2-107">DESCRIPTION</span></span>
<span data-ttu-id="d46a2-108">Das New-AzAvailabilityGroupListener-Cmdlet erstellt einen neuen Verfügbarkeitsgruppen-Listener.</span><span class="sxs-lookup"><span data-stu-id="d46a2-108">The New-AzAvailabilityGroupListener cmdlet creates a new Availability Group Listener.</span></span>

## <span data-ttu-id="d46a2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d46a2-109">EXAMPLES</span></span>

### <span data-ttu-id="d46a2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d46a2-110">Example 1</span></span>
```powershell
PS C:\> New-AzAvailabilityGroupListener -AvailabilityGroupName AvailabilityGroup01 -LoadBalancerResourceId $LoadBalanceResourceId -SubnetId $SubnetId -ProbePort 59999 -SqlVirtualMachineId $VmResourceId1,$VmResourceId2 -Name AgListener01  -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -IpAddress 10.0.0.3
```

<span data-ttu-id="d46a2-111">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d46a2-111">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="d46a2-112">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="d46a2-112">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="d46a2-113">Erstellt einen neuen Verfügbarkeitsgruppen-Listener-AgListener01 für die AvailabilityGroup01 der verfügbarkeitsgruppe in der Gruppe SqlVmGroup01 der SQL-virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="d46a2-113">Creates a new Availability Group Listener AgListener01 for the Availability Group AvailabilityGroup01 in SQL Virtual Machine Group SqlVmGroup01.</span></span>

## <span data-ttu-id="d46a2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d46a2-114">PARAMETERS</span></span>

### <span data-ttu-id="d46a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d46a2-115">-AsJob</span></span>
<span data-ttu-id="d46a2-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="d46a2-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d46a2-117">-AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="d46a2-117">-AvailabilityGroupName</span></span>
<span data-ttu-id="d46a2-118">Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d46a2-118">Availability Group name.</span></span>

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

### <span data-ttu-id="d46a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46a2-119">-DefaultProfile</span></span>
<span data-ttu-id="d46a2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d46a2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d46a2-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="d46a2-121">-IpAddress</span></span>
<span data-ttu-id="d46a2-122">Private IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="d46a2-122">Private Ip Address</span></span>

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

### <span data-ttu-id="d46a2-123">-LoadBalancerResourceId</span><span class="sxs-lookup"><span data-stu-id="d46a2-123">-LoadBalancerResourceId</span></span>
<span data-ttu-id="d46a2-124">Load Balancer-ID</span><span class="sxs-lookup"><span data-stu-id="d46a2-124">Load Balancer Id</span></span>

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

### <span data-ttu-id="d46a2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d46a2-125">-Name</span></span>
<span data-ttu-id="d46a2-126">Listener-Name der verfügbarkeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d46a2-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="d46a2-127">-Port</span><span class="sxs-lookup"><span data-stu-id="d46a2-127">-Port</span></span>
<span data-ttu-id="d46a2-128">Port Nummer des AG-Listener.</span><span class="sxs-lookup"><span data-stu-id="d46a2-128">Port number of AG Listener.</span></span> <span data-ttu-id="d46a2-129">Der Standardwert ist 1433.</span><span class="sxs-lookup"><span data-stu-id="d46a2-129">Default Value is 1433.</span></span>

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

### <span data-ttu-id="d46a2-130">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="d46a2-130">-ProbePort</span></span>
<span data-ttu-id="d46a2-131">Prüfpunkt-Port</span><span class="sxs-lookup"><span data-stu-id="d46a2-131">Probe Port</span></span>

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

### <span data-ttu-id="d46a2-132">-PublicIpAddressResourceId</span><span class="sxs-lookup"><span data-stu-id="d46a2-132">-PublicIpAddressResourceId</span></span>
<span data-ttu-id="d46a2-133">Ressourcen-ID der öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="d46a2-133">Public Ip Address Resource Id</span></span>

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

### <span data-ttu-id="d46a2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46a2-134">-ResourceGroupName</span></span>
<span data-ttu-id="d46a2-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d46a2-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="d46a2-136">-SqlVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d46a2-136">-SqlVirtualMachineId</span></span>
<span data-ttu-id="d46a2-137">Liste der SQL VM-Ressourcen-IDs</span><span class="sxs-lookup"><span data-stu-id="d46a2-137">List of Sql VM Resource IDs</span></span>

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

### <span data-ttu-id="d46a2-138">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="d46a2-138">-SqlVMGroupName</span></span>
<span data-ttu-id="d46a2-139">Gruppenname der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="d46a2-139">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="d46a2-140">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="d46a2-140">-SqlVMGroupObject</span></span>
<span data-ttu-id="d46a2-141">Gruppenobjekt der virtuellen SQL-Maschine</span><span class="sxs-lookup"><span data-stu-id="d46a2-141">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="d46a2-142">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="d46a2-142">-SubnetId</span></span>
<span data-ttu-id="d46a2-143">Subnet-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d46a2-143">Subnet Resource Id</span></span>

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

### <span data-ttu-id="d46a2-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d46a2-144">-Confirm</span></span>
<span data-ttu-id="d46a2-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d46a2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46a2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46a2-146">-WhatIf</span></span>
<span data-ttu-id="d46a2-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d46a2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46a2-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d46a2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46a2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46a2-149">CommonParameters</span></span>
<span data-ttu-id="d46a2-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46a2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46a2-151">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d46a2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46a2-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d46a2-152">INPUTS</span></span>

### <span data-ttu-id="d46a2-153">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="d46a2-153">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="d46a2-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d46a2-154">OUTPUTS</span></span>

### <span data-ttu-id="d46a2-155">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="d46a2-155">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="d46a2-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="d46a2-156">NOTES</span></span>

## <span data-ttu-id="d46a2-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d46a2-157">RELATED LINKS</span></span>
