---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 7853119fcc68b709c2f4963dfa60ebc93ad03351
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165384"
---
# <span data-ttu-id="c7265-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="c7265-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="c7265-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7265-102">SYNOPSIS</span></span>
<span data-ttu-id="c7265-103">Aktualisieren oder Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="c7265-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c7265-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7265-104">SYNTAX</span></span>

### <span data-ttu-id="c7265-105">defaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7265-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7265-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7265-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7265-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7265-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7265-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7265-108">DESCRIPTION</span></span>
<span data-ttu-id="c7265-109">Aktualisieren oder Erstellen eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="c7265-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c7265-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7265-110">EXAMPLES</span></span>

### <span data-ttu-id="c7265-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7265-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="c7265-112">Stellen Sie die Anzahl der Knoten im Kubernetes-Cluster auf 5 ein.</span><span class="sxs-lookup"><span data-stu-id="c7265-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="c7265-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7265-113">PARAMETERS</span></span>

### <span data-ttu-id="c7265-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7265-114">-AsJob</span></span>
<span data-ttu-id="c7265-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c7265-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7265-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7265-116">-DefaultProfile</span></span>
<span data-ttu-id="c7265-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7265-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7265-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="c7265-118">-DnsNamePrefix</span></span>
<span data-ttu-id="c7265-119">Das DNS-Namenspräfix für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="c7265-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="c7265-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="c7265-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="c7265-121">Ob die automatische Skalierung aktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="c7265-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="c7265-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c7265-122">-Id</span></span>
<span data-ttu-id="c7265-123">ID eines verwalteten Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="c7265-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c7265-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7265-124">-InputObject</span></span>
<span data-ttu-id="c7265-125">Ein PSKubernetesCluster-Objekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c7265-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c7265-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="c7265-126">-KubernetesVersion</span></span>
<span data-ttu-id="c7265-127">Die Version von Kubernetes, die zum Erstellen des Clusters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7265-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="c7265-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="c7265-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="c7265-129">Benutzername für die virtuellen Linux-Computer.</span><span class="sxs-lookup"><span data-stu-id="c7265-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="c7265-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="c7265-130">-Location</span></span>
<span data-ttu-id="c7265-131">Azure-Speicherort für den Cluster.</span><span class="sxs-lookup"><span data-stu-id="c7265-131">Azure location for the cluster.</span></span>
<span data-ttu-id="c7265-132">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7265-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="c7265-133">-Name</span><span class="sxs-lookup"><span data-stu-id="c7265-133">-Name</span></span>
<span data-ttu-id="c7265-134">Kubernetes verwalteter Cluster Name.</span><span class="sxs-lookup"><span data-stu-id="c7265-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="c7265-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c7265-135">-NodeCount</span></span>
<span data-ttu-id="c7265-136">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="c7265-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="c7265-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="c7265-137">-NodeMaxCount</span></span>
<span data-ttu-id="c7265-138">Maximale Anzahl von Knoten für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="c7265-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="c7265-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="c7265-139">-NodeMinCount</span></span>
<span data-ttu-id="c7265-140">Minimale Anzahl von Knoten für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="c7265-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="c7265-141">-Nodename</span><span class="sxs-lookup"><span data-stu-id="c7265-141">-NodeName</span></span>
<span data-ttu-id="c7265-142">Eindeutiger Name des Agenten Pool Profils im Kontext der Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c7265-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="c7265-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="c7265-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="c7265-144">Die Standardanzahl von Knoten für die Knoten Pools.</span><span class="sxs-lookup"><span data-stu-id="c7265-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="c7265-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="c7265-145">-NodePoolMode</span></span>
<span data-ttu-id="c7265-146">NodePoolMode stellt den Modus eines Knoten Pools dar.</span><span class="sxs-lookup"><span data-stu-id="c7265-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="c7265-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="c7265-147">-NodeVmSize</span></span>
<span data-ttu-id="c7265-148">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c7265-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="c7265-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7265-149">-ResourceGroupName</span></span>
<span data-ttu-id="c7265-150">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c7265-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7265-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="c7265-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="c7265-152">Die Client-ID und der Client Schlüssel, die dem AAD-Application/Service-Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c7265-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7265-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="c7265-153">-SshKeyValue</span></span>
<span data-ttu-id="c7265-154">SSH-Schlüsseldatei Wert oder Schlüssel Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="c7265-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="c7265-155">Standardmäßig ist {Home}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="c7265-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="c7265-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7265-156">-Tag</span></span>
<span data-ttu-id="c7265-157">Tags, die auf die Ressource angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="c7265-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="c7265-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7265-158">-Confirm</span></span>
<span data-ttu-id="c7265-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7265-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7265-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7265-160">-WhatIf</span></span>
<span data-ttu-id="c7265-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7265-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7265-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7265-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7265-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7265-163">CommonParameters</span></span>
<span data-ttu-id="c7265-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7265-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7265-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7265-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7265-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7265-166">INPUTS</span></span>

### <span data-ttu-id="c7265-167">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c7265-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c7265-168">System. String</span><span class="sxs-lookup"><span data-stu-id="c7265-168">System.String</span></span>

## <span data-ttu-id="c7265-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7265-169">OUTPUTS</span></span>

### <span data-ttu-id="c7265-170">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c7265-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c7265-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7265-171">NOTES</span></span>

## <span data-ttu-id="c7265-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7265-172">RELATED LINKS</span></span>
