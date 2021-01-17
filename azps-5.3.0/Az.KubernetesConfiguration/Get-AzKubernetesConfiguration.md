---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459148"
---
# <span data-ttu-id="42e88-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="42e88-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="42e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42e88-102">SYNOPSIS</span></span>
<span data-ttu-id="42e88-103">Ruft Details zur Quellcodeverwaltungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="42e88-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="42e88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42e88-104">SYNTAX</span></span>

### <span data-ttu-id="42e88-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="42e88-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42e88-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="42e88-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42e88-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="42e88-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="42e88-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42e88-108">DESCRIPTION</span></span>
<span data-ttu-id="42e88-109">Ruft Details zur Quellcodeverwaltungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="42e88-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="42e88-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42e88-110">EXAMPLES</span></span>

### <span data-ttu-id="42e88-111">Beispiel 1: Alle Konfigurationen des Kubernetclusters erhalten</span><span class="sxs-lookup"><span data-stu-id="42e88-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="42e88-112">Dieser Befehl ruft alle Konfigurationen des Kubernetes-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="42e88-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="42e88-113">Beispiel 2: Erhalten einer Konfiguration des Kubernetsclusters nach Name</span><span class="sxs-lookup"><span data-stu-id="42e88-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="42e88-114">Dieser Befehl ruft eine Konfiguration des Kubernetes-Clusters nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="42e88-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="42e88-115">Beispiel 3: Erhalten einer Konfiguration von "Kubernetes Cluster by Object"</span><span class="sxs-lookup"><span data-stu-id="42e88-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="42e88-116">Dieser Befehl ruft eine Konfiguration von "kubernetes cluster by object" ab.</span><span class="sxs-lookup"><span data-stu-id="42e88-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="42e88-117">Beispiel 4: Erhalten einer Konfiguration eines Kubernetclusters nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="42e88-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="42e88-118">Dieser Befehl ruft eine Konfiguration von "kubernetes cluster by pipeline" ab.</span><span class="sxs-lookup"><span data-stu-id="42e88-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="42e88-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42e88-119">PARAMETERS</span></span>

### <span data-ttu-id="42e88-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="42e88-120">-ClusterName</span></span>
<span data-ttu-id="42e88-121">Der Name des Kubernetenclusters.</span><span class="sxs-lookup"><span data-stu-id="42e88-121">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="42e88-122">-ClusterRp</span></span>
<span data-ttu-id="42e88-123">Der Kubernetes-Cluster-RP – entweder Microsoft.ContainerService (für AKS-Cluster) oder Microsoft.Kubernetes (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="42e88-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="42e88-124">-ClusterType</span></span>
<span data-ttu-id="42e88-125">Der Ressourcenname des Kubernetes-Clusters – entweder managedClusters (für AKS-Cluster) oder verbundene Cluster (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="42e88-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e88-126">-DefaultProfile</span></span>
<span data-ttu-id="42e88-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42e88-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42e88-128">-InputObject</span></span>
<span data-ttu-id="42e88-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="42e88-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-130">-Name</span><span class="sxs-lookup"><span data-stu-id="42e88-130">-Name</span></span>
<span data-ttu-id="42e88-131">Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="42e88-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e88-132">-ResourceGroupName</span></span>
<span data-ttu-id="42e88-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42e88-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42e88-134">-SubscriptionId</span></span>
<span data-ttu-id="42e88-135">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="42e88-135">The Azure subscription ID.</span></span>
<span data-ttu-id="42e88-136">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="42e88-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e88-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e88-137">CommonParameters</span></span>
<span data-ttu-id="42e88-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e88-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e88-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42e88-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e88-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42e88-140">INPUTS</span></span>

### <span data-ttu-id="42e88-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IAkiernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="42e88-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="42e88-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42e88-142">OUTPUTS</span></span>

### <span data-ttu-id="42e88-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="42e88-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="42e88-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="42e88-144">NOTES</span></span>

<span data-ttu-id="42e88-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="42e88-145">ALIASES</span></span>

<span data-ttu-id="42e88-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="42e88-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42e88-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42e88-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42e88-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="42e88-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42e88-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="42e88-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="42e88-150">`[ClusterName <String>]`: Der Name des Kubernetenclusters.</span><span class="sxs-lookup"><span data-stu-id="42e88-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="42e88-151">`[ClusterResourceName <String>]`: Der Ressourcenname des Kubernetes-Clusters – entweder managedClusters (für AKS-Cluster) oder verbundene Cluster (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="42e88-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="42e88-152">`[ClusterRp <String>]`: Der Kubernetes-Cluster-RP – entweder Microsoft.ContainerService (für AKS-Cluster) oder Microsoft.Kubernetes (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="42e88-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="42e88-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="42e88-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="42e88-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42e88-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="42e88-155">`[SourceControlConfigurationName <String>]`: Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="42e88-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="42e88-156">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="42e88-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="42e88-157">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="42e88-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="42e88-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="42e88-158">RELATED LINKS</span></span>

