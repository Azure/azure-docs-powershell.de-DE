---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/restart-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudService.md
ms.openlocfilehash: c31aed5422e9b142690875de242462af64acf799
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149009"
---
# <span data-ttu-id="ebd9a-101">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="ebd9a-101">Restart-AzCloudService</span></span>

## <span data-ttu-id="ebd9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebd9a-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd9a-103">Startet eine oder mehrere Rolleninstanzen in einem Clouddienst neu.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-103">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="ebd9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebd9a-104">SYNTAX</span></span>

### <span data-ttu-id="ebd9a-105">RestartExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="ebd9a-105">RestartExpanded (Default)</span></span>
```
Restart-AzCloudService -Name <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ebd9a-106">RestartViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ebd9a-106">RestartViaIdentityExpanded</span></span>
```
Restart-AzCloudService -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ebd9a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebd9a-107">DESCRIPTION</span></span>
<span data-ttu-id="ebd9a-108">Startet eine oder mehrere Rolleninstanzen in einem Clouddienst neu.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-108">Restarts one or more role instances in a cloud service.</span></span>

## <span data-ttu-id="ebd9a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ebd9a-109">EXAMPLES</span></span>

### <span data-ttu-id="ebd9a-110">Beispiel 1: Neustarten von Rolleninstanzen des Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="ebd9a-110">Example 1: Restart role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="ebd9a-111">Mit diesem Befehl werden zwei Rolleninstanzen ContosoFrontEnd_IN_0 und ContosoBackEnd_IN_1 des Clouddiensts "ContosoCS" neu gestartet, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-111">This command restarts 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="ebd9a-112">Beispiel 2: Neustarten aller Rollen des Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="ebd9a-112">Example 2: Restart all roles of cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="ebd9a-113">Mit diesem Befehl werden alle Rolleninstanzen des Clouddiensts "ContosoCS" neu gestartet, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-113">This command restarts all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="ebd9a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebd9a-114">PARAMETERS</span></span>

### <span data-ttu-id="ebd9a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebd9a-115">-AsJob</span></span>
<span data-ttu-id="ebd9a-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ebd9a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ebd9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd9a-117">-DefaultProfile</span></span>
<span data-ttu-id="ebd9a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebd9a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebd9a-119">-InputObject</span></span>
<span data-ttu-id="ebd9a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ebd9a-121">-Name</span></span>
<span data-ttu-id="ebd9a-122">Der Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ebd9a-123">-NoWait</span></span>
<span data-ttu-id="ebd9a-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ebd9a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ebd9a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebd9a-125">-PassThru</span></span>
<span data-ttu-id="ebd9a-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ebd9a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebd9a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ebd9a-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9a-129">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="ebd9a-129">-RoleInstance</span></span>
<span data-ttu-id="ebd9a-130">Liste der Namen der Clouddienst-Rolleninstanzen.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-130">List of cloud service role instance names.</span></span>
<span data-ttu-id="ebd9a-131">Der Wert "\*" bedeutet alle Rolleninstanzen des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-131">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="ebd9a-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebd9a-132">-SubscriptionId</span></span>
<span data-ttu-id="ebd9a-133">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-133">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ebd9a-134">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebd9a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebd9a-135">-Confirm</span></span>
<span data-ttu-id="ebd9a-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebd9a-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ebd9a-137">-WhatIf</span></span>
<span data-ttu-id="ebd9a-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebd9a-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebd9a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd9a-140">CommonParameters</span></span>
<span data-ttu-id="ebd9a-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd9a-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebd9a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd9a-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ebd9a-143">INPUTS</span></span>

### <span data-ttu-id="ebd9a-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="ebd9a-144">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="ebd9a-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ebd9a-145">OUTPUTS</span></span>

### <span data-ttu-id="ebd9a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebd9a-146">System.Boolean</span></span>

## <span data-ttu-id="ebd9a-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ebd9a-147">NOTES</span></span>

<span data-ttu-id="ebd9a-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ebd9a-148">ALIASES</span></span>

<span data-ttu-id="ebd9a-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ebd9a-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ebd9a-150">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ebd9a-151">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ebd9a-152">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ebd9a-152">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ebd9a-153">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ebd9a-153">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="ebd9a-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ebd9a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ebd9a-155">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ebd9a-155">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="ebd9a-156">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-156">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="ebd9a-157">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-157">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="ebd9a-158">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ebd9a-159">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ebd9a-160">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-160">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="ebd9a-161">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="ebd9a-161">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="ebd9a-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ebd9a-162">RELATED LINKS</span></span>

