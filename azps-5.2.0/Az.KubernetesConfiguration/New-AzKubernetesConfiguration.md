---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367728"
---
# <span data-ttu-id="0521e-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="0521e-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="0521e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0521e-102">SYNOPSIS</span></span>
<span data-ttu-id="0521e-103">Erstellen Sie eine neue Konfiguration der Kubernetes-Quellsteuerung.</span><span class="sxs-lookup"><span data-stu-id="0521e-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="0521e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0521e-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0521e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0521e-105">DESCRIPTION</span></span>
<span data-ttu-id="0521e-106">Erstellen Sie eine neue Konfiguration der Kubernetes-Quellsteuerung.</span><span class="sxs-lookup"><span data-stu-id="0521e-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="0521e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0521e-107">EXAMPLES</span></span>

### <span data-ttu-id="0521e-108">Beispiel 1: Erstellen einer Konfiguration für den Cluster "Kubernetes"</span><span class="sxs-lookup"><span data-stu-id="0521e-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="0521e-109">Mit diesem Befehl wird eine Konfiguration für den Cluster "kubernetes" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0521e-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="0521e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0521e-110">PARAMETERS</span></span>

### <span data-ttu-id="0521e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0521e-111">-ClusterName</span></span>
<span data-ttu-id="0521e-112">Der Name des Kubernetenclusters.</span><span class="sxs-lookup"><span data-stu-id="0521e-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="0521e-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="0521e-113">-ClusterScoped</span></span>
<span data-ttu-id="0521e-114">Legen Sie bei übergebener Prüfung den Umfang der Konfiguration auf "Cluster" (Der Standardwert ist "nameSpace").</span><span class="sxs-lookup"><span data-stu-id="0521e-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="0521e-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="0521e-115">-ClusterType</span></span>
<span data-ttu-id="0521e-116">Der Ressourcenname des Kubernetes-Clusters – entweder managedClusters (für AKS-Cluster) oder verbundene Cluster (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="0521e-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="0521e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0521e-117">-DefaultProfile</span></span>
<span data-ttu-id="0521e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0521e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0521e-119">-EnableOperator</span><span class="sxs-lookup"><span data-stu-id="0521e-119">-EnableHelmOperator</span></span>
<span data-ttu-id="0521e-120">Option zum Aktivieren des Operators Für diese Git-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0521e-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="0521e-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="0521e-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="0521e-122">Werte überschreiben für den Operator "Organigramm".</span><span class="sxs-lookup"><span data-stu-id="0521e-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="0521e-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="0521e-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="0521e-124">Version des Netzbetreiberdiagramms "Organigramm".</span><span class="sxs-lookup"><span data-stu-id="0521e-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="0521e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0521e-125">-Name</span></span>
<span data-ttu-id="0521e-126">Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0521e-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="0521e-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="0521e-127">-OperatorInstanceName</span></span>
<span data-ttu-id="0521e-128">Instanzname des Operators – Identifizieren der spezifischen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0521e-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="0521e-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="0521e-129">-OperatorNamespace</span></span>
<span data-ttu-id="0521e-130">Der Namespace, in dem dieser Operator installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0521e-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="0521e-131">Maximal 253 alphanumerische Kleinzeichen, Bindestrich und Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="0521e-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="0521e-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="0521e-132">-OperatorParameters</span></span>
<span data-ttu-id="0521e-133">Alle Parameter für die Operatorinstanz im Zeichenfolgenformat.</span><span class="sxs-lookup"><span data-stu-id="0521e-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="0521e-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="0521e-134">-RepositoryUrl</span></span>
<span data-ttu-id="0521e-135">Url des SourceControl-Repositorys.</span><span class="sxs-lookup"><span data-stu-id="0521e-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="0521e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0521e-136">-ResourceGroupName</span></span>
<span data-ttu-id="0521e-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0521e-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="0521e-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0521e-138">-SubscriptionId</span></span>
<span data-ttu-id="0521e-139">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0521e-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="0521e-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0521e-140">-Confirm</span></span>
<span data-ttu-id="0521e-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0521e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0521e-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0521e-142">-WhatIf</span></span>
<span data-ttu-id="0521e-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0521e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0521e-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0521e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0521e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0521e-145">CommonParameters</span></span>
<span data-ttu-id="0521e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0521e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0521e-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0521e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0521e-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0521e-148">INPUTS</span></span>

## <span data-ttu-id="0521e-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0521e-149">OUTPUTS</span></span>

### <span data-ttu-id="0521e-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0521e-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="0521e-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0521e-151">NOTES</span></span>

<span data-ttu-id="0521e-152">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0521e-152">ALIASES</span></span>

## <span data-ttu-id="0521e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0521e-153">RELATED LINKS</span></span>

