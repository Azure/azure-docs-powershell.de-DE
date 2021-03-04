---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/remove-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Remove-AzCloudService.md
ms.openlocfilehash: 5004aa694dd0ebb90239e2fb77259df9e84c59f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939672"
---
# <span data-ttu-id="6bdff-101">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="6bdff-101">Remove-AzCloudService</span></span>

## <span data-ttu-id="6bdff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bdff-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdff-103">Löscht einen Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="6bdff-103">Deletes a cloud service.</span></span>

## <span data-ttu-id="6bdff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bdff-104">SYNTAX</span></span>

### <span data-ttu-id="6bdff-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6bdff-105">Delete (Default)</span></span>
```
Remove-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6bdff-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6bdff-106">DeleteViaIdentity</span></span>
```
Remove-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6bdff-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bdff-107">DESCRIPTION</span></span>
<span data-ttu-id="6bdff-108">Löscht einen Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="6bdff-108">Deletes a cloud service.</span></span>

## <span data-ttu-id="6bdff-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bdff-109">EXAMPLES</span></span>

### <span data-ttu-id="6bdff-110">Beispiel 1: Entfernen eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="6bdff-110">Example 1: Remove a cloud service</span></span>
```powershell
PS C:\> Remove-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="6bdff-111">Mit diesem Befehl wird der Clouddienst contosoCS entfernt, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="6bdff-111">This command removes the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6bdff-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6bdff-112">PARAMETERS</span></span>

### <span data-ttu-id="6bdff-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bdff-113">-AsJob</span></span>
<span data-ttu-id="6bdff-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6bdff-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6bdff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdff-115">-DefaultProfile</span></span>
<span data-ttu-id="6bdff-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bdff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bdff-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bdff-117">-InputObject</span></span>
<span data-ttu-id="6bdff-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6bdff-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bdff-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6bdff-119">-Name</span></span>
<span data-ttu-id="6bdff-120">Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="6bdff-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdff-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6bdff-121">-NoWait</span></span>
<span data-ttu-id="6bdff-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6bdff-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6bdff-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bdff-123">-PassThru</span></span>
<span data-ttu-id="6bdff-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bdff-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6bdff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bdff-125">-ResourceGroupName</span></span>
<span data-ttu-id="6bdff-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6bdff-126">Name of the resource group.</span></span>

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

### <span data-ttu-id="6bdff-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bdff-127">-SubscriptionId</span></span>
<span data-ttu-id="6bdff-128">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6bdff-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6bdff-129">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="6bdff-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6bdff-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6bdff-130">-Confirm</span></span>
<span data-ttu-id="6bdff-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6bdff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bdff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bdff-132">-WhatIf</span></span>
<span data-ttu-id="6bdff-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6bdff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bdff-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6bdff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bdff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdff-135">CommonParameters</span></span>
<span data-ttu-id="6bdff-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bdff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdff-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6bdff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdff-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bdff-138">INPUTS</span></span>

### <span data-ttu-id="6bdff-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6bdff-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="6bdff-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bdff-140">OUTPUTS</span></span>

### <span data-ttu-id="6bdff-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bdff-141">System.Boolean</span></span>

## <span data-ttu-id="6bdff-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6bdff-142">NOTES</span></span>

<span data-ttu-id="6bdff-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6bdff-143">ALIASES</span></span>

<span data-ttu-id="6bdff-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6bdff-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6bdff-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6bdff-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6bdff-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6bdff-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6bdff-147">INPUTOBJECT <ICloudServiceIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="6bdff-147">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6bdff-148">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6bdff-148">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="6bdff-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6bdff-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6bdff-150">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="6bdff-150">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="6bdff-151">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="6bdff-151">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="6bdff-152">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="6bdff-152">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="6bdff-153">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6bdff-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6bdff-154">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="6bdff-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6bdff-155">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne angibt.</span><span class="sxs-lookup"><span data-stu-id="6bdff-155">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="6bdff-156">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="6bdff-156">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="6bdff-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6bdff-157">RELATED LINKS</span></span>

