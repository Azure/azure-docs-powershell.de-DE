---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/stop-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Stop-AzCloudService.md
ms.openlocfilehash: 539106e979babd1df41ca2505a2978132e825b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946294"
---
# <span data-ttu-id="a0f46-101">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="a0f46-101">Stop-AzCloudService</span></span>

## <span data-ttu-id="a0f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f46-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f46-103">Schalten Sie den Clouddienst aus.</span><span class="sxs-lookup"><span data-stu-id="a0f46-103">Power off the cloud service.</span></span>
<span data-ttu-id="a0f46-104">Beachten Sie, dass Ressourcen weiterhin angefügt sind und Ihnen die Kosten für die Ressourcen in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0f46-104">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="a0f46-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0f46-105">SYNTAX</span></span>

### <span data-ttu-id="a0f46-106">PowerOff (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0f46-106">PowerOff (Default)</span></span>
```
Stop-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a0f46-107">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a0f46-107">PowerOffViaIdentity</span></span>
```
Stop-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0f46-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0f46-108">DESCRIPTION</span></span>
<span data-ttu-id="a0f46-109">Schalten Sie den Clouddienst aus.</span><span class="sxs-lookup"><span data-stu-id="a0f46-109">Power off the cloud service.</span></span>
<span data-ttu-id="a0f46-110">Beachten Sie, dass Ressourcen weiterhin angefügt sind und Ihnen die Kosten für die Ressourcen in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0f46-110">Note that resources are still attached and you are getting charged for the resources.</span></span>

## <span data-ttu-id="a0f46-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0f46-111">EXAMPLES</span></span>

### <span data-ttu-id="a0f46-112">Beispiel 1: Beenden des Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="a0f46-112">Example 1: Stop cloud service</span></span>
```powershell
PS C:\> Stop-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
```

<span data-ttu-id="a0f46-113">Mit diesem Befehl werden alle Rolleninstanzen beendet, die zum Clouddienst ContosoCS gehören.</span><span class="sxs-lookup"><span data-stu-id="a0f46-113">This command stops all the role instances that belong to the the cloud service named ContosoCS.</span></span>

## <span data-ttu-id="a0f46-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a0f46-114">PARAMETERS</span></span>

### <span data-ttu-id="a0f46-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0f46-115">-AsJob</span></span>
<span data-ttu-id="a0f46-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="a0f46-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a0f46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f46-117">-DefaultProfile</span></span>
<span data-ttu-id="a0f46-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0f46-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f46-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0f46-119">-InputObject</span></span>
<span data-ttu-id="a0f46-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a0f46-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f46-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0f46-121">-Name</span></span>
<span data-ttu-id="a0f46-122">Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="a0f46-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f46-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a0f46-123">-NoWait</span></span>
<span data-ttu-id="a0f46-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="a0f46-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a0f46-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0f46-125">-PassThru</span></span>
<span data-ttu-id="a0f46-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0f46-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a0f46-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f46-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0f46-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0f46-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f46-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0f46-129">-SubscriptionId</span></span>
<span data-ttu-id="a0f46-130">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a0f46-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0f46-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="a0f46-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f46-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0f46-132">-Confirm</span></span>
<span data-ttu-id="a0f46-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0f46-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f46-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f46-134">-WhatIf</span></span>
<span data-ttu-id="a0f46-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0f46-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f46-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0f46-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f46-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f46-137">CommonParameters</span></span>
<span data-ttu-id="a0f46-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f46-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f46-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0f46-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f46-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0f46-140">INPUTS</span></span>

### <span data-ttu-id="a0f46-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a0f46-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="a0f46-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0f46-142">OUTPUTS</span></span>

### <span data-ttu-id="a0f46-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0f46-143">System.Boolean</span></span>

## <span data-ttu-id="a0f46-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a0f46-144">NOTES</span></span>

<span data-ttu-id="a0f46-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a0f46-145">ALIASES</span></span>

<span data-ttu-id="a0f46-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a0f46-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0f46-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a0f46-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0f46-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0f46-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0f46-149">INPUTOBJECT <ICloudServiceIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="a0f46-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0f46-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a0f46-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="a0f46-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a0f46-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0f46-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="a0f46-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="a0f46-153">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="a0f46-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="a0f46-154">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="a0f46-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="a0f46-155">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a0f46-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a0f46-156">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="a0f46-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a0f46-157">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne angibt.</span><span class="sxs-lookup"><span data-stu-id="a0f46-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="a0f46-158">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="a0f46-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="a0f46-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a0f46-159">RELATED LINKS</span></span>

