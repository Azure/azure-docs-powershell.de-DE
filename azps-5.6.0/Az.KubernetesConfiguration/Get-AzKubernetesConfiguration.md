---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 8cbf938917f26b1229b5c18d25448da4df3bb5b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931032"
---
# <span data-ttu-id="96be1-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="96be1-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="96be1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96be1-102">SYNOPSIS</span></span>
<span data-ttu-id="96be1-103">Ruft Details zur Quellsteuerelementkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="96be1-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="96be1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96be1-104">SYNTAX</span></span>

### <span data-ttu-id="96be1-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="96be1-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96be1-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="96be1-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96be1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96be1-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="96be1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96be1-108">DESCRIPTION</span></span>
<span data-ttu-id="96be1-109">Ruft Details zur Quellsteuerelementkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="96be1-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="96be1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96be1-110">EXAMPLES</span></span>

### <span data-ttu-id="96be1-111">Beispiel 1: Alle Konfigurationen des Kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="96be1-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:27:45 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="96be1-112">Dieser Befehl ruft alle Konfigurationen des kubernetes-Clusters ab.</span><span class="sxs-lookup"><span data-stu-id="96be1-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="96be1-113">Beispiel 2: Erhalten einer Konfiguration des Kubernetes-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="96be1-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\>  Get-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name  k8sconfig-t02

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="96be1-114">Dieser Befehl ruft eine Konfiguration des Kubernetes-Clusters nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="96be1-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="96be1-115">Beispiel 3: Erhalten einer Konfiguration von Kubernetes-Cluster nach Objekt</span><span class="sxs-lookup"><span data-stu-id="96be1-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name k8sconfig-t02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="96be1-116">Dieser Befehl ruft eine Konfiguration des kubernetes-Clusters nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="96be1-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="96be1-117">Beispiel 4: Erhalten einer Konfiguration des Kubernetes-Clusters per Pipeline</span><span class="sxs-lookup"><span data-stu-id="96be1-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/xxxxx-xxxxxxx-xxxxx-xxxxxx/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/k8sconfig-t02'} | Get-AzKubernetesConfiguration

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:29:33 AM                                             12/21/2020 5:29:33 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="96be1-118">Dieser Befehl ruft eine Konfiguration des kubernetes-Clusters per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="96be1-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="96be1-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="96be1-119">PARAMETERS</span></span>

### <span data-ttu-id="96be1-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="96be1-120">-ClusterName</span></span>
<span data-ttu-id="96be1-121">Der Name des Kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="96be1-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="96be1-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="96be1-122">-ClusterRp</span></span>
<span data-ttu-id="96be1-123">Das Kubernetes-Cluster-RP – entweder Microsoft.ContainerService (für AKS-Cluster) oder Microsoft.Kubernetes (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="96be1-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="96be1-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="96be1-124">-ClusterType</span></span>
<span data-ttu-id="96be1-125">Der Name der Kubernetes-Clusterressourcen – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="96be1-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="96be1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96be1-126">-DefaultProfile</span></span>
<span data-ttu-id="96be1-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96be1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96be1-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96be1-128">-InputObject</span></span>
<span data-ttu-id="96be1-129">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="96be1-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96be1-130">-Name</span><span class="sxs-lookup"><span data-stu-id="96be1-130">-Name</span></span>
<span data-ttu-id="96be1-131">Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="96be1-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="96be1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96be1-132">-ResourceGroupName</span></span>
<span data-ttu-id="96be1-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96be1-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="96be1-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96be1-134">-SubscriptionId</span></span>
<span data-ttu-id="96be1-135">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="96be1-135">The Azure subscription ID.</span></span>
<span data-ttu-id="96be1-136">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="96be1-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="96be1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96be1-137">CommonParameters</span></span>
<span data-ttu-id="96be1-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96be1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96be1-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96be1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96be1-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96be1-140">INPUTS</span></span>

### <span data-ttu-id="96be1-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="96be1-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="96be1-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96be1-142">OUTPUTS</span></span>

### <span data-ttu-id="96be1-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="96be1-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="96be1-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="96be1-144">NOTES</span></span>

<span data-ttu-id="96be1-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="96be1-145">ALIASES</span></span>

<span data-ttu-id="96be1-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="96be1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96be1-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="96be1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96be1-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96be1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96be1-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="96be1-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96be1-150">`[ClusterName <String>]`: Der Name des Kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="96be1-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="96be1-151">`[ClusterResourceName <String>]`: Der Name der Kubernetes-Clusterressource – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="96be1-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="96be1-152">`[ClusterRp <String>]`: Das Kubernetes-Cluster-RP – entweder Microsoft.ContainerService (für AKS-Cluster) oder Microsoft.Kubernetes (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="96be1-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="96be1-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="96be1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96be1-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96be1-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="96be1-155">`[SourceControlConfigurationName <String>]`: Name der Quellsteuerelementkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="96be1-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="96be1-156">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="96be1-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="96be1-157">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="96be1-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="96be1-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="96be1-158">RELATED LINKS</span></span>

