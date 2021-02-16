---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 4306a38920ca8e7a5ab052df054b96a70b2ce613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167977"
---
# <span data-ttu-id="5d659-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="5d659-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="5d659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d659-102">SYNOPSIS</span></span>
<span data-ttu-id="5d659-103">Mit dem asynchronen Vorgang der Reimage-Rolleninstanz wird das Betriebssystem unter Instanzen von Webrollen oder Workerrollen neu installiert.</span><span class="sxs-lookup"><span data-stu-id="5d659-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="5d659-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d659-104">SYNTAX</span></span>

### <span data-ttu-id="5d659-105">Reimage (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d659-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d659-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d659-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d659-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d659-107">DESCRIPTION</span></span>
<span data-ttu-id="5d659-108">Mit dem asynchronen Vorgang der Reimage-Rolleninstanz wird das Betriebssystem unter Instanzen von Webrollen oder Workerrollen neu installiert.</span><span class="sxs-lookup"><span data-stu-id="5d659-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="5d659-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d659-109">EXAMPLES</span></span>

### <span data-ttu-id="5d659-110">Beispiel 1: Neubilden der Rolleninstanz eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="5d659-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="5d659-111">Dieser Befehl reimages rolleninstanz namens ContosoFrontEnd_IN_0 des Clouddiensts "ContosoCS", der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="5d659-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="5d659-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d659-112">PARAMETERS</span></span>

### <span data-ttu-id="5d659-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d659-113">-AsJob</span></span>
<span data-ttu-id="5d659-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5d659-114">Run the command as a job</span></span>

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

### <span data-ttu-id="5d659-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="5d659-115">-CloudServiceName</span></span>
<span data-ttu-id="5d659-116">.</span><span class="sxs-lookup"><span data-stu-id="5d659-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d659-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d659-117">-DefaultProfile</span></span>
<span data-ttu-id="5d659-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d659-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d659-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d659-119">-InputObject</span></span>
<span data-ttu-id="5d659-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="5d659-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d659-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5d659-121">-NoWait</span></span>
<span data-ttu-id="5d659-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5d659-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d659-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d659-123">-PassThru</span></span>
<span data-ttu-id="5d659-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5d659-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5d659-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d659-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d659-126">.</span><span class="sxs-lookup"><span data-stu-id="5d659-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d659-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="5d659-127">-RoleInstanceName</span></span>
<span data-ttu-id="5d659-128">Der Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="5d659-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d659-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d659-129">-SubscriptionId</span></span>
<span data-ttu-id="5d659-130">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5d659-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d659-131">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="5d659-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d659-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d659-132">-Confirm</span></span>
<span data-ttu-id="5d659-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d659-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d659-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5d659-134">-WhatIf</span></span>
<span data-ttu-id="5d659-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d659-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d659-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d659-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d659-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d659-137">CommonParameters</span></span>
<span data-ttu-id="5d659-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d659-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d659-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d659-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d659-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d659-140">INPUTS</span></span>

### <span data-ttu-id="5d659-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="5d659-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="5d659-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d659-142">OUTPUTS</span></span>

### <span data-ttu-id="5d659-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d659-143">System.Boolean</span></span>

## <span data-ttu-id="5d659-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d659-144">NOTES</span></span>

<span data-ttu-id="5d659-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5d659-145">ALIASES</span></span>

<span data-ttu-id="5d659-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5d659-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d659-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d659-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d659-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d659-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d659-149">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="5d659-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d659-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5d659-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="5d659-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="5d659-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d659-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5d659-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="5d659-153">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="5d659-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="5d659-154">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="5d659-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="5d659-155">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5d659-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d659-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="5d659-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5d659-157">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5d659-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="5d659-158">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="5d659-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="5d659-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d659-159">RELATED LINKS</span></span>

