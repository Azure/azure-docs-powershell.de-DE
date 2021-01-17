---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370795"
---
# <span data-ttu-id="114a3-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="114a3-101">New-AzAksCluster</span></span>

## <span data-ttu-id="114a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="114a3-102">SYNOPSIS</span></span>
<span data-ttu-id="114a3-103">Erstellen Sie einen neuen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="114a3-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="114a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="114a3-104">SYNTAX</span></span>

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

## <span data-ttu-id="114a3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="114a3-105">DESCRIPTION</span></span>

<span data-ttu-id="114a3-106">Erstellen Sie einen neuen Azure Kubernetes Service (AKS)-Cluster.</span><span class="sxs-lookup"><span data-stu-id="114a3-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="114a3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="114a3-107">EXAMPLES</span></span>

### <span data-ttu-id="114a3-108">Neuer AKS mit Standard-Parametern.</span><span class="sxs-lookup"><span data-stu-id="114a3-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="114a3-109">Erstellen Sie den Windows Server-Container auf einem AKS.</span><span class="sxs-lookup"><span data-stu-id="114a3-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="114a3-110">Zum Erstellen des Windows Server-Containers auf einem AKS müssen Sie beim Erstellen der AKS mindestens vier folgende Parameter und den Wert für bzw. den Wert `NetworkPlugin` `NodeVmSetType` `azure` `VirtualMachineScaleSets` angeben.</span><span class="sxs-lookup"><span data-stu-id="114a3-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="114a3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="114a3-111">PARAMETERS</span></span>

