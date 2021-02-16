---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 8d44cc541cf44e03e2946ce428eb96c2f902bf84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162348"
---
# <span data-ttu-id="a267b-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a267b-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="a267b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a267b-102">SYNOPSIS</span></span>
<span data-ttu-id="a267b-103">Löscht Rolleninstanzen in einem Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="a267b-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="a267b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a267b-104">SYNTAX</span></span>

### <span data-ttu-id="a267b-105">DeleteExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a267b-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a267b-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a267b-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a267b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a267b-107">DESCRIPTION</span></span>
<span data-ttu-id="a267b-108">Löscht Rolleninstanzen in einem Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="a267b-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="a267b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a267b-109">EXAMPLES</span></span>

### <span data-ttu-id="a267b-110">Beispiel 1: Entfernen einer Clouddienstrolleinstanz</span><span class="sxs-lookup"><span data-stu-id="a267b-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="a267b-111">Mit diesem Befehl wird die Rolleninstanz namens ContosoFrontEnd_IN_0 des Clouddiensts "ContosoCS" entfernt, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="a267b-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a267b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a267b-112">PARAMETERS</span></span>

### <span data-ttu-id="a267b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a267b-113">-AsJob</span></span>
<span data-ttu-id="a267b-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a267b-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a267b-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="a267b-115">-CloudServiceName</span></span>
<span data-ttu-id="a267b-116">Der Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="a267b-116">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a267b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a267b-117">-DefaultProfile</span></span>
<span data-ttu-id="a267b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a267b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a267b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a267b-119">-InputObject</span></span>
<span data-ttu-id="a267b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a267b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a267b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a267b-121">-NoWait</span></span>
<span data-ttu-id="a267b-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a267b-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a267b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a267b-123">-PassThru</span></span>
<span data-ttu-id="a267b-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a267b-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a267b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a267b-125">-ResourceGroupName</span></span>
<span data-ttu-id="a267b-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a267b-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a267b-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="a267b-127">-RoleInstance</span></span>
<span data-ttu-id="a267b-128">Liste der Namen der Clouddienst-Rolleninstanzen.</span><span class="sxs-lookup"><span data-stu-id="a267b-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="a267b-129">Der Wert "\*" bedeutet alle Rolleninstanzen des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="a267b-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a267b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a267b-130">-SubscriptionId</span></span>
<span data-ttu-id="a267b-131">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a267b-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a267b-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a267b-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a267b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a267b-133">-Confirm</span></span>
<span data-ttu-id="a267b-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a267b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a267b-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a267b-135">-WhatIf</span></span>
<span data-ttu-id="a267b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a267b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a267b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a267b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a267b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a267b-138">CommonParameters</span></span>
<span data-ttu-id="a267b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a267b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a267b-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a267b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a267b-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a267b-141">INPUTS</span></span>

### <span data-ttu-id="a267b-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a267b-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="a267b-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a267b-143">OUTPUTS</span></span>

### <span data-ttu-id="a267b-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a267b-144">System.Boolean</span></span>

## <span data-ttu-id="a267b-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a267b-145">NOTES</span></span>

<span data-ttu-id="a267b-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a267b-146">ALIASES</span></span>

<span data-ttu-id="a267b-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a267b-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a267b-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a267b-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a267b-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a267b-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a267b-150">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a267b-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a267b-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a267b-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="a267b-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a267b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a267b-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a267b-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="a267b-154">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="a267b-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="a267b-155">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="a267b-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="a267b-156">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a267b-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a267b-157">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a267b-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a267b-158">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a267b-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="a267b-159">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="a267b-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="a267b-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a267b-160">RELATED LINKS</span></span>

