---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: d998e29fc254b1bf507ab7d7732bc3bdcf68f54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145044"
---
# <span data-ttu-id="fbbfa-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="fbbfa-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="fbbfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbfa-103">Der asynchrone Vorgang "Rolleninstanz neu erstellen" installiert das Betriebssystem erneut auf Instanzen von Webrollen oder Workerrollen und initialisiert die von ihnen verwendeten Speicherressourcen.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="fbbfa-104">Wenn Sie keine Speicherressourcen initialisieren möchten, können Sie die Reimage-Rolleninstanz verwenden.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="fbbfa-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbbfa-105">SYNTAX</span></span>

### <span data-ttu-id="fbbfa-106">Neu erstellen (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbbfa-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fbbfa-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fbbfa-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbbfa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbbfa-108">DESCRIPTION</span></span>
<span data-ttu-id="fbbfa-109">Der asynchrone Vorgang "Rolleninstanz neu erstellen" installiert das Betriebssystem erneut auf Instanzen von Webrollen oder Workerrollen und initialisiert die von ihnen verwendeten Speicherressourcen.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="fbbfa-110">Wenn Sie keine Speicherressourcen initialisieren möchten, können Sie die Reimage-Rolleninstanz verwenden.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="fbbfa-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbbfa-111">EXAMPLES</span></span>

### <span data-ttu-id="fbbfa-112">Beispiel 1: Neuerstellen der Rolleninstanz eines Clouddiensts</span><span class="sxs-lookup"><span data-stu-id="fbbfa-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="fbbfa-113">Dieser Befehl reimages rolleninstanz namens ContosoFrontEnd_IN_0 des Clouddiensts "ContosoCS", der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="fbbfa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbbfa-114">PARAMETERS</span></span>

### <span data-ttu-id="fbbfa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbbfa-115">-AsJob</span></span>
<span data-ttu-id="fbbfa-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fbbfa-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fbbfa-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="fbbfa-117">-CloudServiceName</span></span>
<span data-ttu-id="fbbfa-118">.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbfa-119">-DefaultProfile</span></span>
<span data-ttu-id="fbbfa-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbbfa-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbbfa-121">-InputObject</span></span>
<span data-ttu-id="fbbfa-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbfa-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fbbfa-123">-NoWait</span></span>
<span data-ttu-id="fbbfa-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fbbfa-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fbbfa-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbbfa-125">-PassThru</span></span>
<span data-ttu-id="fbbfa-126">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fbbfa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbfa-127">-ResourceGroupName</span></span>
<span data-ttu-id="fbbfa-128">.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbfa-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="fbbfa-129">-RoleInstanceName</span></span>
<span data-ttu-id="fbbfa-130">Der Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbfa-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbbfa-131">-SubscriptionId</span></span>
<span data-ttu-id="fbbfa-132">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fbbfa-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbfa-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbbfa-134">-Confirm</span></span>
<span data-ttu-id="fbbfa-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbbfa-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fbbfa-136">-WhatIf</span></span>
<span data-ttu-id="fbbfa-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbbfa-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbbfa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbfa-139">CommonParameters</span></span>
<span data-ttu-id="fbbfa-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbfa-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbbfa-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbfa-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbfa-142">INPUTS</span></span>

### <span data-ttu-id="fbbfa-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="fbbfa-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="fbbfa-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbfa-144">OUTPUTS</span></span>

### <span data-ttu-id="fbbfa-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbbfa-145">System.Boolean</span></span>

## <span data-ttu-id="fbbfa-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbbfa-146">NOTES</span></span>

<span data-ttu-id="fbbfa-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fbbfa-147">ALIASES</span></span>

<span data-ttu-id="fbbfa-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="fbbfa-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fbbfa-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fbbfa-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fbbfa-151">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="fbbfa-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fbbfa-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="fbbfa-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="fbbfa-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="fbbfa-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fbbfa-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="fbbfa-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="fbbfa-155">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="fbbfa-156">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="fbbfa-157">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fbbfa-158">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="fbbfa-159">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="fbbfa-160">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="fbbfa-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="fbbfa-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbbfa-161">RELATED LINKS</span></span>

