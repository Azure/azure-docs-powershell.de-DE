---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 12a07367835341e86ca181f2fa419e8996a434a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171377"
---
# <span data-ttu-id="b5108-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="b5108-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="b5108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5108-102">SYNOPSIS</span></span>
<span data-ttu-id="b5108-103">Der asynchrone Vorgang der Neustartrolleinstanz fordert einen Neustart einer Rolleninstanz im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="b5108-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="b5108-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5108-104">SYNTAX</span></span>

### <span data-ttu-id="b5108-105">Neu starten (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5108-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b5108-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5108-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5108-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5108-107">DESCRIPTION</span></span>
<span data-ttu-id="b5108-108">Der asynchrone Vorgang der Neustartrolleinstanz fordert einen Neustart einer Rolleninstanz im Clouddienst an.</span><span class="sxs-lookup"><span data-stu-id="b5108-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="b5108-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5108-109">EXAMPLES</span></span>

### <span data-ttu-id="b5108-110">Beispiel 1: Neustarten der Rolleninstanz eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="b5108-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="b5108-111">Mit diesem Befehl wird die Rolleninstanz mit ContosoFrontEnd_IN_0 des Clouddiensts "ContosoCS" neu gestartet, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="b5108-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b5108-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5108-112">PARAMETERS</span></span>

### <span data-ttu-id="b5108-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5108-113">-AsJob</span></span>
<span data-ttu-id="b5108-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b5108-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b5108-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b5108-115">-CloudServiceName</span></span>
<span data-ttu-id="b5108-116">.</span><span class="sxs-lookup"><span data-stu-id="b5108-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5108-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5108-117">-DefaultProfile</span></span>
<span data-ttu-id="b5108-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5108-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5108-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5108-119">-InputObject</span></span>
<span data-ttu-id="b5108-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b5108-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5108-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b5108-121">-NoWait</span></span>
<span data-ttu-id="b5108-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b5108-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b5108-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5108-123">-PassThru</span></span>
<span data-ttu-id="b5108-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="b5108-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b5108-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5108-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5108-126">.</span><span class="sxs-lookup"><span data-stu-id="b5108-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5108-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="b5108-127">-RoleInstanceName</span></span>
<span data-ttu-id="b5108-128">Der Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="b5108-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5108-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5108-129">-SubscriptionId</span></span>
<span data-ttu-id="b5108-130">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5108-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5108-131">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="b5108-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5108-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5108-132">-Confirm</span></span>
<span data-ttu-id="b5108-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5108-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5108-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b5108-134">-WhatIf</span></span>
<span data-ttu-id="b5108-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5108-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5108-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5108-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5108-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5108-137">CommonParameters</span></span>
<span data-ttu-id="b5108-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5108-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5108-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5108-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5108-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5108-140">INPUTS</span></span>

### <span data-ttu-id="b5108-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b5108-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b5108-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5108-142">OUTPUTS</span></span>

### <span data-ttu-id="b5108-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5108-143">System.Boolean</span></span>

## <span data-ttu-id="b5108-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5108-144">NOTES</span></span>

<span data-ttu-id="b5108-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b5108-145">ALIASES</span></span>

<span data-ttu-id="b5108-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b5108-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5108-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b5108-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5108-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5108-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5108-149">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b5108-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5108-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b5108-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b5108-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b5108-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5108-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b5108-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b5108-153">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="b5108-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b5108-154">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="b5108-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b5108-155">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5108-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b5108-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="b5108-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b5108-157">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b5108-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b5108-158">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="b5108-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="b5108-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5108-159">RELATED LINKS</span></span>

