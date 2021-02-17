---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171996"
---
# <span data-ttu-id="94c39-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="94c39-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="94c39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94c39-102">SYNOPSIS</span></span>
<span data-ttu-id="94c39-103">Aktualisieren oder erstellen Sie einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="94c39-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="94c39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94c39-104">SYNTAX</span></span>

### <span data-ttu-id="94c39-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="94c39-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c39-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94c39-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c39-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94c39-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94c39-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94c39-108">DESCRIPTION</span></span>
<span data-ttu-id="94c39-109">Aktualisieren oder erstellen Sie einen verwalteten Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="94c39-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="94c39-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94c39-110">EXAMPLES</span></span>

### <span data-ttu-id="94c39-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94c39-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="94c39-112">Legen Sie die Anzahl der Knoten im Cluster "Kubernetes" auf 5.</span><span class="sxs-lookup"><span data-stu-id="94c39-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="94c39-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94c39-113">PARAMETERS</span></span>

### <span data-ttu-id="94c39-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94c39-114">-AsJob</span></span>
<span data-ttu-id="94c39-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="94c39-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94c39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c39-116">-DefaultProfile</span></span>
<span data-ttu-id="94c39-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94c39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c39-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="94c39-118">-DnsNamePrefix</span></span>
<span data-ttu-id="94c39-119">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="94c39-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="94c39-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="94c39-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="94c39-121">Aktivieren der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="94c39-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="94c39-122">-ID</span><span class="sxs-lookup"><span data-stu-id="94c39-122">-Id</span></span>
<span data-ttu-id="94c39-123">ID eines verwalteten Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="94c39-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c39-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94c39-124">-InputObject</span></span>
<span data-ttu-id="94c39-125">Ein PSAkiernetesCluster-Objekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="94c39-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94c39-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="94c39-126">-KubernetesVersion</span></span>
<span data-ttu-id="94c39-127">Die Version von Kubernetes, die zum Erstellen des Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94c39-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="94c39-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="94c39-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="94c39-129">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="94c39-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="94c39-130">-Location</span><span class="sxs-lookup"><span data-stu-id="94c39-130">-Location</span></span>
<span data-ttu-id="94c39-131">Azure-Standort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="94c39-131">Azure location for the cluster.</span></span>
<span data-ttu-id="94c39-132">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="94c39-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="94c39-133">-Name</span><span class="sxs-lookup"><span data-stu-id="94c39-133">-Name</span></span>
<span data-ttu-id="94c39-134">Verwalteter Clustername in Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="94c39-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c39-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="94c39-135">-NodeCount</span></span>
<span data-ttu-id="94c39-136">Die Standardanzahl von Knoten für die Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="94c39-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="94c39-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="94c39-137">-NodeMaxCount</span></span>
<span data-ttu-id="94c39-138">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="94c39-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="94c39-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="94c39-139">-NodeMinCount</span></span>
<span data-ttu-id="94c39-140">Mindestanzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="94c39-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="94c39-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="94c39-141">-NodeName</span></span>
<span data-ttu-id="94c39-142">Eindeutiger Name des Agentpoolprofils im Kontext des Abonnements und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94c39-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="94c39-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="94c39-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="94c39-144">Die Standardanzahl von Knoten für die Knotenpools.</span><span class="sxs-lookup"><span data-stu-id="94c39-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="94c39-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="94c39-145">-NodePoolMode</span></span>
<span data-ttu-id="94c39-146">NodePoolMode stellt den Modus eines Knotenpools dar.</span><span class="sxs-lookup"><span data-stu-id="94c39-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="94c39-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="94c39-147">-NodeVmSize</span></span>
<span data-ttu-id="94c39-148">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="94c39-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="94c39-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c39-149">-ResourceGroupName</span></span>
<span data-ttu-id="94c39-150">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="94c39-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c39-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="94c39-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="94c39-152">Die Client-ID und der geheime Clientgeheimnis, die der Anwendung bzw. dem Dienstprinzipal von AAD zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94c39-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c39-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="94c39-153">-SshKeyValue</span></span>
<span data-ttu-id="94c39-154">Wert der SSH-Schlüsseldatei oder Schlüsseldateipfad.</span><span class="sxs-lookup"><span data-stu-id="94c39-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="94c39-155">Der Standardwert ist {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="94c39-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="94c39-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="94c39-156">-Tag</span></span>
<span data-ttu-id="94c39-157">Auf die Ressource anzuwendende Tags</span><span class="sxs-lookup"><span data-stu-id="94c39-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="94c39-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94c39-158">-Confirm</span></span>
<span data-ttu-id="94c39-159">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94c39-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c39-160">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="94c39-160">-WhatIf</span></span>
<span data-ttu-id="94c39-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94c39-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c39-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94c39-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c39-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c39-163">CommonParameters</span></span>
<span data-ttu-id="94c39-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c39-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c39-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94c39-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c39-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94c39-166">INPUTS</span></span>

### <span data-ttu-id="94c39-167">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="94c39-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="94c39-168">System.String</span><span class="sxs-lookup"><span data-stu-id="94c39-168">System.String</span></span>

## <span data-ttu-id="94c39-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94c39-169">OUTPUTS</span></span>

### <span data-ttu-id="94c39-170">Microsoft.Azure.Commands.Aks.Models.PSAkiernetesCluster</span><span class="sxs-lookup"><span data-stu-id="94c39-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="94c39-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="94c39-171">NOTES</span></span>

## <span data-ttu-id="94c39-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="94c39-172">RELATED LINKS</span></span>
