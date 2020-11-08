---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: f7a3479fb7fd70c47d5d4d3b80004cb25d9baa0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165397"
---
# <span data-ttu-id="69a8e-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="69a8e-101">New-AzAksCluster</span></span>

## <span data-ttu-id="69a8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="69a8e-103">Erstellen eines neuen verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="69a8e-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="69a8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69a8e-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeOsType <String>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
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

## <span data-ttu-id="69a8e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69a8e-105">DESCRIPTION</span></span>

<span data-ttu-id="69a8e-106">Erstellen Sie einen neuen Azure Kubernetes Service (AKS)-Cluster.</span><span class="sxs-lookup"><span data-stu-id="69a8e-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="69a8e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69a8e-107">EXAMPLES</span></span>

### <span data-ttu-id="69a8e-108">Neues a AKS mit Standard params.</span><span class="sxs-lookup"><span data-stu-id="69a8e-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="69a8e-109">Erstellen eines Windows Server-Containers auf einem AKS</span><span class="sxs-lookup"><span data-stu-id="69a8e-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="69a8e-110">Zum Erstellen eines Windows Server-Containers für eine AKS müssen Sie beim Erstellen der AKS mindestens vier folgende Parameter angeben und den Wert für `NetworkPlugin` und `NodeVmSetType` muss und müssen sein `azure` `VirtualMachineScaleSets` .</span><span class="sxs-lookup"><span data-stu-id="69a8e-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="69a8e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="69a8e-111">PARAMETERS</span></span>

### <span data-ttu-id="69a8e-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="69a8e-112">-AcrNameToAttach</span></span>
<span data-ttu-id="69a8e-113">Erteilen der Rolle "acrpull" des angegebenen ACR an AKS-Dienstprinzipal, beispielsweise myacr</span><span class="sxs-lookup"><span data-stu-id="69a8e-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="69a8e-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="69a8e-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="69a8e-115">Add-on-Namen müssen aktiviert werden, wenn Cluster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="69a8e-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="69a8e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69a8e-116">-AsJob</span></span>
<span data-ttu-id="69a8e-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="69a8e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69a8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a8e-118">-DefaultProfile</span></span>
<span data-ttu-id="69a8e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69a8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69a8e-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="69a8e-120">-DnsNamePrefix</span></span>
<span data-ttu-id="69a8e-121">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="69a8e-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="69a8e-122">Die Länge muss <= 9 sein, wenn Benutzer den Windows-Container hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="69a8e-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="69a8e-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="69a8e-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="69a8e-124">Ob die automatische Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="69a8e-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="69a8e-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="69a8e-125">-EnableRbac</span></span>
<span data-ttu-id="69a8e-126">Ob Kubernetes Role-Based Access aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="69a8e-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="69a8e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="69a8e-127">-Force</span></span>
<span data-ttu-id="69a8e-128">Erstellen eines Clusters, auch wenn er bereits vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="69a8e-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="69a8e-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="69a8e-129">-GenerateSshKey</span></span>
<span data-ttu-id="69a8e-130">Generieren Sie eine SSH-Schlüsseldatei in {Home}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="69a8e-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="69a8e-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="69a8e-131">-KubernetesVersion</span></span>
<span data-ttu-id="69a8e-132">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69a8e-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="69a8e-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="69a8e-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="69a8e-134">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="69a8e-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="69a8e-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="69a8e-135">-LoadBalancerSku</span></span>
<span data-ttu-id="69a8e-136">Die SKU des Lastenausgleichs für den verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="69a8e-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="69a8e-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="69a8e-137">-Location</span></span>
<span data-ttu-id="69a8e-138">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="69a8e-138">Azure location for the cluster.</span></span>
<span data-ttu-id="69a8e-139">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="69a8e-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="69a8e-140">-Name</span><span class="sxs-lookup"><span data-stu-id="69a8e-140">-Name</span></span>
<span data-ttu-id="69a8e-141">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="69a8e-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="69a8e-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="69a8e-142">-NetworkPlugin</span></span>
<span data-ttu-id="69a8e-143">Netzwerk-Plugin zum Erstellen von Kubernetes-Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="69a8e-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="69a8e-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="69a8e-144">-NodeCount</span></span>
<span data-ttu-id="69a8e-145">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="69a8e-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="69a8e-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="69a8e-146">-NodeMaxCount</span></span>
<span data-ttu-id="69a8e-147">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="69a8e-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="69a8e-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="69a8e-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="69a8e-149">Die maximale Anzahl von Hülsen, die auf dem Knoten ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="69a8e-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="69a8e-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="69a8e-150">-NodeMinCount</span></span>
<span data-ttu-id="69a8e-151">Minimale Anzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="69a8e-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="69a8e-152">-Nodename</span><span class="sxs-lookup"><span data-stu-id="69a8e-152">-NodeName</span></span>
<span data-ttu-id="69a8e-153">Eindeutiger Name des Agenten Pool Profils im Kontext der Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69a8e-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="69a8e-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="69a8e-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="69a8e-155">Die Größe der Betriebssystem Diskette für jeden Knoten im Knoten Pool in GB.</span><span class="sxs-lookup"><span data-stu-id="69a8e-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="69a8e-156">Mind. 30 GB.</span><span class="sxs-lookup"><span data-stu-id="69a8e-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="69a8e-157">-NodeOsType</span><span class="sxs-lookup"><span data-stu-id="69a8e-157">-NodeOsType</span></span>
<span data-ttu-id="69a8e-158">OsType, der zum Angeben des Betriebssystemtyps verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69a8e-158">OsType to be used to specify os type.</span></span> <span data-ttu-id="69a8e-159">Wählen Sie unter Linux und Windows aus.</span><span class="sxs-lookup"><span data-stu-id="69a8e-159">Choose from Linux and Windows.</span></span> <span data-ttu-id="69a8e-160">Standardmäßig für Linux.</span><span class="sxs-lookup"><span data-stu-id="69a8e-160">Default to Linux.</span></span>

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

