---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165863"
---
# <span data-ttu-id="19ac6-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="19ac6-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="19ac6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="19ac6-103">Löschen eines verbundenen Clusters und Entfernen der nachverfolgten Ressource im Azure Resource Manager (Arm).</span><span class="sxs-lookup"><span data-stu-id="19ac6-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="19ac6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ac6-104">SYNTAX</span></span>

### <span data-ttu-id="19ac6-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="19ac6-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19ac6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19ac6-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="19ac6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19ac6-107">DESCRIPTION</span></span>
<span data-ttu-id="19ac6-108">Löschen eines verbundenen Clusters und Entfernen der nachverfolgten Ressource im Azure Resource Manager (Arm).</span><span class="sxs-lookup"><span data-stu-id="19ac6-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="19ac6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19ac6-109">EXAMPLES</span></span>

### <span data-ttu-id="19ac6-110">Beispiel 1: Entfernen einer verbundenen kubernetes</span><span class="sxs-lookup"><span data-stu-id="19ac6-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="19ac6-111">Dieser Befehl entfernt eine verbundene kubernetes</span><span class="sxs-lookup"><span data-stu-id="19ac6-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="19ac6-112">Beispiel 2: Entfernen einer verbundenen kubernetes nach Objekt</span><span class="sxs-lookup"><span data-stu-id="19ac6-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="19ac6-113">Dieser Befehl entfernt eine verbundene kubernetes nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="19ac6-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="19ac6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ac6-114">PARAMETERS</span></span>

### <span data-ttu-id="19ac6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19ac6-115">-AsJob</span></span>
<span data-ttu-id="19ac6-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="19ac6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="19ac6-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="19ac6-117">-ClusterName</span></span>
<span data-ttu-id="19ac6-118">Der Name des Kubernetes-Clusters, in dem Get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="19ac6-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="19ac6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ac6-119">-DefaultProfile</span></span>
<span data-ttu-id="19ac6-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19ac6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19ac6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19ac6-121">-InputObject</span></span>
<span data-ttu-id="19ac6-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="19ac6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19ac6-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="19ac6-123">-KubeConfig</span></span>
<span data-ttu-id="19ac6-124">Pfad zur Datei "Kuben-Konfiguration"</span><span class="sxs-lookup"><span data-stu-id="19ac6-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="19ac6-125">-Kubencontext</span><span class="sxs-lookup"><span data-stu-id="19ac6-125">-KubeContext</span></span>
<span data-ttu-id="19ac6-126">Kubconfig-Kontext vom aktuellen Computer</span><span class="sxs-lookup"><span data-stu-id="19ac6-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="19ac6-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="19ac6-127">-NoWait</span></span>
<span data-ttu-id="19ac6-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="19ac6-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19ac6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19ac6-129">-PassThru</span></span>
<span data-ttu-id="19ac6-130">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="19ac6-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19ac6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19ac6-131">-ResourceGroupName</span></span>
<span data-ttu-id="19ac6-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="19ac6-132">The name of the resource group.</span></span>
<span data-ttu-id="19ac6-133">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="19ac6-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="19ac6-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="19ac6-134">-SubscriptionId</span></span>
<span data-ttu-id="19ac6-135">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="19ac6-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="19ac6-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19ac6-136">-Confirm</span></span>
<span data-ttu-id="19ac6-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19ac6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ac6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ac6-138">-WhatIf</span></span>
<span data-ttu-id="19ac6-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19ac6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ac6-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19ac6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ac6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ac6-141">CommonParameters</span></span>
<span data-ttu-id="19ac6-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ac6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ac6-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19ac6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ac6-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19ac6-144">INPUTS</span></span>

### <span data-ttu-id="19ac6-145">Microsoft. Azure. PowerShell. Cmdlets. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="19ac6-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="19ac6-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19ac6-146">OUTPUTS</span></span>

### <span data-ttu-id="19ac6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19ac6-147">System.Boolean</span></span>

## <span data-ttu-id="19ac6-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="19ac6-148">NOTES</span></span>

<span data-ttu-id="19ac6-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="19ac6-149">ALIASES</span></span>

<span data-ttu-id="19ac6-150">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19ac6-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19ac6-151">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19ac6-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19ac6-152">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="19ac6-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19ac6-153">Inputobject <IConnectedKubernetesIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="19ac6-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19ac6-154">`[ClusterName <String>]`: Der Name des Kubernetes-Clusters, in dem Get aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="19ac6-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="19ac6-155">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="19ac6-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19ac6-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="19ac6-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="19ac6-157">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="19ac6-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="19ac6-158">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="19ac6-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="19ac6-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19ac6-159">RELATED LINKS</span></span>

