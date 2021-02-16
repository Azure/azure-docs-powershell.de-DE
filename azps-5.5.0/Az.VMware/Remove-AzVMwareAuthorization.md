---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Remove-AzVMwareAuthorization.md
ms.openlocfilehash: 39a6f251cd0cfb190ea8541f5b04c35d710de2c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164481"
---
# <span data-ttu-id="224a3-101">Remove-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="224a3-101">Remove-AzVMwareAuthorization</span></span>

## <span data-ttu-id="224a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="224a3-102">SYNOPSIS</span></span>
<span data-ttu-id="224a3-103">Löschen einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="224a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="224a3-104">SYNTAX</span></span>

### <span data-ttu-id="224a3-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="224a3-105">Delete (Default)</span></span>
```
Remove-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="224a3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="224a3-106">DeleteViaIdentity</span></span>
```
Remove-AzVMwareAuthorization -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="224a3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="224a3-107">DESCRIPTION</span></span>
<span data-ttu-id="224a3-108">Löschen einer ExpressRoute-Schaltkreisautorisierung in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="224a3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="224a3-109">EXAMPLES</span></span>

### <span data-ttu-id="224a3-110">Beispiel 1: Löschen der Autorisierung für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="224a3-111">Löschen der Autorisierung für die private Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="224a3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="224a3-112">PARAMETERS</span></span>

### <span data-ttu-id="224a3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="224a3-113">-AsJob</span></span>
<span data-ttu-id="224a3-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="224a3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="224a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224a3-115">-DefaultProfile</span></span>
<span data-ttu-id="224a3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="224a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="224a3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="224a3-117">-InputObject</span></span>
<span data-ttu-id="224a3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="224a3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="224a3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="224a3-119">-Name</span></span>
<span data-ttu-id="224a3-120">Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="224a3-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="224a3-121">-NoWait</span></span>
<span data-ttu-id="224a3-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="224a3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="224a3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="224a3-123">-PassThru</span></span>
<span data-ttu-id="224a3-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="224a3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="224a3-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="224a3-125">-PrivateCloudName</span></span>
<span data-ttu-id="224a3-126">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="224a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="224a3-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="224a3-128">The name of the resource group.</span></span>
<span data-ttu-id="224a3-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="224a3-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="224a3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="224a3-130">-SubscriptionId</span></span>
<span data-ttu-id="224a3-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="224a3-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="224a3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="224a3-132">-Confirm</span></span>
<span data-ttu-id="224a3-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="224a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="224a3-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="224a3-134">-WhatIf</span></span>
<span data-ttu-id="224a3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="224a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="224a3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="224a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="224a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224a3-137">CommonParameters</span></span>
<span data-ttu-id="224a3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="224a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224a3-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="224a3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224a3-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="224a3-140">INPUTS</span></span>

### <span data-ttu-id="224a3-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="224a3-141">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="224a3-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="224a3-142">OUTPUTS</span></span>

### <span data-ttu-id="224a3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="224a3-143">System.Boolean</span></span>

## <span data-ttu-id="224a3-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="224a3-144">NOTES</span></span>

<span data-ttu-id="224a3-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="224a3-145">ALIASES</span></span>

<span data-ttu-id="224a3-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="224a3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="224a3-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="224a3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="224a3-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="224a3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="224a3-149">INPUTOBJECT <IVMwareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="224a3-149">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="224a3-150">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="224a3-151">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="224a3-152">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="224a3-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="224a3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="224a3-154">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="224a3-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="224a3-155">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="224a3-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="224a3-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="224a3-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="224a3-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="224a3-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="224a3-158">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="224a3-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="224a3-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="224a3-159">RELATED LINKS</span></span>