### <span data-ttu-id="69a8e-161">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="69a8e-161">-NodePoolMode</span></span>
<span data-ttu-id="69a8e-162">NodePoolMode stellt den Modus eines Knoten Pools dar.</span><span class="sxs-lookup"><span data-stu-id="69a8e-162">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="69a8e-163">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="69a8e-163">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="69a8e-164">ScaleSetEvictionPolicy, das zum Angeben von Räumungs Richtlinien für den Skalierungs Satz der virtuellen Maschine mit niedriger Priorität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69a8e-164">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="69a8e-165">Standard zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="69a8e-165">Default to Delete.</span></span>

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

### <span data-ttu-id="69a8e-166">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="69a8e-166">-NodeSetPriority</span></span>
<span data-ttu-id="69a8e-167">ScaleSetPriority, das zum Angeben der Skalierungs Priorität für den virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69a8e-167">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="69a8e-168">Standardmäßig auf normal.</span><span class="sxs-lookup"><span data-stu-id="69a8e-168">Default to regular.</span></span>

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

### <span data-ttu-id="69a8e-169">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="69a8e-169">-NodeVmSetType</span></span>
<span data-ttu-id="69a8e-170">AgentPoolType stellt Typen eines Agenten Pools dar.</span><span class="sxs-lookup"><span data-stu-id="69a8e-170">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="69a8e-171">Mögliche Werte sind: ' VirtualMachineScaleSets ', ' availabilityset '</span><span class="sxs-lookup"><span data-stu-id="69a8e-171">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="69a8e-172">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="69a8e-172">-NodeVmSize</span></span>
<span data-ttu-id="69a8e-173">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="69a8e-173">The size of the Virtual Machine.</span></span> <span data-ttu-id="69a8e-174">Der Standardwert ist Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="69a8e-174">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="69a8e-175">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="69a8e-175">-NodeVnetSubnetID</span></span>
<span data-ttu-id="69a8e-176">VNet Subnet-ID gibt den Subnetzmasken des VNet an.</span><span class="sxs-lookup"><span data-stu-id="69a8e-176">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="69a8e-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69a8e-177">-ResourceGroupName</span></span>
<span data-ttu-id="69a8e-178">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69a8e-178">Resource Group Name.</span></span>

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

### <span data-ttu-id="69a8e-179">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="69a8e-179">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="69a8e-180">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="69a8e-180">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69a8e-181">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="69a8e-181">-SshKeyValue</span></span>
<span data-ttu-id="69a8e-182">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="69a8e-182">SSH key file value or key file path.</span></span>
<span data-ttu-id="69a8e-183">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="69a8e-183">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="69a8e-184">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="69a8e-184">-SubnetName</span></span>
<span data-ttu-id="69a8e-185">Subnet-Name des VirtualNode-addons.</span><span class="sxs-lookup"><span data-stu-id="69a8e-185">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="69a8e-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="69a8e-186">-Tag</span></span>
<span data-ttu-id="69a8e-187">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="69a8e-187">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="69a8e-188">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="69a8e-188">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="69a8e-189">Der für Windows-VMS zu verwendende Administrator-Benutzername.</span><span class="sxs-lookup"><span data-stu-id="69a8e-189">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="69a8e-190">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="69a8e-190">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="69a8e-191">Das für Windows-VMS zu verwendende Administratorkennwort, dessen Länge mindestens 12 sein muss, mit mindestens einem Kleinbuchstaben, also `[a-z]` einem `[A-Z]` und einem Sonderzeichen `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="69a8e-191">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="69a8e-192">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="69a8e-192">-WorkspaceResourceId</span></span>
<span data-ttu-id="69a8e-193">Ressourcen-ID des Arbeitsbereichs des Überwachungs-addons.</span><span class="sxs-lookup"><span data-stu-id="69a8e-193">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="69a8e-194">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69a8e-194">-Confirm</span></span>
<span data-ttu-id="69a8e-195">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69a8e-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a8e-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a8e-196">-WhatIf</span></span>
<span data-ttu-id="69a8e-197">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69a8e-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a8e-198">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69a8e-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a8e-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a8e-199">CommonParameters</span></span>
<span data-ttu-id="69a8e-200">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a8e-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a8e-201">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69a8e-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a8e-202">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69a8e-202">INPUTS</span></span>

### <span data-ttu-id="69a8e-203">Keine</span><span class="sxs-lookup"><span data-stu-id="69a8e-203">None</span></span>

## <span data-ttu-id="69a8e-204">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69a8e-204">OUTPUTS</span></span>

### <span data-ttu-id="69a8e-205">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="69a8e-205">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="69a8e-206">Notizen</span><span class="sxs-lookup"><span data-stu-id="69a8e-206">NOTES</span></span>

## <span data-ttu-id="69a8e-207">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69a8e-207">RELATED LINKS</span></span>
