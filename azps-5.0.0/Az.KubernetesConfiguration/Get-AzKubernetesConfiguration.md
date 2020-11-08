---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179242"
---
# <span data-ttu-id="dc8c4-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc8c4-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="dc8c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8c4-103">Ruft Details der Quell Code Verwaltungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="dc8c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc8c4-104">SYNTAX</span></span>

### <span data-ttu-id="dc8c4-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc8c4-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc8c4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="dc8c4-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc8c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc8c4-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc8c4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc8c4-108">DESCRIPTION</span></span>
<span data-ttu-id="dc8c4-109">Ruft Details der Quell Code Verwaltungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="dc8c4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc8c4-110">EXAMPLES</span></span>

### <span data-ttu-id="dc8c4-111">Beispiel 1: Abrufen aller Konfigurationen des kubernetes-Clusters</span><span class="sxs-lookup"><span data-stu-id="dc8c4-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dc8c4-112">Dieser Befehl ruft alle Konfigurationen des kubernetes-Clusters ab.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="dc8c4-113">Beispiel 2: Abrufen einer Konfiguration des kubernetes-Clusters anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="dc8c4-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dc8c4-114">Dieser Befehl ruft eine Konfiguration des kubernetes-Clusters mit dem Namen ab.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="dc8c4-115">Beispiel 3: Abrufen einer Konfiguration des kubernetes-Clusters nach Objekt</span><span class="sxs-lookup"><span data-stu-id="dc8c4-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dc8c4-116">Dieser Befehl ruft eine Konfiguration des kubernetes-Clusters nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="dc8c4-117">Beispiel 4: Abrufen einer Konfiguration des kubernetes-Clusters nach Pipeline</span><span class="sxs-lookup"><span data-stu-id="dc8c4-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="dc8c4-118">Dieser Befehl ruft eine Konfiguration des kubernetes-Clusters nach Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="dc8c4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc8c4-119">PARAMETERS</span></span>

### <span data-ttu-id="dc8c4-120">-Clustername</span><span class="sxs-lookup"><span data-stu-id="dc8c4-120">-ClusterName</span></span>
<span data-ttu-id="dc8c4-121">Der Name des kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="dc8c4-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="dc8c4-122">-ClusterRp</span></span>
<span data-ttu-id="dc8c4-123">Der Kubernetes-Cluster RP – entweder Microsoft. ContainerService (für AKS-Cluster) oder Microsoft. Kubernetes (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="dc8c4-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="dc8c4-124">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="dc8c4-124">-ClusterType</span></span>
<span data-ttu-id="dc8c4-125">Der Kubernetes-Clusterressourcen Name – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="dc8c4-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="dc8c4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8c4-126">-DefaultProfile</span></span>
<span data-ttu-id="dc8c4-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8c4-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc8c4-128">-InputObject</span></span>
<span data-ttu-id="dc8c4-129">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc8c4-130">-Name</span><span class="sxs-lookup"><span data-stu-id="dc8c4-130">-Name</span></span>
<span data-ttu-id="dc8c4-131">Der Name der Quell Code Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="dc8c4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8c4-132">-ResourceGroupName</span></span>
<span data-ttu-id="dc8c4-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc8c4-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dc8c4-134">-SubscriptionId</span></span>
<span data-ttu-id="dc8c4-135">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-135">The Azure subscription ID.</span></span>
<span data-ttu-id="dc8c4-136">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="dc8c4-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="dc8c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8c4-137">CommonParameters</span></span>
<span data-ttu-id="dc8c4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8c4-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc8c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8c4-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc8c4-140">INPUTS</span></span>

### <span data-ttu-id="dc8c4-141">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="dc8c4-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="dc8c4-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc8c4-142">OUTPUTS</span></span>

### <span data-ttu-id="dc8c4-143">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc8c4-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="dc8c4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc8c4-144">NOTES</span></span>

<span data-ttu-id="dc8c4-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="dc8c4-145">ALIASES</span></span>

<span data-ttu-id="dc8c4-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc8c4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc8c4-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc8c4-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc8c4-149">Inputobject <IKubernetesConfigurationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="dc8c4-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc8c4-150">`[ClusterName <String>]`: Der Name des kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="dc8c4-151">`[ClusterResourceName <String>]`: Der Kubernetes-Clusterressourcen Name – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="dc8c4-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="dc8c4-152">`[ClusterRp <String>]`: Kubernetes-Cluster RP – entweder Microsoft. ContainerService (für AKS-Cluster) oder Microsoft. Kubernetes (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="dc8c4-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="dc8c4-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="dc8c4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc8c4-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="dc8c4-155">`[SourceControlConfigurationName <String>]`: Name der Quell Code Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="dc8c4-156">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="dc8c4-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="dc8c4-157">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="dc8c4-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="dc8c4-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc8c4-158">RELATED LINKS</span></span>

