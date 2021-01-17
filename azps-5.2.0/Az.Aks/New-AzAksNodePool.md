---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360855"
---
# <span data-ttu-id="331a9-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="331a9-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="331a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="331a9-102">SYNOPSIS</span></span>
<span data-ttu-id="331a9-103">Erstellen Sie einen neuen Knotenpool in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="331a9-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="331a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="331a9-104">SYNTAX</span></span>

### <span data-ttu-id="331a9-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="331a9-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="331a9-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="331a9-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="331a9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="331a9-107">DESCRIPTION</span></span>
<span data-ttu-id="331a9-108">Erstellen Sie einen neuen Knotenpool in einem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="331a9-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="331a9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="331a9-109">EXAMPLES</span></span>

### <span data-ttu-id="331a9-110">Erstellen eines Knotenpools mit Standardparametern</span><span class="sxs-lookup"><span data-stu-id="331a9-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="331a9-111">Erstellen des Windows Server-Containers auf einem AKS</span><span class="sxs-lookup"><span data-stu-id="331a9-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="331a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="331a9-112">PARAMETERS</span></span>

### <span data-ttu-id="331a9-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="331a9-113">-ClusterName</span></span>
<span data-ttu-id="331a9-114">Der Name der verwalteten Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="331a9-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="331a9-115">-ClusterObject</span></span>
<span data-ttu-id="331a9-116">Geben Sie das Clusterobjekt an, in dem ein Knotenpool erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="331a9-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-117">-Count</span><span class="sxs-lookup"><span data-stu-id="331a9-117">-Count</span></span>
<span data-ttu-id="331a9-118">Die Standardanzahl von Knoten für die Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="331a9-118">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331a9-119">-DefaultProfile</span></span>
<span data-ttu-id="331a9-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="331a9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="331a9-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="331a9-121">-EnableAutoScaling</span></span>
<span data-ttu-id="331a9-122">Aktivieren der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="331a9-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="331a9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="331a9-123">-Force</span></span>
<span data-ttu-id="331a9-124">Erstellen eines Knotenpools auch dann, wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="331a9-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="331a9-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="331a9-125">-KubernetesVersion</span></span>
<span data-ttu-id="331a9-126">Die Version von Kubernetes, die zum Erstellen des Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="331a9-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="331a9-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="331a9-127">-MaxCount</span></span>
<span data-ttu-id="331a9-128">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="331a9-128">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="331a9-129">-MaxPodCount</span></span>
<span data-ttu-id="331a9-130">Maximale Anzahl von Pods, die auf Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="331a9-130">Maximum number of pods that can run on node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="331a9-131">-MinCount</span></span>
<span data-ttu-id="331a9-132">Mindestanzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="331a9-132">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-133">-Name</span><span class="sxs-lookup"><span data-stu-id="331a9-133">-Name</span></span>
<span data-ttu-id="331a9-134">Der Name des Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="331a9-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="331a9-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="331a9-135">-OsDiskSize</span></span>
<span data-ttu-id="331a9-136">Die Standardanzahl von Knoten für die Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="331a9-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="331a9-137">-OsType</span></span>
<span data-ttu-id="331a9-138">OsType, der zum Angeben des Betriebssystemtyps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="331a9-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="331a9-139">Wählen Sie unter Linux und Windows aus.</span><span class="sxs-lookup"><span data-stu-id="331a9-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="331a9-140">Standard für Linux.</span><span class="sxs-lookup"><span data-stu-id="331a9-140">Default to Linux.</span></span>

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

### <span data-ttu-id="331a9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331a9-141">-ResourceGroupName</span></span>
<span data-ttu-id="331a9-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="331a9-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="331a9-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="331a9-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="331a9-144">ScaleSetEvictionPolicy zum Angeben einer Entfernungsrichtlinie für den Skalierungssatz für virtuelle Computer mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="331a9-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="331a9-145">Standardmäßig "Löschen".</span><span class="sxs-lookup"><span data-stu-id="331a9-145">Default to Delete.</span></span>

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

### <span data-ttu-id="331a9-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="331a9-146">-ScaleSetPriority</span></span>
<span data-ttu-id="331a9-147">ScaleSetPriority zur Angabe der Priorität für den Skalierungssatz des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="331a9-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="331a9-148">Standardmäßig auf "Normal" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="331a9-148">Default to regular.</span></span>

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

### <span data-ttu-id="331a9-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="331a9-149">-VmSetType</span></span>
<span data-ttu-id="331a9-150">Stellt Die Typen eines Knotenpools dar.</span><span class="sxs-lookup"><span data-stu-id="331a9-150">Represents types of an node pool.</span></span>
<span data-ttu-id="331a9-151">Mögliche Werte sind: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="331a9-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="331a9-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="331a9-152">-VmSize</span></span>
<span data-ttu-id="331a9-153">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="331a9-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="331a9-154">Der Standardwert ist Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="331a9-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="331a9-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="331a9-155">-VnetSubnetID</span></span>
<span data-ttu-id="331a9-156">VNet SubnetID gibt den Subnetzbezeichner des VNet an.</span><span class="sxs-lookup"><span data-stu-id="331a9-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="331a9-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="331a9-157">-Confirm</span></span>
<span data-ttu-id="331a9-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="331a9-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="331a9-159">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="331a9-159">-WhatIf</span></span>
<span data-ttu-id="331a9-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="331a9-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="331a9-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="331a9-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="331a9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331a9-162">CommonParameters</span></span>
<span data-ttu-id="331a9-163">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331a9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331a9-164">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="331a9-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331a9-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="331a9-165">INPUTS</span></span>

### <span data-ttu-id="331a9-166">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="331a9-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="331a9-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="331a9-167">OUTPUTS</span></span>

### <span data-ttu-id="331a9-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="331a9-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="331a9-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="331a9-169">NOTES</span></span>

## <span data-ttu-id="331a9-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="331a9-170">RELATED LINKS</span></span>
