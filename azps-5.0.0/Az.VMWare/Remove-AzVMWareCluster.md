---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301666"
---
# <span data-ttu-id="546b9-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="546b9-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="546b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="546b9-102">SYNOPSIS</span></span>
<span data-ttu-id="546b9-103">Löschen eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="546b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="546b9-104">SYNTAX</span></span>

### <span data-ttu-id="546b9-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="546b9-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="546b9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="546b9-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="546b9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="546b9-107">DESCRIPTION</span></span>
<span data-ttu-id="546b9-108">Löschen eines Clusters in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="546b9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="546b9-109">EXAMPLES</span></span>

### <span data-ttu-id="546b9-110">Beispiel 1: Löschen eines Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="546b9-111">Löschen eines Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="546b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="546b9-112">PARAMETERS</span></span>

### <span data-ttu-id="546b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="546b9-113">-AsJob</span></span>
<span data-ttu-id="546b9-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="546b9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="546b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546b9-115">-DefaultProfile</span></span>
<span data-ttu-id="546b9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="546b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="546b9-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="546b9-117">-InputObject</span></span>
<span data-ttu-id="546b9-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="546b9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="546b9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="546b9-119">-Name</span></span>
<span data-ttu-id="546b9-120">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546b9-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="546b9-121">-NoWait</span></span>
<span data-ttu-id="546b9-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="546b9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="546b9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="546b9-123">-PassThru</span></span>
<span data-ttu-id="546b9-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="546b9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="546b9-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="546b9-125">-PrivateCloudName</span></span>
<span data-ttu-id="546b9-126">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="546b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="546b9-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="546b9-128">The name of the resource group.</span></span>
<span data-ttu-id="546b9-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="546b9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="546b9-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="546b9-130">-SubscriptionId</span></span>
<span data-ttu-id="546b9-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="546b9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="546b9-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="546b9-132">-Confirm</span></span>
<span data-ttu-id="546b9-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="546b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="546b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="546b9-134">-WhatIf</span></span>
<span data-ttu-id="546b9-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="546b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="546b9-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="546b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="546b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546b9-137">CommonParameters</span></span>
<span data-ttu-id="546b9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="546b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546b9-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="546b9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546b9-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="546b9-140">INPUTS</span></span>

### <span data-ttu-id="546b9-141">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="546b9-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="546b9-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="546b9-142">OUTPUTS</span></span>

### <span data-ttu-id="546b9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="546b9-143">System.Boolean</span></span>

## <span data-ttu-id="546b9-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="546b9-144">NOTES</span></span>

<span data-ttu-id="546b9-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="546b9-145">ALIASES</span></span>

<span data-ttu-id="546b9-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="546b9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="546b9-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="546b9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="546b9-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="546b9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="546b9-149">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="546b9-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="546b9-150">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="546b9-151">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="546b9-152">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="546b9-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="546b9-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="546b9-154">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="546b9-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="546b9-155">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="546b9-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="546b9-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="546b9-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="546b9-157">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="546b9-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="546b9-158">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="546b9-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="546b9-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="546b9-159">RELATED LINKS</span></span>

