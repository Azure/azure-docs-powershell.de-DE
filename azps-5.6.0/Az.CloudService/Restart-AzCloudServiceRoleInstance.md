---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/restart-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Restart-AzCloudServiceRoleInstance.md
ms.openlocfilehash: f184696dbcfce35bf6e52f889d2c787214330e70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935336"
---
# <span data-ttu-id="a6bea-101">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="a6bea-101">Restart-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="a6bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6bea-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bea-103">Der asynchrone Neustart der Rolleninstanz erfordert einen Neustart einer Rolleninstanz im Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="a6bea-103">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="a6bea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6bea-104">SYNTAX</span></span>

### <span data-ttu-id="a6bea-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6bea-105">Restart (Default)</span></span>
```
Restart-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6bea-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6bea-106">RestartViaIdentity</span></span>
```
Restart-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6bea-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6bea-107">DESCRIPTION</span></span>
<span data-ttu-id="a6bea-108">Der asynchrone Neustart der Rolleninstanz erfordert einen Neustart einer Rolleninstanz im Clouddienst.</span><span class="sxs-lookup"><span data-stu-id="a6bea-108">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

## <span data-ttu-id="a6bea-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6bea-109">EXAMPLES</span></span>

### <span data-ttu-id="a6bea-110">Beispiel 1: Neu starten der Rolleninstanz eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="a6bea-110">Example 1: Restart role instance of a cloud service</span></span>
```powershell
PS C:\> Restart-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="a6bea-111">Mit diesem Befehl wird die Rolleninstanz ContosoFrontEnd_IN_0 des Clouddiensts ContosoCS neu gestartet, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="a6bea-111">This command restarts role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a6bea-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a6bea-112">PARAMETERS</span></span>

### <span data-ttu-id="a6bea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6bea-113">-AsJob</span></span>
<span data-ttu-id="a6bea-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a6bea-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a6bea-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="a6bea-115">-CloudServiceName</span></span>
<span data-ttu-id="a6bea-116">.</span><span class="sxs-lookup"><span data-stu-id="a6bea-116">.</span></span>

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

### <span data-ttu-id="a6bea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bea-117">-DefaultProfile</span></span>
<span data-ttu-id="a6bea-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6bea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6bea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6bea-119">-InputObject</span></span>
<span data-ttu-id="a6bea-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a6bea-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a6bea-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6bea-121">-NoWait</span></span>
<span data-ttu-id="a6bea-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a6bea-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6bea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6bea-123">-PassThru</span></span>
<span data-ttu-id="a6bea-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6bea-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a6bea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bea-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6bea-126">.</span><span class="sxs-lookup"><span data-stu-id="a6bea-126">.</span></span>

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

### <span data-ttu-id="a6bea-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="a6bea-127">-RoleInstanceName</span></span>
<span data-ttu-id="a6bea-128">Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="a6bea-128">Name of the role instance.</span></span>

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

### <span data-ttu-id="a6bea-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6bea-129">-SubscriptionId</span></span>
<span data-ttu-id="a6bea-130">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a6bea-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6bea-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="a6bea-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a6bea-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6bea-132">-Confirm</span></span>
<span data-ttu-id="a6bea-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6bea-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bea-134">-WhatIf</span></span>
<span data-ttu-id="a6bea-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6bea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bea-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6bea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bea-137">CommonParameters</span></span>
<span data-ttu-id="a6bea-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6bea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bea-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6bea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bea-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6bea-140">INPUTS</span></span>

### <span data-ttu-id="a6bea-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a6bea-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="a6bea-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6bea-142">OUTPUTS</span></span>

### <span data-ttu-id="a6bea-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6bea-143">System.Boolean</span></span>

## <span data-ttu-id="a6bea-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a6bea-144">NOTES</span></span>

<span data-ttu-id="a6bea-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a6bea-145">ALIASES</span></span>

<span data-ttu-id="a6bea-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a6bea-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6bea-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a6bea-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6bea-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6bea-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6bea-149">INPUTOBJECT <ICloudServiceIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="a6bea-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6bea-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a6bea-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="a6bea-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a6bea-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6bea-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a6bea-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="a6bea-153">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="a6bea-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="a6bea-154">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="a6bea-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="a6bea-155">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a6bea-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a6bea-156">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="a6bea-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a6bea-157">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne angibt.</span><span class="sxs-lookup"><span data-stu-id="a6bea-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="a6bea-158">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="a6bea-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="a6bea-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a6bea-159">RELATED LINKS</span></span>

