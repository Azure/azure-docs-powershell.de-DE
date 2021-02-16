---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwarePrivateCloud.md
ms.openlocfilehash: 76ad6df6dbbd9b019e4c89fdbca55107264f0406
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173441"
---
# <span data-ttu-id="52b61-101">Remove-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="52b61-101">Remove-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="52b61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b61-102">SYNOPSIS</span></span>
<span data-ttu-id="52b61-103">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-103">Delete a private cloud</span></span>

## <span data-ttu-id="52b61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52b61-104">SYNTAX</span></span>

### <span data-ttu-id="52b61-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="52b61-105">Delete (Default)</span></span>
```
Remove-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="52b61-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52b61-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52b61-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52b61-107">DESCRIPTION</span></span>
<span data-ttu-id="52b61-108">Löschen einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-108">Delete a private cloud</span></span>

## <span data-ttu-id="52b61-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52b61-109">EXAMPLES</span></span>

### <span data-ttu-id="52b61-110">Beispiel 1: Löschen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="52b61-111">Löschen der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-111">Delete private cloud</span></span>

## <span data-ttu-id="52b61-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52b61-112">PARAMETERS</span></span>

### <span data-ttu-id="52b61-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52b61-113">-AsJob</span></span>
<span data-ttu-id="52b61-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="52b61-114">Run the command as a job</span></span>

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

### <span data-ttu-id="52b61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b61-115">-DefaultProfile</span></span>
<span data-ttu-id="52b61-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52b61-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b61-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52b61-117">-InputObject</span></span>
<span data-ttu-id="52b61-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="52b61-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b61-119">-Name</span><span class="sxs-lookup"><span data-stu-id="52b61-119">-Name</span></span>
<span data-ttu-id="52b61-120">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-120">Name of the private cloud</span></span>

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

### <span data-ttu-id="52b61-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="52b61-121">-NoWait</span></span>
<span data-ttu-id="52b61-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="52b61-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52b61-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52b61-123">-PassThru</span></span>
<span data-ttu-id="52b61-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="52b61-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="52b61-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b61-125">-ResourceGroupName</span></span>
<span data-ttu-id="52b61-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="52b61-126">The name of the resource group.</span></span>
<span data-ttu-id="52b61-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="52b61-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="52b61-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52b61-128">-SubscriptionId</span></span>
<span data-ttu-id="52b61-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="52b61-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="52b61-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52b61-130">-Confirm</span></span>
<span data-ttu-id="52b61-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52b61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52b61-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="52b61-132">-WhatIf</span></span>
<span data-ttu-id="52b61-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52b61-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b61-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52b61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52b61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b61-135">CommonParameters</span></span>
<span data-ttu-id="52b61-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b61-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52b61-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b61-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52b61-138">INPUTS</span></span>

### <span data-ttu-id="52b61-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="52b61-139">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="52b61-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52b61-140">OUTPUTS</span></span>

### <span data-ttu-id="52b61-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52b61-141">System.Boolean</span></span>

## <span data-ttu-id="52b61-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="52b61-142">NOTES</span></span>

<span data-ttu-id="52b61-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="52b61-143">ALIASES</span></span>

<span data-ttu-id="52b61-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="52b61-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52b61-145">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52b61-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52b61-146">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52b61-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52b61-147">INPUTOBJECT <IVMwareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="52b61-147">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52b61-148">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="52b61-149">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="52b61-150">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="52b61-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="52b61-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52b61-152">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="52b61-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="52b61-153">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="52b61-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="52b61-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="52b61-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="52b61-155">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="52b61-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="52b61-156">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="52b61-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="52b61-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="52b61-157">RELATED LINKS</span></span>

