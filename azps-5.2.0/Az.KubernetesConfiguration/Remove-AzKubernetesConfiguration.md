---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361652"
---
# <span data-ttu-id="b3de2-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3de2-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="b3de2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3de2-102">SYNOPSIS</span></span>
<span data-ttu-id="b3de2-103">Dadurch wird die ZUM Einrichten der Quellsteuerungskonfiguration verwendete YAML-Datei gelöscht, was die zukünftige Synchronisierung aus dem Quell-Repository beendet.</span><span class="sxs-lookup"><span data-stu-id="b3de2-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="b3de2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3de2-104">SYNTAX</span></span>

### <span data-ttu-id="b3de2-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3de2-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3de2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3de2-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3de2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3de2-107">DESCRIPTION</span></span>
<span data-ttu-id="b3de2-108">Dadurch wird die ZUM Einrichten der Quellsteuerungskonfiguration verwendete YAML-Datei gelöscht, was die zukünftige Synchronisierung aus dem Quell-Repository beendet.</span><span class="sxs-lookup"><span data-stu-id="b3de2-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="b3de2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3de2-109">EXAMPLES</span></span>

### <span data-ttu-id="b3de2-110">Beispiel 1: Entfernen einer Konfiguration des Kubernetclusters nach Name</span><span class="sxs-lookup"><span data-stu-id="b3de2-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="b3de2-111">Mit diesem Befehl wird eine Konfiguration des Kubernetclusters nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="b3de2-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="b3de2-112">Beispiel 2: Entfernen einer Konfiguration von Kubernets (Cluster nach Objekt)</span><span class="sxs-lookup"><span data-stu-id="b3de2-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="b3de2-113">Mit diesem Befehl wird eine Konfiguration von "Kubernetes Cluster nach Objekt" entfernt.</span><span class="sxs-lookup"><span data-stu-id="b3de2-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="b3de2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3de2-114">PARAMETERS</span></span>

### <span data-ttu-id="b3de2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3de2-115">-AsJob</span></span>
<span data-ttu-id="b3de2-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b3de2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3de2-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b3de2-117">-ClusterName</span></span>
<span data-ttu-id="b3de2-118">Der Name des Kubernetenclusters.</span><span class="sxs-lookup"><span data-stu-id="b3de2-118">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3de2-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="b3de2-119">-ClusterType</span></span>
<span data-ttu-id="b3de2-120">Der Ressourcenname des Kubernetes-Clusters – entweder managedClusters (für AKS-Cluster) oder verbundene Cluster (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="b3de2-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3de2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3de2-121">-DefaultProfile</span></span>
<span data-ttu-id="b3de2-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3de2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3de2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3de2-123">-InputObject</span></span>
<span data-ttu-id="b3de2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b3de2-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3de2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b3de2-125">-Name</span></span>
<span data-ttu-id="b3de2-126">Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b3de2-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3de2-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3de2-127">-NoWait</span></span>
<span data-ttu-id="b3de2-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b3de2-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3de2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3de2-129">-PassThru</span></span>
<span data-ttu-id="b3de2-130">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b3de2-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3de2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3de2-131">-ResourceGroupName</span></span>
<span data-ttu-id="b3de2-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3de2-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3de2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3de2-133">-SubscriptionId</span></span>
<span data-ttu-id="b3de2-134">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b3de2-134">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3de2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3de2-135">-Confirm</span></span>
<span data-ttu-id="b3de2-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3de2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3de2-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b3de2-137">-WhatIf</span></span>
<span data-ttu-id="b3de2-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3de2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3de2-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3de2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3de2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3de2-140">CommonParameters</span></span>
<span data-ttu-id="b3de2-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3de2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3de2-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3de2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3de2-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3de2-143">INPUTS</span></span>

### <span data-ttu-id="b3de2-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IAkiernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="b3de2-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="b3de2-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3de2-145">OUTPUTS</span></span>

### <span data-ttu-id="b3de2-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3de2-146">System.Boolean</span></span>

## <span data-ttu-id="b3de2-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3de2-147">NOTES</span></span>

<span data-ttu-id="b3de2-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b3de2-148">ALIASES</span></span>

<span data-ttu-id="b3de2-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b3de2-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3de2-150">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3de2-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3de2-151">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3de2-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3de2-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b3de2-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3de2-153">`[ClusterName <String>]`: Der Name des Kubernetclusters.</span><span class="sxs-lookup"><span data-stu-id="b3de2-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="b3de2-154">`[ClusterResourceName <String>]`: Der Name der Clusterressource "Kubernetes" – entweder "managedClusters" (für AKS-Cluster) oder "connectedClusters" (für "OnPrem K8S"-Cluster).</span><span class="sxs-lookup"><span data-stu-id="b3de2-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b3de2-155">`[ClusterRp <String>]`: Der Kubernetes-Cluster-RP – entweder Microsoft.ContainerService (für AKS-Cluster) oder Microsoft.Kubernetes (für OnPrem K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="b3de2-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="b3de2-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b3de2-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3de2-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b3de2-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b3de2-158">`[SourceControlConfigurationName <String>]`: Name der Quellcodeverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="b3de2-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="b3de2-159">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b3de2-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b3de2-160">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="b3de2-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b3de2-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3de2-161">RELATED LINKS</span></span>

