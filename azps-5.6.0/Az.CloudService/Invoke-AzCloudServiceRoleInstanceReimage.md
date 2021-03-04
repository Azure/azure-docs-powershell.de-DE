---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925144"
---
# <span data-ttu-id="dfbcc-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="dfbcc-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="dfbcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfbcc-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbcc-103">Der asynchrone Vorgang "Rolleninstanz neu abbilden" installiert das Betriebssystem erneut auf Instanzen von Webrollen oder Workerrollen.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="dfbcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfbcc-104">SYNTAX</span></span>

### <span data-ttu-id="dfbcc-105">Neubild (Standard)</span><span class="sxs-lookup"><span data-stu-id="dfbcc-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dfbcc-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dfbcc-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfbcc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfbcc-107">DESCRIPTION</span></span>
<span data-ttu-id="dfbcc-108">Der asynchrone Vorgang "Rolleninstanz neu abbilden" installiert das Betriebssystem erneut auf Instanzen von Webrollen oder Workerrollen.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="dfbcc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfbcc-109">EXAMPLES</span></span>

### <span data-ttu-id="dfbcc-110">Beispiel 1: Erneutes Abbilden der Rolleninstanz eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="dfbcc-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="dfbcc-111">Mit diesem Befehl wird die Rolleninstanz ContosoFrontEnd_IN_0 des Clouddiensts ContosoCS, der zur Ressourcengruppe "ContosOrg" gehört, neu abbilden.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="dfbcc-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dfbcc-112">PARAMETERS</span></span>

### <span data-ttu-id="dfbcc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfbcc-113">-AsJob</span></span>
<span data-ttu-id="dfbcc-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="dfbcc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dfbcc-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="dfbcc-115">-CloudServiceName</span></span>
<span data-ttu-id="dfbcc-116">.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-116">.</span></span>

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

### <span data-ttu-id="dfbcc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbcc-117">-DefaultProfile</span></span>
<span data-ttu-id="dfbcc-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfbcc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfbcc-119">-InputObject</span></span>
<span data-ttu-id="dfbcc-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dfbcc-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dfbcc-121">-NoWait</span></span>
<span data-ttu-id="dfbcc-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="dfbcc-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dfbcc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfbcc-123">-PassThru</span></span>
<span data-ttu-id="dfbcc-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dfbcc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbcc-125">-ResourceGroupName</span></span>
<span data-ttu-id="dfbcc-126">.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-126">.</span></span>

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

### <span data-ttu-id="dfbcc-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="dfbcc-127">-RoleInstanceName</span></span>
<span data-ttu-id="dfbcc-128">Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-128">Name of the role instance.</span></span>

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

### <span data-ttu-id="dfbcc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfbcc-129">-SubscriptionId</span></span>
<span data-ttu-id="dfbcc-130">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dfbcc-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dfbcc-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfbcc-132">-Confirm</span></span>
<span data-ttu-id="dfbcc-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfbcc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbcc-134">-WhatIf</span></span>
<span data-ttu-id="dfbcc-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfbcc-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfbcc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbcc-137">CommonParameters</span></span>
<span data-ttu-id="dfbcc-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbcc-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfbcc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbcc-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfbcc-140">INPUTS</span></span>

### <span data-ttu-id="dfbcc-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="dfbcc-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="dfbcc-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfbcc-142">OUTPUTS</span></span>

### <span data-ttu-id="dfbcc-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dfbcc-143">System.Boolean</span></span>

## <span data-ttu-id="dfbcc-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dfbcc-144">NOTES</span></span>

<span data-ttu-id="dfbcc-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dfbcc-145">ALIASES</span></span>

<span data-ttu-id="dfbcc-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dfbcc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfbcc-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfbcc-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfbcc-149">INPUTOBJECT <ICloudServiceIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="dfbcc-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfbcc-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dfbcc-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="dfbcc-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dfbcc-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfbcc-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dfbcc-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="dfbcc-153">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="dfbcc-154">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="dfbcc-155">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dfbcc-156">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dfbcc-157">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne angibt.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="dfbcc-158">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="dfbcc-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="dfbcc-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dfbcc-159">RELATED LINKS</span></span>

