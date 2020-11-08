---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166560"
---
# <span data-ttu-id="29314-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="29314-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="29314-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29314-102">SYNOPSIS</span></span>
<span data-ttu-id="29314-103">Erstellen Sie eine neue Kubernetes-Quell Code Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="29314-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="29314-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29314-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29314-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29314-105">DESCRIPTION</span></span>
<span data-ttu-id="29314-106">Erstellen Sie eine neue Kubernetes-Quell Code Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="29314-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="29314-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29314-107">EXAMPLES</span></span>

### <span data-ttu-id="29314-108">Beispiel 1: Erstellen eines Konfigurations für kubernetes-Cluster</span><span class="sxs-lookup"><span data-stu-id="29314-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="29314-109">Mit diesem Befehl wird ein Konfigurations für kubernetes-Cluster erstellt.</span><span class="sxs-lookup"><span data-stu-id="29314-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="29314-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="29314-110">PARAMETERS</span></span>

### <span data-ttu-id="29314-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="29314-111">-ClusterName</span></span>
<span data-ttu-id="29314-112">Der Name des kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="29314-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="29314-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="29314-113">-ClusterScoped</span></span>
<span data-ttu-id="29314-114">Bei Übergabe wird der Bereich der Konfiguration auf Cluster gesetzt (Standard ist Namespace).</span><span class="sxs-lookup"><span data-stu-id="29314-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="29314-115">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="29314-115">-ClusterType</span></span>
<span data-ttu-id="29314-116">Der Kubernetes-Clusterressourcen Name – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="29314-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="29314-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29314-117">-DefaultProfile</span></span>
<span data-ttu-id="29314-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29314-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29314-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="29314-119">-EnableHelmOperator</span></span>
<span data-ttu-id="29314-120">Option zum Aktivieren des Helms-Operators für diese git-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="29314-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="29314-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="29314-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="29314-122">Überschreibung der Werte für das Steuer Diagramm des Operators</span><span class="sxs-lookup"><span data-stu-id="29314-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="29314-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="29314-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="29314-124">Die Version des Operators Helm-Diagramms.</span><span class="sxs-lookup"><span data-stu-id="29314-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="29314-125">-Name</span><span class="sxs-lookup"><span data-stu-id="29314-125">-Name</span></span>
<span data-ttu-id="29314-126">Der Name der Quell Code Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="29314-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="29314-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="29314-127">-OperatorInstanceName</span></span>
<span data-ttu-id="29314-128">Instanzname des Operators – identifizieren der jeweiligen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="29314-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="29314-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="29314-129">-OperatorNamespace</span></span>
<span data-ttu-id="29314-130">Der Namespace, in dem dieser Operator installiert ist.</span><span class="sxs-lookup"><span data-stu-id="29314-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="29314-131">Maximal zulässige alphanumerische Zeichen in 253 Kleinbuchstaben, Bindestrich und Punkt.</span><span class="sxs-lookup"><span data-stu-id="29314-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="29314-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="29314-132">-OperatorParameters</span></span>
<span data-ttu-id="29314-133">Alle Parameter für die Operator Instanz im Zeichenfolgenformat</span><span class="sxs-lookup"><span data-stu-id="29314-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="29314-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="29314-134">-RepositoryUrl</span></span>
<span data-ttu-id="29314-135">Die URL des SourceControl-Repositorys.</span><span class="sxs-lookup"><span data-stu-id="29314-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="29314-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29314-136">-ResourceGroupName</span></span>
<span data-ttu-id="29314-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29314-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="29314-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="29314-138">-SubscriptionId</span></span>
<span data-ttu-id="29314-139">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="29314-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="29314-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29314-140">-Confirm</span></span>
<span data-ttu-id="29314-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29314-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29314-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29314-142">-WhatIf</span></span>
<span data-ttu-id="29314-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29314-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29314-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29314-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29314-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29314-145">CommonParameters</span></span>
<span data-ttu-id="29314-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29314-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29314-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29314-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29314-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29314-148">INPUTS</span></span>

## <span data-ttu-id="29314-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29314-149">OUTPUTS</span></span>

### <span data-ttu-id="29314-150">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="29314-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="29314-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="29314-151">NOTES</span></span>

<span data-ttu-id="29314-152">Aliase</span><span class="sxs-lookup"><span data-stu-id="29314-152">ALIASES</span></span>

## <span data-ttu-id="29314-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29314-153">RELATED LINKS</span></span>