### <span data-ttu-id="114a3-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="114a3-112">-AcrNameToAttach</span></span>
<span data-ttu-id="114a3-113">Gewähren der Rolle "acrpull" des angegebenen ACR an den AKS-Dienstprinzipal, z. B. myacr</span><span class="sxs-lookup"><span data-stu-id="114a3-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="114a3-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="114a3-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="114a3-115">Add-On-Namen, die beim Erstellen des Cluster aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="114a3-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="114a3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="114a3-116">-AsJob</span></span>
<span data-ttu-id="114a3-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="114a3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="114a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114a3-118">-DefaultProfile</span></span>
<span data-ttu-id="114a3-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="114a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="114a3-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="114a3-120">-DnsNamePrefix</span></span>
<span data-ttu-id="114a3-121">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="114a3-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="114a3-122">Die Länge muss <= 9 sein, wenn Benutzer den Container "Windows" hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="114a3-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="114a3-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="114a3-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="114a3-124">Aktivieren der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="114a3-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="114a3-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="114a3-125">-EnableRbac</span></span>
<span data-ttu-id="114a3-126">Aktivieren von Kubernetes Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="114a3-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="114a3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="114a3-127">-Force</span></span>
<span data-ttu-id="114a3-128">Cluster erstellen, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="114a3-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="114a3-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="114a3-129">-GenerateSshKey</span></span>
<span data-ttu-id="114a3-130">Generieren Sie eine ssh-Schlüsseldatei für {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="114a3-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="114a3-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="114a3-131">-KubernetesVersion</span></span>
<span data-ttu-id="114a3-132">Die Version von Kubernetes, die zum Erstellen des Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="114a3-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="114a3-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="114a3-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="114a3-134">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="114a3-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="114a3-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="114a3-135">-LoadBalancerSku</span></span>
<span data-ttu-id="114a3-136">Die SKU für den Lastenausgleich für den verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="114a3-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="114a3-137">-Location</span><span class="sxs-lookup"><span data-stu-id="114a3-137">-Location</span></span>
<span data-ttu-id="114a3-138">Azure-Standort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="114a3-138">Azure location for the cluster.</span></span>
<span data-ttu-id="114a3-139">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="114a3-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="114a3-140">-Name</span><span class="sxs-lookup"><span data-stu-id="114a3-140">-Name</span></span>
<span data-ttu-id="114a3-141">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="114a3-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="114a3-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="114a3-142">-NetworkPlugin</span></span>
<span data-ttu-id="114a3-143">Netzwerk-Plug-In, das zum Erstellen eines Kubernetes-Netzwerks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="114a3-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="114a3-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="114a3-144">-NodeCount</span></span>
<span data-ttu-id="114a3-145">Die Standardanzahl von Knoten für die Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="114a3-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="114a3-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="114a3-146">-NodeMaxCount</span></span>
<span data-ttu-id="114a3-147">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="114a3-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="114a3-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="114a3-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="114a3-149">Maximale Anzahl von Pods, die auf knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="114a3-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="114a3-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="114a3-150">-NodeMinCount</span></span>
<span data-ttu-id="114a3-151">Mindestanzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="114a3-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="114a3-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="114a3-152">-NodeName</span></span>
<span data-ttu-id="114a3-153">Eindeutiger Name des Agentpoolprofils im Kontext des Abonnements und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="114a3-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="114a3-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="114a3-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="114a3-155">Größe in GB des Betriebssystemdatenträgers für jeden Knoten im Knotenpool.</span><span class="sxs-lookup"><span data-stu-id="114a3-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="114a3-156">Mindestens 30 GB.</span><span class="sxs-lookup"><span data-stu-id="114a3-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="114a3-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="114a3-157">-NodePoolMode</span></span>
<span data-ttu-id="114a3-158">NodePoolMode stellt den Modus eines Knotenpools dar.</span><span class="sxs-lookup"><span data-stu-id="114a3-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="114a3-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="114a3-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="114a3-160">ScaleSetEvictionPolicy zum Angeben einer Entfernungsrichtlinie für den Skalierungssatz für virtuelle Computer mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="114a3-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="114a3-161">Standardmäßig "Löschen".</span><span class="sxs-lookup"><span data-stu-id="114a3-161">Default to Delete.</span></span>

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

### <span data-ttu-id="114a3-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="114a3-162">-NodeSetPriority</span></span>
<span data-ttu-id="114a3-163">ScaleSetPriority zum Angeben der Priorität des Skalierungsskalens für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="114a3-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="114a3-164">Standardmäßig auf "Normal" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="114a3-164">Default to regular.</span></span>

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

### <span data-ttu-id="114a3-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="114a3-165">-NodeVmSetType</span></span>
<span data-ttu-id="114a3-166">AgentPoolType stellt Typen eines Agentpools dar.</span><span class="sxs-lookup"><span data-stu-id="114a3-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="114a3-167">Mögliche Werte sind: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="114a3-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="114a3-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="114a3-168">-NodeVmSize</span></span>
<span data-ttu-id="114a3-169">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="114a3-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="114a3-170">Der Standardwert ist Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="114a3-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="114a3-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="114a3-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="114a3-172">VNet SubnetID gibt den Subnetzbezeichner des VNet an.</span><span class="sxs-lookup"><span data-stu-id="114a3-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="114a3-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="114a3-173">-ResourceGroupName</span></span>
<span data-ttu-id="114a3-174">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="114a3-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="114a3-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="114a3-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="114a3-176">Die Client-ID und der geheime Clientgeheimnis, die der Anwendung bzw. dem Dienstprinzipal von AAD zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="114a3-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="114a3-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="114a3-177">-SshKeyValue</span></span>
<span data-ttu-id="114a3-178">Wert der SSH-Schlüsseldatei oder Schlüsseldateipfad.</span><span class="sxs-lookup"><span data-stu-id="114a3-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="114a3-179">Der Standardwert ist {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="114a3-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="114a3-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="114a3-180">-SubnetName</span></span>
<span data-ttu-id="114a3-181">Subnetzname des VirtualNode-Add-Ons.</span><span class="sxs-lookup"><span data-stu-id="114a3-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="114a3-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="114a3-182">-Tag</span></span>
<span data-ttu-id="114a3-183">Auf die Ressource anzuwendende Tags</span><span class="sxs-lookup"><span data-stu-id="114a3-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="114a3-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="114a3-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="114a3-185">Der Administratorbenutzername, der für Windows-VMs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="114a3-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="114a3-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="114a3-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="114a3-187">Das Administratorkennwort, das für Windows-VMs verwendet werden soll, muss mindestens 12 Lang sein und mindestens ein Kleinzeichen enthalten, d. h. ein Sonderzeichen und ein `[a-z]` `[A-Z]` `[!@#$%^&_()]` Sonderzeichen.</span><span class="sxs-lookup"><span data-stu-id="114a3-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="114a3-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="114a3-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="114a3-189">Ressourcen-ID des Arbeitsbereichs des Überwachungs-Add-Ons.</span><span class="sxs-lookup"><span data-stu-id="114a3-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="114a3-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="114a3-190">-Confirm</span></span>
<span data-ttu-id="114a3-191">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="114a3-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="114a3-192">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="114a3-192">-WhatIf</span></span>
<span data-ttu-id="114a3-193">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="114a3-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="114a3-194">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="114a3-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="114a3-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114a3-195">CommonParameters</span></span>
<span data-ttu-id="114a3-196">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114a3-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114a3-197">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="114a3-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114a3-198">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="114a3-198">INPUTS</span></span>

### <span data-ttu-id="114a3-199">Keine</span><span class="sxs-lookup"><span data-stu-id="114a3-199">None</span></span>

## <span data-ttu-id="114a3-200">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="114a3-200">OUTPUTS</span></span>

### <span data-ttu-id="114a3-201">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="114a3-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="114a3-202">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="114a3-202">NOTES</span></span>

## <span data-ttu-id="114a3-203">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="114a3-203">RELATED LINKS</span></span>
