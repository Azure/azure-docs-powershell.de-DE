---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 7abbe244e702c80f18d2c9e97236f74d60f094bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948856"
---
# <span data-ttu-id="fb131-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="fb131-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="fb131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb131-102">SYNOPSIS</span></span>
<span data-ttu-id="fb131-103">Löschen Sie einen verbundenen Cluster, und entfernen Sie die nachverfolgte Ressource in Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="fb131-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="fb131-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb131-104">SYNTAX</span></span>

### <span data-ttu-id="fb131-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb131-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fb131-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fb131-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fb131-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb131-107">DESCRIPTION</span></span>
<span data-ttu-id="fb131-108">Löschen Sie einen verbundenen Cluster, und entfernen Sie die nachverfolgte Ressource in Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="fb131-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="fb131-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fb131-109">EXAMPLES</span></span>

### <span data-ttu-id="fb131-110">Beispiel 1: Entfernen eines verbundenen Kubernetes</span><span class="sxs-lookup"><span data-stu-id="fb131-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="fb131-111">Mit diesem Befehl werden verbundene Kubernetes entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb131-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="fb131-112">Beispiel 2: Entfernen eines verbundenen Kubernetes nach Objekt</span><span class="sxs-lookup"><span data-stu-id="fb131-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="fb131-113">Mit diesem Befehl wird ein verbundenes Kubernetes nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="fb131-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="fb131-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fb131-114">PARAMETERS</span></span>

### <span data-ttu-id="fb131-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb131-115">-AsJob</span></span>
<span data-ttu-id="fb131-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb131-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fb131-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fb131-117">-ClusterName</span></span>
<span data-ttu-id="fb131-118">Der Name des Kubernetes-Clusters, für den get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fb131-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="fb131-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb131-119">-DefaultProfile</span></span>
<span data-ttu-id="fb131-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb131-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb131-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb131-121">-InputObject</span></span>
<span data-ttu-id="fb131-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="fb131-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fb131-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="fb131-123">-KubeConfig</span></span>
<span data-ttu-id="fb131-124">Pfad zur Kube-Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="fb131-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="fb131-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="fb131-125">-KubeContext</span></span>
<span data-ttu-id="fb131-126">Kubconfig-Kontext vom aktuellen Computer</span><span class="sxs-lookup"><span data-stu-id="fb131-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="fb131-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fb131-127">-NoWait</span></span>
<span data-ttu-id="fb131-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fb131-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fb131-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb131-129">-PassThru</span></span>
<span data-ttu-id="fb131-130">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb131-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fb131-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb131-131">-ResourceGroupName</span></span>
<span data-ttu-id="fb131-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fb131-132">The name of the resource group.</span></span>
<span data-ttu-id="fb131-133">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="fb131-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb131-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb131-134">-SubscriptionId</span></span>
<span data-ttu-id="fb131-135">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="fb131-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb131-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb131-136">-Confirm</span></span>
<span data-ttu-id="fb131-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb131-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb131-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb131-138">-WhatIf</span></span>
<span data-ttu-id="fb131-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb131-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb131-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb131-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb131-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb131-141">CommonParameters</span></span>
<span data-ttu-id="fb131-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb131-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb131-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb131-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb131-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fb131-144">INPUTS</span></span>

### <span data-ttu-id="fb131-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="fb131-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="fb131-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fb131-146">OUTPUTS</span></span>

### <span data-ttu-id="fb131-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb131-147">System.Boolean</span></span>

## <span data-ttu-id="fb131-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fb131-148">NOTES</span></span>

<span data-ttu-id="fb131-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fb131-149">ALIASES</span></span>

<span data-ttu-id="fb131-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="fb131-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fb131-151">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="fb131-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fb131-152">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fb131-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fb131-153">INPUTOBJECT <IConnectedKubernetesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="fb131-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fb131-154">`[ClusterName <String>]`: Der Name des Kubernetes-Clusters, für den get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fb131-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="fb131-155">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="fb131-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fb131-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fb131-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fb131-157">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="fb131-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="fb131-158">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="fb131-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="fb131-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fb131-159">RELATED LINKS</span></span>

