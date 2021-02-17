---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 425a2f2fcc145b360ea981a4d78113d6053c90e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152572"
---
# <span data-ttu-id="577ce-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="577ce-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="577ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577ce-102">SYNOPSIS</span></span>
<span data-ttu-id="577ce-103">Erstellen Sie eine neue Konfiguration der Kubernetes-Quellsteuerung.</span><span class="sxs-lookup"><span data-stu-id="577ce-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="577ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="577ce-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="577ce-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="577ce-105">DESCRIPTION</span></span>
<span data-ttu-id="577ce-106">Erstellen Sie eine neue Konfiguration der Kubernetes-Quellsteuerung.</span><span class="sxs-lookup"><span data-stu-id="577ce-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="577ce-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="577ce-107">EXAMPLES</span></span>

### <span data-ttu-id="577ce-108">Beispiel 1: Erstellen einer Konfiguration für den Cluster "Kubernetes"</span><span class="sxs-lookup"><span data-stu-id="577ce-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="577ce-109">Mit diesem Befehl wird eine Konfiguration für den Kubernetes-Cluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="577ce-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="577ce-110">Beispiel 1: Erstellen einer Konfiguration für einen Kubernetes-Cluster mit Angabe des ParameteroperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="577ce-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="577ce-111">Dieser Befehl erstellt eine Konfiguration im neuen Operatornamespace für den Kubernetes-Cluster.</span><span class="sxs-lookup"><span data-stu-id="577ce-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="577ce-112">Hinweis: Es ist nicht möglich, eine Konfiguration in einem vorhandenen Operatornamespace zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="577ce-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="577ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="577ce-113">PARAMETERS</span></span>

### <span data-ttu-id="577ce-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="577ce-114">-ClusterName</span></span>
<span data-ttu-id="577ce-115">Der Name des Kubernetenclusters.</span><span class="sxs-lookup"><span data-stu-id="577ce-115">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="577ce-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="577ce-116">-ClusterScoped</span></span>
<span data-ttu-id="577ce-117">Legen Sie bei übergebener Prüfung den Umfang der Konfiguration auf "Cluster" (Der Standardwert ist "nameSpace").</span><span class="sxs-lookup"><span data-stu-id="577ce-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="577ce-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="577ce-118">-ClusterType</span></span>
<span data-ttu-id="577ce-119">Der Ressourcenname des Kubernetes-Clusters – entweder managedClusters (für AKS-Cluster) oder verbundene Cluster (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="577ce-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="577ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577ce-120">-DefaultProfile</span></span>
<span data-ttu-id="577ce-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="577ce-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="577ce-122">-EnableOperator</span><span class="sxs-lookup"><span data-stu-id="577ce-122">-EnableHelmOperator</span></span>
<span data-ttu-id="577ce-123">Option zum Aktivieren des Operators Für diese Git-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="577ce-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="577ce-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="577ce-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="577ce-125">Werte überschreiben für den Operator "Organigramm".</span><span class="sxs-lookup"><span data-stu-id="577ce-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="577ce-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="577ce-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="577ce-127">Version des Netzbetreiberdiagramms "Organigramm".</span><span class="sxs-lookup"><span data-stu-id="577ce-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="577ce-128">-Name</span><span class="sxs-lookup"><span data-stu-id="577ce-128">-Name</span></span>
<span data-ttu-id="577ce-129">Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="577ce-129">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="577ce-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="577ce-130">-OperatorInstanceName</span></span>
<span data-ttu-id="577ce-131">Instanzname des Operators – Identifizieren der spezifischen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="577ce-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="577ce-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="577ce-132">-OperatorNamespace</span></span>
<span data-ttu-id="577ce-133">Der Namespace, in dem dieser Operator installiert ist.</span><span class="sxs-lookup"><span data-stu-id="577ce-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="577ce-134">Maximal 253 alphanumerische Kleinzeichen, Bindestrich und Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="577ce-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="577ce-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="577ce-135">-OperatorParameters</span></span>
<span data-ttu-id="577ce-136">Alle Parameter für die Operatorinstanz im Zeichenfolgenformat.</span><span class="sxs-lookup"><span data-stu-id="577ce-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="577ce-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="577ce-137">-RepositoryUrl</span></span>
<span data-ttu-id="577ce-138">Url des SourceControl-Repositorys.</span><span class="sxs-lookup"><span data-stu-id="577ce-138">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="577ce-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577ce-139">-ResourceGroupName</span></span>
<span data-ttu-id="577ce-140">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="577ce-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="577ce-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="577ce-141">-SubscriptionId</span></span>
<span data-ttu-id="577ce-142">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="577ce-142">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="577ce-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="577ce-143">-Confirm</span></span>
<span data-ttu-id="577ce-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="577ce-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577ce-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="577ce-145">-WhatIf</span></span>
<span data-ttu-id="577ce-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="577ce-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577ce-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="577ce-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577ce-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577ce-148">CommonParameters</span></span>
<span data-ttu-id="577ce-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577ce-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577ce-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="577ce-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577ce-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="577ce-151">INPUTS</span></span>

## <span data-ttu-id="577ce-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="577ce-152">OUTPUTS</span></span>

### <span data-ttu-id="577ce-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="577ce-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="577ce-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="577ce-154">NOTES</span></span>

<span data-ttu-id="577ce-155">ALIASE</span><span class="sxs-lookup"><span data-stu-id="577ce-155">ALIASES</span></span>

## <span data-ttu-id="577ce-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="577ce-156">RELATED LINKS</span></span>

