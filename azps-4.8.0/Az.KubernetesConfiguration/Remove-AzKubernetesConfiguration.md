---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166567"
---
# <span data-ttu-id="6bead-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bead-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="6bead-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6bead-102">SYNOPSIS</span></span>
<span data-ttu-id="6bead-103">Dadurch wird die YAML-Datei gelöscht, die zum Einrichten der Quellcodeverwaltungs-Konfiguration verwendet wird, wodurch die zukünftige Synchronisierung aus dem Quell-Repo gestoppt wird.</span><span class="sxs-lookup"><span data-stu-id="6bead-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="6bead-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bead-104">SYNTAX</span></span>

### <span data-ttu-id="6bead-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6bead-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6bead-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6bead-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6bead-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6bead-107">DESCRIPTION</span></span>
<span data-ttu-id="6bead-108">Dadurch wird die YAML-Datei gelöscht, die zum Einrichten der Quellcodeverwaltungs-Konfiguration verwendet wird, wodurch die zukünftige Synchronisierung aus dem Quell-Repo gestoppt wird.</span><span class="sxs-lookup"><span data-stu-id="6bead-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="6bead-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6bead-109">EXAMPLES</span></span>

### <span data-ttu-id="6bead-110">Beispiel 1: Entfernen eines Konfigurations des kubernetes-Clusters nach Name</span><span class="sxs-lookup"><span data-stu-id="6bead-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="6bead-111">Mit diesem Befehl wird ein Konfigurations des kubernetes-Clusters nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="6bead-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="6bead-112">Beispiel 2: Entfernen eines Konfigurations des kubernetes-Clusters nach Objekt</span><span class="sxs-lookup"><span data-stu-id="6bead-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="6bead-113">Dieser Befehl entfernt eine Konfigurations des kubernetes-Clusters nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="6bead-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="6bead-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bead-114">PARAMETERS</span></span>

### <span data-ttu-id="6bead-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bead-115">-AsJob</span></span>
<span data-ttu-id="6bead-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6bead-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6bead-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6bead-117">-ClusterName</span></span>
<span data-ttu-id="6bead-118">Der Name des kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="6bead-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="6bead-119">-Clustertyp</span><span class="sxs-lookup"><span data-stu-id="6bead-119">-ClusterType</span></span>
<span data-ttu-id="6bead-120">Der Kubernetes-Clusterressourcen Name – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="6bead-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="6bead-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bead-121">-DefaultProfile</span></span>
<span data-ttu-id="6bead-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6bead-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bead-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6bead-123">-InputObject</span></span>
<span data-ttu-id="6bead-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6bead-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6bead-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6bead-125">-Name</span></span>
<span data-ttu-id="6bead-126">Der Name der Quell Code Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6bead-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="6bead-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6bead-127">-NoWait</span></span>
<span data-ttu-id="6bead-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6bead-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6bead-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bead-129">-PassThru</span></span>
<span data-ttu-id="6bead-130">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="6bead-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6bead-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bead-131">-ResourceGroupName</span></span>
<span data-ttu-id="6bead-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6bead-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="6bead-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6bead-133">-SubscriptionId</span></span>
<span data-ttu-id="6bead-134">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6bead-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="6bead-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6bead-135">-Confirm</span></span>
<span data-ttu-id="6bead-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bead-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bead-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bead-137">-WhatIf</span></span>
<span data-ttu-id="6bead-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bead-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bead-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bead-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bead-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bead-140">CommonParameters</span></span>
<span data-ttu-id="6bead-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bead-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bead-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bead-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bead-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6bead-143">INPUTS</span></span>

### <span data-ttu-id="6bead-144">Microsoft. Azure. PowerShell. Cmdlets. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="6bead-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="6bead-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6bead-145">OUTPUTS</span></span>

### <span data-ttu-id="6bead-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6bead-146">System.Boolean</span></span>

## <span data-ttu-id="6bead-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="6bead-147">NOTES</span></span>

<span data-ttu-id="6bead-148">Aliase</span><span class="sxs-lookup"><span data-stu-id="6bead-148">ALIASES</span></span>

<span data-ttu-id="6bead-149">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6bead-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6bead-150">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6bead-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6bead-151">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="6bead-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6bead-152">Inputobject <IKubernetesConfigurationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="6bead-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6bead-153">`[ClusterName <String>]`: Der Name des kubernetes-Clusters.</span><span class="sxs-lookup"><span data-stu-id="6bead-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="6bead-154">`[ClusterResourceName <String>]`: Der Kubernetes-Clusterressourcen Name – entweder managedClusters (für AKS-Cluster) oder connectedClusters (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="6bead-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="6bead-155">`[ClusterRp <String>]`: Kubernetes-Cluster RP – entweder Microsoft. ContainerService (für AKS-Cluster) oder Microsoft. Kubernetes (für onprem-K8S-Cluster).</span><span class="sxs-lookup"><span data-stu-id="6bead-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="6bead-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="6bead-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6bead-157">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6bead-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6bead-158">`[SourceControlConfigurationName <String>]`: Name der Quell Code Verwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="6bead-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="6bead-159">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6bead-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6bead-160">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="6bead-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6bead-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6bead-161">RELATED LINKS</span></span>

