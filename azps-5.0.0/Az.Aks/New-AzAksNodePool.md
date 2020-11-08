---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177318"
---
# <span data-ttu-id="4f8aa-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="4f8aa-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="4f8aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8aa-103">Erstellen eines neuen Knoten Pools in einem bestimmten Cluster</span><span class="sxs-lookup"><span data-stu-id="4f8aa-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="4f8aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f8aa-104">SYNTAX</span></span>

### <span data-ttu-id="4f8aa-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f8aa-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8aa-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f8aa-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f8aa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f8aa-107">DESCRIPTION</span></span>
<span data-ttu-id="4f8aa-108">Erstellen eines neuen Knoten Pools in einem bestimmten Cluster</span><span class="sxs-lookup"><span data-stu-id="4f8aa-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="4f8aa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f8aa-109">EXAMPLES</span></span>

### <span data-ttu-id="4f8aa-110">Erstellen eines Knoten Pools mit Standardparametern</span><span class="sxs-lookup"><span data-stu-id="4f8aa-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="4f8aa-111">Erstellen eines Windows Server-Containers auf einem AKS</span><span class="sxs-lookup"><span data-stu-id="4f8aa-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="4f8aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f8aa-112">PARAMETERS</span></span>

### <span data-ttu-id="4f8aa-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4f8aa-113">-ClusterName</span></span>
<span data-ttu-id="4f8aa-114">Der Name der verwalteten Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="4f8aa-115">-Clusterobject</span><span class="sxs-lookup"><span data-stu-id="4f8aa-115">-ClusterObject</span></span>
<span data-ttu-id="4f8aa-116">Geben Sie das Clusterobjekt an, in dem der Knoten Pool erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="4f8aa-117">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="4f8aa-117">-Count</span></span>
<span data-ttu-id="4f8aa-118">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="4f8aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8aa-119">-DefaultProfile</span></span>
<span data-ttu-id="4f8aa-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f8aa-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="4f8aa-121">-EnableAutoScaling</span></span>
<span data-ttu-id="4f8aa-122">Ob die automatische Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="4f8aa-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="4f8aa-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4f8aa-123">-Force</span></span>
<span data-ttu-id="4f8aa-124">Erstellen eines Knoten Pools, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="4f8aa-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="4f8aa-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="4f8aa-125">-KubernetesVersion</span></span>
<span data-ttu-id="4f8aa-126">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="4f8aa-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4f8aa-127">-MaxCount</span></span>
<span data-ttu-id="4f8aa-128">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="4f8aa-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="4f8aa-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="4f8aa-129">-MaxPodCount</span></span>
<span data-ttu-id="4f8aa-130">Die maximale Anzahl von Hülsen, die auf dem Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="4f8aa-131">-"Mincount</span><span class="sxs-lookup"><span data-stu-id="4f8aa-131">-MinCount</span></span>
<span data-ttu-id="4f8aa-132">Minimale Anzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="4f8aa-133">-Name</span><span class="sxs-lookup"><span data-stu-id="4f8aa-133">-Name</span></span>
<span data-ttu-id="4f8aa-134">Der Name des Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="4f8aa-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="4f8aa-135">-OsDiskSize</span></span>
<span data-ttu-id="4f8aa-136">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="4f8aa-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="4f8aa-137">-OsType</span></span>
<span data-ttu-id="4f8aa-138">OsType, der zum Angeben des Betriebssystemtyps verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="4f8aa-139">Wählen Sie unter Linux und Windows aus.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="4f8aa-140">Standardmäßig für Linux.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-140">Default to Linux.</span></span>

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

### <span data-ttu-id="4f8aa-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8aa-141">-ResourceGroupName</span></span>
<span data-ttu-id="4f8aa-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="4f8aa-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f8aa-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="4f8aa-144">ScaleSetEvictionPolicy, das zum Angeben von Räumungs Richtlinien für den Skalierungs Satz der virtuellen Maschine mit niedriger Priorität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="4f8aa-145">Standard zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-145">Default to Delete.</span></span>

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

### <span data-ttu-id="4f8aa-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="4f8aa-146">-ScaleSetPriority</span></span>
<span data-ttu-id="4f8aa-147">ScaleSetPriority, das zum Angeben der Skalierungs Priorität für den virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="4f8aa-148">Standardmäßig auf normal.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-148">Default to regular.</span></span>

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

### <span data-ttu-id="4f8aa-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="4f8aa-149">-VmSetType</span></span>
<span data-ttu-id="4f8aa-150">Stellt Typen eines Knoten Pools dar.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-150">Represents types of an node pool.</span></span>
<span data-ttu-id="4f8aa-151">Mögliche Werte sind: ' VirtualMachineScaleSets ', ' availabilityset '</span><span class="sxs-lookup"><span data-stu-id="4f8aa-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="4f8aa-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="4f8aa-152">-VmSize</span></span>
<span data-ttu-id="4f8aa-153">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="4f8aa-154">Der Standardwert ist Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="4f8aa-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="4f8aa-155">-VnetSubnetID</span></span>
<span data-ttu-id="4f8aa-156">VNet Subnet-ID gibt den Subnetzmasken des VNet an.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="4f8aa-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f8aa-157">-Confirm</span></span>
<span data-ttu-id="4f8aa-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8aa-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f8aa-159">-WhatIf</span></span>
<span data-ttu-id="4f8aa-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f8aa-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8aa-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8aa-162">CommonParameters</span></span>
<span data-ttu-id="4f8aa-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8aa-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f8aa-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8aa-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f8aa-165">INPUTS</span></span>

### <span data-ttu-id="4f8aa-166">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="4f8aa-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="4f8aa-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f8aa-167">OUTPUTS</span></span>

### <span data-ttu-id="4f8aa-168">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="4f8aa-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="4f8aa-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f8aa-169">NOTES</span></span>

## <span data-ttu-id="4f8aa-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f8aa-170">RELATED LINKS</span></span>
