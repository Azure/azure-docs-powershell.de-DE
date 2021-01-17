---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460511"
---
# <span data-ttu-id="876d8-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="876d8-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="876d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876d8-102">SYNOPSIS</span></span>
<span data-ttu-id="876d8-103">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-103">Delete a private cloud</span></span>

## <span data-ttu-id="876d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="876d8-104">SYNTAX</span></span>

### <span data-ttu-id="876d8-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="876d8-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="876d8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="876d8-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="876d8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="876d8-107">DESCRIPTION</span></span>
<span data-ttu-id="876d8-108">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-108">Delete a private cloud</span></span>

## <span data-ttu-id="876d8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="876d8-109">EXAMPLES</span></span>

### <span data-ttu-id="876d8-110">Beispiel 1: Löschen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="876d8-111">Löschen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-111">Delete private cloud</span></span>

## <span data-ttu-id="876d8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="876d8-112">PARAMETERS</span></span>

### <span data-ttu-id="876d8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="876d8-113">-AsJob</span></span>
<span data-ttu-id="876d8-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="876d8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="876d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876d8-115">-DefaultProfile</span></span>
<span data-ttu-id="876d8-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="876d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="876d8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="876d8-117">-InputObject</span></span>
<span data-ttu-id="876d8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="876d8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="876d8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="876d8-119">-Name</span></span>
<span data-ttu-id="876d8-120">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876d8-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="876d8-121">-NoWait</span></span>
<span data-ttu-id="876d8-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="876d8-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="876d8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="876d8-123">-PassThru</span></span>
<span data-ttu-id="876d8-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="876d8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="876d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="876d8-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="876d8-126">The name of the resource group.</span></span>
<span data-ttu-id="876d8-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="876d8-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="876d8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="876d8-128">-SubscriptionId</span></span>
<span data-ttu-id="876d8-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="876d8-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="876d8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="876d8-130">-Confirm</span></span>
<span data-ttu-id="876d8-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="876d8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="876d8-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="876d8-132">-WhatIf</span></span>
<span data-ttu-id="876d8-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="876d8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="876d8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="876d8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="876d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876d8-135">CommonParameters</span></span>
<span data-ttu-id="876d8-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876d8-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="876d8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876d8-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="876d8-138">INPUTS</span></span>

### <span data-ttu-id="876d8-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="876d8-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="876d8-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="876d8-140">OUTPUTS</span></span>

### <span data-ttu-id="876d8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="876d8-141">System.Boolean</span></span>

## <span data-ttu-id="876d8-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="876d8-142">NOTES</span></span>

<span data-ttu-id="876d8-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="876d8-143">ALIASES</span></span>

<span data-ttu-id="876d8-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="876d8-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="876d8-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="876d8-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="876d8-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="876d8-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="876d8-147">INPUTOBJECT <IVMWareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="876d8-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="876d8-148">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="876d8-149">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="876d8-150">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="876d8-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="876d8-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="876d8-152">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="876d8-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="876d8-153">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="876d8-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="876d8-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="876d8-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="876d8-155">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="876d8-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="876d8-156">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="876d8-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="876d8-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="876d8-157">RELATED LINKS</span></span>

