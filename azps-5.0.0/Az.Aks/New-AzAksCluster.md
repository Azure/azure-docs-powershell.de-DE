---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177317"
---
# <span data-ttu-id="b80d9-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="b80d9-101">New-AzAksCluster</span></span>

## <span data-ttu-id="b80d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b80d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b80d9-103">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="b80d9-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="b80d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b80d9-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b80d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b80d9-105">DESCRIPTION</span></span>

<span data-ttu-id="b80d9-106">Erstellen Sie einen neuen Azure Kubernetes Service (AKS)-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b80d9-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="b80d9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b80d9-107">EXAMPLES</span></span>

### <span data-ttu-id="b80d9-108">Neues a AKS mit Standard params.</span><span class="sxs-lookup"><span data-stu-id="b80d9-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="b80d9-109">Erstellen eines Windows Server-Containers auf einem AKS</span><span class="sxs-lookup"><span data-stu-id="b80d9-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="b80d9-110">Zum Erstellen eines Windows Server-Containers für eine AKS müssen Sie beim Erstellen der AKS mindestens vier folgende Parameter angeben und den Wert für `NetworkPlugin` und `NodeVmSetType` muss und müssen sein `azure` `VirtualMachineScaleSets` .</span><span class="sxs-lookup"><span data-stu-id="b80d9-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="b80d9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b80d9-111">PARAMETERS</span></span>

### <span data-ttu-id="b80d9-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="b80d9-112">-AcrNameToAttach</span></span>
<span data-ttu-id="b80d9-113">Erteilen der Rolle "acrpull" des angegebenen ACR an AKS-Dienstprinzipal, beispielsweise myacr</span><span class="sxs-lookup"><span data-stu-id="b80d9-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="b80d9-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="b80d9-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="b80d9-115">Add-on-Namen müssen aktiviert werden, wenn Cluster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b80d9-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="b80d9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b80d9-116">-AsJob</span></span>
<span data-ttu-id="b80d9-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b80d9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b80d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80d9-118">-DefaultProfile</span></span>
<span data-ttu-id="b80d9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b80d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b80d9-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="b80d9-120">-DnsNamePrefix</span></span>
<span data-ttu-id="b80d9-121">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="b80d9-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="b80d9-122">Die Länge muss <= 9 sein, wenn Benutzer den Windows-Container hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="b80d9-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="b80d9-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="b80d9-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="b80d9-124">Ob die automatische Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="b80d9-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="b80d9-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="b80d9-125">-EnableRbac</span></span>
<span data-ttu-id="b80d9-126">Ob Kubernetes Role-Based Access aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="b80d9-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="b80d9-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b80d9-127">-Force</span></span>
<span data-ttu-id="b80d9-128">Erstellen eines Clusters, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="b80d9-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="b80d9-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="b80d9-129">-GenerateSshKey</span></span>
<span data-ttu-id="b80d9-130">Generieren Sie eine SSH-Schlüsseldatei in {Home}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="b80d9-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="b80d9-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="b80d9-131">-KubernetesVersion</span></span>
<span data-ttu-id="b80d9-132">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b80d9-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="b80d9-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="b80d9-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="b80d9-134">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="b80d9-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="b80d9-135">-LoadBalancerSku</span></span>
<span data-ttu-id="b80d9-136">Die SKU des Lastenausgleichs für den verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="b80d9-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="b80d9-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="b80d9-137">-Location</span></span>
<span data-ttu-id="b80d9-138">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="b80d9-138">Azure location for the cluster.</span></span>
<span data-ttu-id="b80d9-139">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="b80d9-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="b80d9-140">-Name</span><span class="sxs-lookup"><span data-stu-id="b80d9-140">-Name</span></span>
<span data-ttu-id="b80d9-141">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="b80d9-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="b80d9-142">-NetworkPlugin</span></span>
<span data-ttu-id="b80d9-143">Netzwerk-Plugin zum Erstellen von Kubernetes-Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="b80d9-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b80d9-144">-NodeCount</span></span>
<span data-ttu-id="b80d9-145">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="b80d9-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="b80d9-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="b80d9-146">-NodeMaxCount</span></span>
<span data-ttu-id="b80d9-147">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="b80d9-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="b80d9-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="b80d9-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="b80d9-149">Die maximale Anzahl von Hülsen, die auf dem Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b80d9-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="b80d9-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="b80d9-150">-NodeMinCount</span></span>
<span data-ttu-id="b80d9-151">Minimale Anzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="b80d9-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="b80d9-152">-Nodename</span><span class="sxs-lookup"><span data-stu-id="b80d9-152">-NodeName</span></span>
<span data-ttu-id="b80d9-153">Eindeutiger Name des Agenten Pool Profils im Kontext der Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b80d9-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="b80d9-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="b80d9-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="b80d9-155">Die Größe der Betriebssystem Diskette für jeden Knoten im Knoten Pool in GB.</span><span class="sxs-lookup"><span data-stu-id="b80d9-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="b80d9-156">Mind. 30 GB.</span><span class="sxs-lookup"><span data-stu-id="b80d9-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="b80d9-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="b80d9-157">-NodePoolMode</span></span>
<span data-ttu-id="b80d9-158">NodePoolMode stellt den Modus eines Knoten Pools dar.</span><span class="sxs-lookup"><span data-stu-id="b80d9-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="b80d9-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b80d9-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="b80d9-160">ScaleSetEvictionPolicy, das zum Angeben von Räumungs Richtlinien für den Skalierungs Satz der virtuellen Maschine mit niedriger Priorität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b80d9-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="b80d9-161">Standard zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="b80d9-161">Default to Delete.</span></span>

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

