---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290020"
---
# <span data-ttu-id="a3615-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="a3615-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="a3615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3615-102">SYNOPSIS</span></span>
<span data-ttu-id="a3615-103">Löschen Sie einen verbundenen Cluster, und entfernen Sie die nachverfolgte Ressource in Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="a3615-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="a3615-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3615-104">SYNTAX</span></span>

### <span data-ttu-id="a3615-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3615-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3615-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3615-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a3615-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3615-107">DESCRIPTION</span></span>
<span data-ttu-id="a3615-108">Löschen Sie einen verbundenen Cluster, und entfernen Sie die nachverfolgte Ressource in Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="a3615-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="a3615-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3615-109">EXAMPLES</span></span>

### <span data-ttu-id="a3615-110">Beispiel 1: Entfernen eines verbundenen Kubernets</span><span class="sxs-lookup"><span data-stu-id="a3615-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="a3615-111">Mit diesem Befehl wird ein verbundenes Kubernets entfernt.</span><span class="sxs-lookup"><span data-stu-id="a3615-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="a3615-112">Beispiel 2: Entfernen eines verbundenen Kubernets nach Objekt</span><span class="sxs-lookup"><span data-stu-id="a3615-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="a3615-113">Mit diesem Befehl wird ein verbundenes Kubernetes nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a3615-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="a3615-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3615-114">PARAMETERS</span></span>

### <span data-ttu-id="a3615-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3615-115">-AsJob</span></span>
<span data-ttu-id="a3615-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a3615-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a3615-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a3615-117">-ClusterName</span></span>
<span data-ttu-id="a3615-118">Der Name des Kubernetes-Cluster, für den "get" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a3615-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3615-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3615-119">-DefaultProfile</span></span>
<span data-ttu-id="a3615-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3615-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3615-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3615-121">-InputObject</span></span>
<span data-ttu-id="a3615-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a3615-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3615-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="a3615-123">-KubeConfig</span></span>
<span data-ttu-id="a3615-124">Pfad zur Konfigurationsdatei "kube"</span><span class="sxs-lookup"><span data-stu-id="a3615-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="a3615-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="a3615-125">-KubeContext</span></span>
<span data-ttu-id="a3615-126">Kontext "Kubconfig" vom aktuellen Computer</span><span class="sxs-lookup"><span data-stu-id="a3615-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="a3615-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a3615-127">-NoWait</span></span>
<span data-ttu-id="a3615-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a3615-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a3615-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3615-129">-PassThru</span></span>
<span data-ttu-id="a3615-130">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a3615-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a3615-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3615-131">-ResourceGroupName</span></span>
<span data-ttu-id="a3615-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3615-132">The name of the resource group.</span></span>
<span data-ttu-id="a3615-133">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a3615-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a3615-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3615-134">-SubscriptionId</span></span>
<span data-ttu-id="a3615-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a3615-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a3615-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3615-136">-Confirm</span></span>
<span data-ttu-id="a3615-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3615-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3615-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a3615-138">-WhatIf</span></span>
<span data-ttu-id="a3615-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3615-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3615-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3615-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3615-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3615-141">CommonParameters</span></span>
<span data-ttu-id="a3615-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3615-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3615-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3615-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3615-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3615-144">INPUTS</span></span>

### <span data-ttu-id="a3615-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedConnecternetes.Models.IConnectedKoppelernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="a3615-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="a3615-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3615-146">OUTPUTS</span></span>

### <span data-ttu-id="a3615-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3615-147">System.Boolean</span></span>

## <span data-ttu-id="a3615-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3615-148">NOTES</span></span>

<span data-ttu-id="a3615-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a3615-149">ALIASES</span></span>

<span data-ttu-id="a3615-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a3615-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3615-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a3615-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3615-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3615-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3615-153">INPUTOBJECT <IConnectedKubernetesIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a3615-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3615-154">`[ClusterName <String>]`: Der Name des Kubernetes-Cluster, für den "get" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a3615-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="a3615-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a3615-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3615-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3615-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a3615-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a3615-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="a3615-158">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a3615-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="a3615-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3615-159">RELATED LINKS</span></span>

