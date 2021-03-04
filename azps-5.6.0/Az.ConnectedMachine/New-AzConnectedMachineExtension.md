---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: df2e1de102143f227178b45ea14264f9e61d86a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948811"
---
# <span data-ttu-id="8847d-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8847d-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="8847d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8847d-102">SYNOPSIS</span></span>
<span data-ttu-id="8847d-103">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="8847d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8847d-104">SYNTAX</span></span>

### <span data-ttu-id="8847d-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="8847d-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8847d-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="8847d-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8847d-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8847d-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8847d-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8847d-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8847d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8847d-109">DESCRIPTION</span></span>
<span data-ttu-id="8847d-110">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="8847d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8847d-111">EXAMPLES</span></span>

### <span data-ttu-id="8847d-112">Beispiel 1: Hinzufügen einer neuen Erweiterung zu einem Computer</span><span class="sxs-lookup"><span data-stu-id="8847d-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8847d-113">Legt eine Erweiterung auf einem Computer fest.</span><span class="sxs-lookup"><span data-stu-id="8847d-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="8847d-114">Beispiel 2: Hinzufügen einer neuen Erweiterung mit über die Pipeline angegebenen Erweiterungsparametern</span><span class="sxs-lookup"><span data-stu-id="8847d-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8847d-115">Dadurch wird eine neue Erweiterung mit den Erweiterungsparametern erstellt, die vom über die Pipeline übergebenen Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8847d-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="8847d-116">Dies ist großartig, wenn Sie die Parameter eines Computers übernehmen und auf einen anderen Computer anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8847d-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="8847d-117">Beispiel 3: Hinzufügen einer neuen Erweiterung mit über die Pipeline angegebener Position</span><span class="sxs-lookup"><span data-stu-id="8847d-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8847d-118">Dadurch wird mithilfe der über die Pipeline bereitgestellten Identität eine neue Computererweiterung erstellt.</span><span class="sxs-lookup"><span data-stu-id="8847d-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="8847d-119">Sie werden dies wahrscheinlich nicht tun, aber es ist möglich.</span><span class="sxs-lookup"><span data-stu-id="8847d-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="8847d-120">Beispiel 4: Hinzufügen einer neuen Erweiterung mithilfe eines Erweiterungsobjekts als Speicherort und Parameter für die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="8847d-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="8847d-121">Dadurch wird eine neue Computererweiterung mit der über die Pipeline bereitgestellten Identität und den Erweiterungsdetails erstellt, die vom übergebenen Erweiterungsobjekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8847d-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="8847d-122">Sie werden dies wahrscheinlich nicht tun, aber es ist möglich.</span><span class="sxs-lookup"><span data-stu-id="8847d-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="8847d-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8847d-123">PARAMETERS</span></span>

### <span data-ttu-id="8847d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8847d-124">-AsJob</span></span>
<span data-ttu-id="8847d-125">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8847d-125">Run the command as a job</span></span>

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

### <span data-ttu-id="8847d-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8847d-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8847d-127">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn sie zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8847d-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="8847d-128">Nach der Bereitstellung wird die Erweiterung jedoch nur dann ein Upgrade auf Nebenversionen durchführen, wenn sie erneut bereitgestellt wird, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8847d-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8847d-129">-DefaultProfile</span></span>
<span data-ttu-id="8847d-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8847d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8847d-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="8847d-131">-ExtensionParameter</span></span>
<span data-ttu-id="8847d-132">Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="8847d-133">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8847d-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="8847d-134">-ExtensionType</span></span>
<span data-ttu-id="8847d-135">Gibt den Typ der Erweiterung an. Ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="8847d-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="8847d-136">-ForceRerun</span></span>
<span data-ttu-id="8847d-137">So muss der Erweiterungshandler auch dann aktualisiert werden, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8847d-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8847d-138">-InputObject</span></span>
<span data-ttu-id="8847d-139">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8847d-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-140">-Location</span><span class="sxs-lookup"><span data-stu-id="8847d-140">-Location</span></span>
<span data-ttu-id="8847d-141">Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="8847d-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="8847d-142">-MachineName</span></span>
<span data-ttu-id="8847d-143">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8847d-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-144">-Name</span><span class="sxs-lookup"><span data-stu-id="8847d-144">-Name</span></span>
<span data-ttu-id="8847d-145">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8847d-146">-NoWait</span></span>
<span data-ttu-id="8847d-147">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8847d-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8847d-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="8847d-148">-ProtectedSetting</span></span>
<span data-ttu-id="8847d-149">Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8847d-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8847d-150">-Publisher</span></span>
<span data-ttu-id="8847d-151">Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="8847d-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8847d-152">-ResourceGroupName</span></span>
<span data-ttu-id="8847d-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8847d-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-154">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="8847d-154">-Setting</span></span>
<span data-ttu-id="8847d-155">Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8847d-156">-SubscriptionId</span></span>
<span data-ttu-id="8847d-157">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8847d-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8847d-158">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="8847d-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="8847d-159">-Tag</span></span>
<span data-ttu-id="8847d-160">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="8847d-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8847d-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="8847d-162">Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="8847d-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847d-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8847d-163">-Confirm</span></span>
<span data-ttu-id="8847d-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8847d-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8847d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8847d-165">-WhatIf</span></span>
<span data-ttu-id="8847d-166">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8847d-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8847d-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8847d-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8847d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8847d-168">CommonParameters</span></span>
<span data-ttu-id="8847d-169">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8847d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8847d-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8847d-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8847d-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8847d-171">INPUTS</span></span>

### <span data-ttu-id="8847d-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8847d-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="8847d-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="8847d-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="8847d-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8847d-174">OUTPUTS</span></span>

### <span data-ttu-id="8847d-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8847d-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="8847d-176">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8847d-176">NOTES</span></span>

<span data-ttu-id="8847d-177">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8847d-177">ALIASES</span></span>

<span data-ttu-id="8847d-178">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="8847d-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8847d-179">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="8847d-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8847d-180">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8847d-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8847d-181">ERWEITERUNGSPARAMETER <IMachineExtension> : Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="8847d-182">`Location <String>`: Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="8847d-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="8847d-183">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="8847d-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8847d-184">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8847d-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8847d-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn sie zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8847d-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="8847d-186">Nach der Bereitstellung wird die Erweiterung jedoch nur dann ein Upgrade auf Nebenversionen durchführen, wenn sie erneut bereitgestellt wird, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8847d-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="8847d-187">`[ForceUpdateTag <String>]`: Wie der Erweiterungshandler erzwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8847d-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="8847d-188">`[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an. Ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="8847d-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="8847d-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8847d-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="8847d-190">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="8847d-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="8847d-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="8847d-192">`[TypeHandlerVersion <String>]`: Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="8847d-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="8847d-193">INPUTOBJECT <IConnectedMachineIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="8847d-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8847d-194">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="8847d-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="8847d-195">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="8847d-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8847d-196">`[Name <String>]`: Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="8847d-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="8847d-197">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8847d-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8847d-198">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8847d-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8847d-199">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="8847d-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8847d-200">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8847d-200">RELATED LINKS</span></span>

