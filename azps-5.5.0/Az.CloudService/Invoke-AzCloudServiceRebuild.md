---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudservicerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRebuild.md
ms.openlocfilehash: 1efeb45704898588c7ba8f08148f88d0eaf3e5c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166673"
---
# <span data-ttu-id="2919c-101">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="2919c-101">Invoke-AzCloudServiceRebuild</span></span>

## <span data-ttu-id="2919c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2919c-102">SYNOPSIS</span></span>
<span data-ttu-id="2919c-103">Mit "Rolleninstanzen neu erstellen" wird das Betriebssystem auf Instanzen von Webrollen oder Workerrollen neu installiert, und die von ihnen verwendeten Speicherressourcen werden initialisiert.</span><span class="sxs-lookup"><span data-stu-id="2919c-103">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="2919c-104">Wenn Sie keine Speicherressourcen initialisieren möchten, können Sie "Rolleninstanzen neu abbilden" verwenden.</span><span class="sxs-lookup"><span data-stu-id="2919c-104">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="2919c-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2919c-105">SYNTAX</span></span>

### <span data-ttu-id="2919c-106">RebuildExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2919c-106">RebuildExpanded (Default)</span></span>
```
Invoke-AzCloudServiceRebuild -CloudServiceName <String> -ResourceGroupName <String> -RoleInstance <String[]>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2919c-107">RebuildViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2919c-107">RebuildViaIdentityExpanded</span></span>
```
Invoke-AzCloudServiceRebuild -InputObject <ICloudServiceIdentity> -RoleInstance <String[]>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2919c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2919c-108">DESCRIPTION</span></span>
<span data-ttu-id="2919c-109">Mit "Rolleninstanzen neu erstellen" wird das Betriebssystem auf Instanzen von Webrollen oder Workerrollen neu installiert, und die von ihnen verwendeten Speicherressourcen werden initialisiert.</span><span class="sxs-lookup"><span data-stu-id="2919c-109">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="2919c-110">Wenn Sie keine Speicherressourcen initialisieren möchten, können Sie "Rolleninstanzen neu abbilden" verwenden.</span><span class="sxs-lookup"><span data-stu-id="2919c-110">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

## <span data-ttu-id="2919c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2919c-111">EXAMPLES</span></span>

### <span data-ttu-id="2919c-112">Beispiel 1: Neuerstellen von Rolleninstanzen des Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="2919c-112">Example 1: Rebuild role instances of cloud service</span></span>
```powershell
PS C:\> $roleInstances = @("ContosoFrontEnd_IN_0", "ContosoBackEnd_IN_1")
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance $roleInstances
```

<span data-ttu-id="2919c-113">Dieser Befehl erstellt zwei Rolleninstanzen ContosoFrontEnd_IN_0 und ContosoBackEnd_IN_1 des Clouddiensts "ContosoCS", der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="2919c-113">This command rebuilds 2 role instances ContosoFrontEnd_IN_0 and ContosoBackEnd_IN_1 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="2919c-114">Beispiel 2: Neuerstellen aller Rollen des Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="2919c-114">Example 2: Rebuild all roles of cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstance "*"
```

<span data-ttu-id="2919c-115">Mit diesem Befehl werden alle Rolleninstanzen des Clouddiensts "ContosoCS" neu erstellt, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="2919c-115">This command rebuilds all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="2919c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2919c-116">PARAMETERS</span></span>

### <span data-ttu-id="2919c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2919c-117">-AsJob</span></span>
<span data-ttu-id="2919c-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2919c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2919c-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="2919c-119">-CloudServiceName</span></span>
<span data-ttu-id="2919c-120">Der Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="2919c-120">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2919c-121">-DefaultProfile</span></span>
<span data-ttu-id="2919c-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2919c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2919c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2919c-123">-InputObject</span></span>
<span data-ttu-id="2919c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="2919c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2919c-125">-NoWait</span></span>
<span data-ttu-id="2919c-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2919c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2919c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2919c-127">-PassThru</span></span>
<span data-ttu-id="2919c-128">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2919c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2919c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2919c-129">-ResourceGroupName</span></span>
<span data-ttu-id="2919c-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2919c-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-131">-RoleInstance</span><span class="sxs-lookup"><span data-stu-id="2919c-131">-RoleInstance</span></span>
<span data-ttu-id="2919c-132">Liste der Namen der Clouddienst-Rolleninstanzen.</span><span class="sxs-lookup"><span data-stu-id="2919c-132">List of cloud service role instance names.</span></span>
<span data-ttu-id="2919c-133">Der Wert "\*" bedeutet alle Rolleninstanzen des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="2919c-133">Value of '\*' will signify all role instances of the cloud service.</span></span>

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

### <span data-ttu-id="2919c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2919c-134">-SubscriptionId</span></span>
<span data-ttu-id="2919c-135">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2919c-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2919c-136">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="2919c-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RebuildExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2919c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2919c-137">-Confirm</span></span>
<span data-ttu-id="2919c-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2919c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2919c-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2919c-139">-WhatIf</span></span>
<span data-ttu-id="2919c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2919c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2919c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2919c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2919c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2919c-142">CommonParameters</span></span>
<span data-ttu-id="2919c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2919c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2919c-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2919c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2919c-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2919c-145">INPUTS</span></span>

### <span data-ttu-id="2919c-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="2919c-146">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="2919c-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2919c-147">OUTPUTS</span></span>

### <span data-ttu-id="2919c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2919c-148">System.Boolean</span></span>

## <span data-ttu-id="2919c-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2919c-149">NOTES</span></span>

<span data-ttu-id="2919c-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2919c-150">ALIASES</span></span>

<span data-ttu-id="2919c-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2919c-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2919c-152">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2919c-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2919c-153">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2919c-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2919c-154">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="2919c-154">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2919c-155">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2919c-155">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="2919c-156">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2919c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2919c-157">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2919c-157">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="2919c-158">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="2919c-158">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="2919c-159">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="2919c-159">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="2919c-160">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2919c-160">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2919c-161">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="2919c-161">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2919c-162">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2919c-162">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="2919c-163">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="2919c-163">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="2919c-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2919c-164">RELATED LINKS</span></span>