### <span data-ttu-id="b80d9-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="b80d9-162">-NodeSetPriority</span></span>
<span data-ttu-id="b80d9-163">ScaleSetPriority, das zum Angeben der Skalierungs Priorität für den virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b80d9-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="b80d9-164">Standardmäßig auf normal.</span><span class="sxs-lookup"><span data-stu-id="b80d9-164">Default to regular.</span></span>

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

### <span data-ttu-id="b80d9-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="b80d9-165">-NodeVmSetType</span></span>
<span data-ttu-id="b80d9-166">AgentPoolType stellt Typen eines Agenten Pools dar.</span><span class="sxs-lookup"><span data-stu-id="b80d9-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="b80d9-167">Mögliche Werte sind: ' VirtualMachineScaleSets ', ' availabilityset '</span><span class="sxs-lookup"><span data-stu-id="b80d9-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="b80d9-168">-NodeVmSize</span></span>
<span data-ttu-id="b80d9-169">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b80d9-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="b80d9-170">Der Standardwert ist Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="b80d9-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="b80d9-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="b80d9-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="b80d9-172">VNet Subnet-ID gibt den Subnetzmasken des VNet an.</span><span class="sxs-lookup"><span data-stu-id="b80d9-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="b80d9-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80d9-173">-ResourceGroupName</span></span>
<span data-ttu-id="b80d9-174">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b80d9-174">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="b80d9-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="b80d9-176">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b80d9-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="b80d9-177">-SshKeyValue</span></span>
<span data-ttu-id="b80d9-178">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="b80d9-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="b80d9-179">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="b80d9-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b80d9-180">-SubnetName</span></span>
<span data-ttu-id="b80d9-181">Subnet-Name des VirtualNode-addons.</span><span class="sxs-lookup"><span data-stu-id="b80d9-181">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="b80d9-182">-Tag</span></span>
<span data-ttu-id="b80d9-183">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="b80d9-183">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="b80d9-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="b80d9-185">Der für Windows-VMS zu verwendende Administrator-Benutzername.</span><span class="sxs-lookup"><span data-stu-id="b80d9-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="b80d9-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="b80d9-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="b80d9-187">Das für Windows-VMS zu verwendende Administratorkennwort, dessen Länge mindestens 12 sein muss, mit mindestens einem Kleinbuchstaben, also `[a-z]` einem `[A-Z]` und einem Sonderzeichen `[!@#$%^&_()]` .</span><span class="sxs-lookup"><span data-stu-id="b80d9-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b80d9-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="b80d9-189">Ressourcen-ID des Arbeitsbereichs des Überwachungs-addons.</span><span class="sxs-lookup"><span data-stu-id="b80d9-189">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b80d9-190">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b80d9-190">-Confirm</span></span>
<span data-ttu-id="b80d9-191">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b80d9-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b80d9-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b80d9-192">-WhatIf</span></span>
<span data-ttu-id="b80d9-193">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b80d9-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b80d9-194">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b80d9-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b80d9-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80d9-195">CommonParameters</span></span>
<span data-ttu-id="b80d9-196">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b80d9-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80d9-197">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b80d9-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80d9-198">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b80d9-198">INPUTS</span></span>

### <span data-ttu-id="b80d9-199">Keine</span><span class="sxs-lookup"><span data-stu-id="b80d9-199">None</span></span>

## <span data-ttu-id="b80d9-200">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b80d9-200">OUTPUTS</span></span>

### <span data-ttu-id="b80d9-201">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b80d9-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b80d9-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="b80d9-202">NOTES</span></span>

## <span data-ttu-id="b80d9-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b80d9-203">RELATED LINKS</span></span>
