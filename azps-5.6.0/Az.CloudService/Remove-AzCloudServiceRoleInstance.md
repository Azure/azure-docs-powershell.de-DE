---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 5a29444c5f6d05ddbf614e86cd13af6818d24d79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920843"
---
# <span data-ttu-id="f0c71-101">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="f0c71-101">Remove-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="f0c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c71-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c71-103">Löscht Rolleninstanzen in einem Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="f0c71-103">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="f0c71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0c71-104">SYNTAX</span></span>

### <span data-ttu-id="f0c71-105">DeleteExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0c71-105">DeleteExpanded (Default)</span></span>
```
Remove-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstance <String[]> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f0c71-106">DeleteViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f0c71-106">DeleteViaIdentityExpanded</span></span>
```
Remove-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0c71-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0c71-107">DESCRIPTION</span></span>
<span data-ttu-id="f0c71-108">Löscht Rolleninstanzen in einem Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="f0c71-108">Deletes role instances in a cloud service.</span></span>

## <span data-ttu-id="f0c71-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0c71-109">EXAMPLES</span></span>

### <span data-ttu-id="f0c71-110">Beispiel 1: Entfernen einer Clouddienstrolleinstanz</span><span class="sxs-lookup"><span data-stu-id="f0c71-110">Example 1: Remove a cloud service role instance</span></span>
```powershell
PS C:\> Remove-AzCloudServiceInstance -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="f0c71-111">Mit diesem Befehl wird die Rolleninstanz ContosoFrontEnd_IN_0 des Clouddiensts ContosoCS entfernt, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="f0c71-111">This command removes the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="f0c71-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0c71-112">PARAMETERS</span></span>

### <span data-ttu-id="f0c71-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0c71-113">-AsJob</span></span>
<span data-ttu-id="f0c71-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f0c71-114">Run the command as a job</span></span>

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

### <span data-ttu-id="f0c71-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f0c71-115">-CloudServiceName</span></span>
<span data-ttu-id="f0c71-116">Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="f0c71-116">Name of the cloud service.</span></span>

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

### <span data-ttu-id="f0c71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c71-117">-DefaultProfile</span></span>
<span data-ttu-id="f0c71-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0c71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c71-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0c71-119">-InputObject</span></span>
<span data-ttu-id="f0c71-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f0c71-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0c71-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f0c71-121">-NoWait</span></span>
<span data-ttu-id="f0c71-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f0c71-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f0c71-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0c71-123">-PassThru</span></span>
<span data-ttu-id="f0c71-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0c71-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f0c71-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c71-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0c71-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0c71-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="f0c71-127">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="f0c71-127">-RoleInstance</span></span>
<span data-ttu-id="f0c71-128">Liste der Namen der Rolleninstanznamen des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="f0c71-128">List of cloud service role instance names.</span></span>
<span data-ttu-id="f0c71-129">Der Wert "\*" bedeutet alle Rolleninstanzen des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="f0c71-129">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="f0c71-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f0c71-130">-SubscriptionId</span></span>
<span data-ttu-id="f0c71-131">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f0c71-131">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f0c71-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="f0c71-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f0c71-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0c71-133">-Confirm</span></span>
<span data-ttu-id="f0c71-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0c71-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c71-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c71-135">-WhatIf</span></span>
<span data-ttu-id="f0c71-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0c71-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c71-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0c71-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c71-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c71-138">CommonParameters</span></span>
<span data-ttu-id="f0c71-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c71-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c71-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0c71-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c71-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0c71-141">INPUTS</span></span>

### <span data-ttu-id="f0c71-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f0c71-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="f0c71-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0c71-143">OUTPUTS</span></span>

### <span data-ttu-id="f0c71-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0c71-144">System.Boolean</span></span>

## <span data-ttu-id="f0c71-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0c71-145">NOTES</span></span>

<span data-ttu-id="f0c71-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f0c71-146">ALIASES</span></span>

<span data-ttu-id="f0c71-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="f0c71-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0c71-148">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="f0c71-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0c71-149">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f0c71-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0c71-150">INPUTOBJECT <ICloudServiceIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="f0c71-150">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0c71-151">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f0c71-151">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="f0c71-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="f0c71-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0c71-153">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f0c71-153">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="f0c71-154">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="f0c71-154">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="f0c71-155">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="f0c71-155">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="f0c71-156">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f0c71-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f0c71-157">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="f0c71-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f0c71-158">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne angibt.</span><span class="sxs-lookup"><span data-stu-id="f0c71-158">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="f0c71-159">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="f0c71-159">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="f0c71-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0c71-160">RELATED LINKS</span></span>

