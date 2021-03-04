---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 0040ab3bc037527400ea1f3eabf3c887189fc73c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931027"
---
# <span data-ttu-id="da84d-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="da84d-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="da84d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da84d-102">SYNOPSIS</span></span>
<span data-ttu-id="da84d-103">Erstellen Sie eine neue Kubernetes-Quellsteuerelementkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="da84d-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="da84d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da84d-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da84d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da84d-105">DESCRIPTION</span></span>
<span data-ttu-id="da84d-106">Erstellen Sie eine neue Kubernetes-Quellsteuerelementkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="da84d-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="da84d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da84d-107">EXAMPLES</span></span>

### <span data-ttu-id="da84d-108">Beispiel 1: Erstellen einer Konfiguration für den Kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="da84d-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="da84d-109">Mit diesem Befehl wird eine Konfiguration für den Kubernetes-Cluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="da84d-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="da84d-110">Beispiel 1: Erstellen einer Konfiguration für den Kubernetes-Cluster mit angeben von Paramter OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="da84d-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="da84d-111">Mit diesem Befehl wird eine Konfiguration im neuen Operatornamespace für den Kubernetes-Cluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="da84d-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="da84d-112">Hinweis: Eine Konfiguration in einem vorhandenen Operatornamespace kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="da84d-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="da84d-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="da84d-113">PARAMETERS</span></span>

### <span data-ttu-id="da84d-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="da84d-114">-ClusterName</span></span>
<span data-ttu-id="da84d-115">Der Name des Kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="da84d-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="da84d-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="da84d-116">-ClusterScoped</span></span>
<span data-ttu-id="da84d-117">Wenn übergeben festgelegt wird, legen Sie den Bereich der Konfiguration auf Cluster (Standard ist nameSpace) ein.</span><span class="sxs-lookup"><span data-stu-id="da84d-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="da84d-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="da84d-118">-ClusterType</span></span>
<span data-ttu-id="da84d-119">Der Name der Kubernetes-Clusterressourcen – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="da84d-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="da84d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da84d-120">-DefaultProfile</span></span>
<span data-ttu-id="da84d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da84d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da84d-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="da84d-122">-EnableHelmOperator</span></span>
<span data-ttu-id="da84d-123">Option zum Aktivieren des Helmoperators für diese Git-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="da84d-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="da84d-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="da84d-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="da84d-125">Werte überschreiben für das Diagramm "Helm" des Operators.</span><span class="sxs-lookup"><span data-stu-id="da84d-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="da84d-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="da84d-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="da84d-127">Version des Operator -Diagramms "Helm".</span><span class="sxs-lookup"><span data-stu-id="da84d-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="da84d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="da84d-128">-Name</span></span>
<span data-ttu-id="da84d-129">Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="da84d-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da84d-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="da84d-130">-OperatorInstanceName</span></span>
<span data-ttu-id="da84d-131">Instanzname des Operators – Identifizieren der spezifischen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="da84d-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="da84d-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="da84d-132">-OperatorNamespace</span></span>
<span data-ttu-id="da84d-133">Der Namespace, auf dem dieser Operator installiert ist.</span><span class="sxs-lookup"><span data-stu-id="da84d-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="da84d-134">Maximal 253 alphanumerische Zeichen, Bindestriche und Perioden</span><span class="sxs-lookup"><span data-stu-id="da84d-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="da84d-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="da84d-135">-OperatorParameters</span></span>
<span data-ttu-id="da84d-136">Alle Parameter für die Operatorinstanz im Zeichenfolgenformat.</span><span class="sxs-lookup"><span data-stu-id="da84d-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="da84d-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="da84d-137">-RepositoryUrl</span></span>
<span data-ttu-id="da84d-138">URL des SourceControl-Repositorys.</span><span class="sxs-lookup"><span data-stu-id="da84d-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="da84d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da84d-139">-ResourceGroupName</span></span>
<span data-ttu-id="da84d-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da84d-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="da84d-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da84d-141">-SubscriptionId</span></span>
<span data-ttu-id="da84d-142">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="da84d-142">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da84d-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da84d-143">-Confirm</span></span>
<span data-ttu-id="da84d-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da84d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da84d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da84d-145">-WhatIf</span></span>
<span data-ttu-id="da84d-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da84d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da84d-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da84d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da84d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da84d-148">CommonParameters</span></span>
<span data-ttu-id="da84d-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da84d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da84d-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da84d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da84d-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da84d-151">INPUTS</span></span>

## <span data-ttu-id="da84d-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da84d-152">OUTPUTS</span></span>

### <span data-ttu-id="da84d-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="da84d-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20210301.ISourceControlConfiguration</span></span>

## <span data-ttu-id="da84d-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="da84d-154">NOTES</span></span>

<span data-ttu-id="da84d-155">ALIASE</span><span class="sxs-lookup"><span data-stu-id="da84d-155">ALIASES</span></span>

## <span data-ttu-id="da84d-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="da84d-156">RELATED LINKS</span></span>

