---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: e6da084f13d85f8c4f5a8934cd5fd4f05882c251
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948776"
---
# <span data-ttu-id="64d20-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="64d20-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="64d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d20-102">SYNOPSIS</span></span>
<span data-ttu-id="64d20-103">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="64d20-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="64d20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64d20-104">SYNTAX</span></span>

### <span data-ttu-id="64d20-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="64d20-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="64d20-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="64d20-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64d20-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64d20-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64d20-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="64d20-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64d20-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64d20-109">DESCRIPTION</span></span>
<span data-ttu-id="64d20-110">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="64d20-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="64d20-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64d20-111">EXAMPLES</span></span>

### <span data-ttu-id="64d20-112">Beispiel 1: Aktualisieren einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="64d20-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="64d20-113">Aktualisiert eine Erweiterung auf einem bestimmten Computer.</span><span class="sxs-lookup"><span data-stu-id="64d20-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="64d20-114">Beispiel 2: Aktualisieren einer Erweiterung mit über die Pipeline angegebener Position</span><span class="sxs-lookup"><span data-stu-id="64d20-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="64d20-115">Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="64d20-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="64d20-116">Hier verwenden wir die über die Pipeline übergebene Erweiterung, um zu ermitteln, für welche Erweiterung wir arbeiten möchten, und geben an, was wir über die normalen Parameter ändern möchten (z. B. `-Settings` )</span><span class="sxs-lookup"><span data-stu-id="64d20-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="64d20-117">Beispiel 3: Aktualisieren einer Erweiterung mit über die Pipeline angegebenen Erweiterungsparametern</span><span class="sxs-lookup"><span data-stu-id="64d20-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="64d20-118">Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="64d20-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="64d20-119">Hier verwenden wir die über die Pipeline übergebene Erweiterung, um die Änderungen an der Erweiterung zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="64d20-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="64d20-120">Die Position der Erweiterung wird nicht über die Pipeline abgerufen, sondern über die normal angegebenen Parameter (durch den Parameter splat).</span><span class="sxs-lookup"><span data-stu-id="64d20-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="64d20-121">Beispiel 4: Verwenden eines Erweiterungsobjekts als Speicherort und Parameter für die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="64d20-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="64d20-122">Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="64d20-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="64d20-123">Hier verwenden wir die über die Pipeline übergebene Erweiterung, um zu ermitteln, für welche Erweiterung wir arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="64d20-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="64d20-124">Darüber hinaus verwenden wir die Parameter des Erweiterungsobjekts, um anzugeben, was aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64d20-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="64d20-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="64d20-125">PARAMETERS</span></span>

### <span data-ttu-id="64d20-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64d20-126">-AsJob</span></span>
<span data-ttu-id="64d20-127">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="64d20-127">Run the command as a job</span></span>

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

### <span data-ttu-id="64d20-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="64d20-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="64d20-129">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn sie zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="64d20-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="64d20-130">Nach der Bereitstellung wird die Erweiterung jedoch nur dann ein Upgrade auf Nebenversionen durchführen, wenn sie erneut bereitgestellt wird, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64d20-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d20-131">-DefaultProfile</span></span>
<span data-ttu-id="64d20-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64d20-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64d20-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="64d20-133">-ExtensionParameter</span></span>
<span data-ttu-id="64d20-134">Beschreibt ein Computererweiterungsupdate.</span><span class="sxs-lookup"><span data-stu-id="64d20-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="64d20-135">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="64d20-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="64d20-136">-ForceRerun</span></span>
<span data-ttu-id="64d20-137">So muss der Erweiterungshandler auch dann aktualisiert werden, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="64d20-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64d20-138">-InputObject</span></span>
<span data-ttu-id="64d20-139">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="64d20-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="64d20-140">-MachineName</span></span>
<span data-ttu-id="64d20-141">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="64d20-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-142">-Name</span><span class="sxs-lookup"><span data-stu-id="64d20-142">-Name</span></span>
<span data-ttu-id="64d20-143">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="64d20-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64d20-144">-NoWait</span></span>
<span data-ttu-id="64d20-145">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="64d20-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64d20-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="64d20-146">-ProtectedSetting</span></span>
<span data-ttu-id="64d20-147">Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="64d20-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="64d20-148">-Publisher</span></span>
<span data-ttu-id="64d20-149">Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="64d20-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d20-150">-ResourceGroupName</span></span>
<span data-ttu-id="64d20-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64d20-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-152">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="64d20-152">-Setting</span></span>
<span data-ttu-id="64d20-153">Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="64d20-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64d20-154">-SubscriptionId</span></span>
<span data-ttu-id="64d20-155">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="64d20-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64d20-156">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="64d20-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="64d20-157">-Tag</span></span>
<span data-ttu-id="64d20-158">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="64d20-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-159">-Type</span><span class="sxs-lookup"><span data-stu-id="64d20-159">-Type</span></span>
<span data-ttu-id="64d20-160">Gibt den Typ der Erweiterung an. Ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="64d20-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="64d20-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="64d20-162">Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="64d20-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d20-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64d20-163">-Confirm</span></span>
<span data-ttu-id="64d20-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64d20-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d20-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d20-165">-WhatIf</span></span>
<span data-ttu-id="64d20-166">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64d20-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d20-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64d20-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d20-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d20-168">CommonParameters</span></span>
<span data-ttu-id="64d20-169">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d20-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d20-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64d20-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d20-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64d20-171">INPUTS</span></span>

### <span data-ttu-id="64d20-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="64d20-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="64d20-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="64d20-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="64d20-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64d20-174">OUTPUTS</span></span>

### <span data-ttu-id="64d20-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="64d20-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="64d20-176">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="64d20-176">NOTES</span></span>

<span data-ttu-id="64d20-177">ALIASE</span><span class="sxs-lookup"><span data-stu-id="64d20-177">ALIASES</span></span>

<span data-ttu-id="64d20-178">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="64d20-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64d20-179">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="64d20-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64d20-180">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64d20-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64d20-181">ERWEITERUNGSPARAMETER <IMachineExtensionUpdate> : Beschreibt ein Computererweiterungsupdate.</span><span class="sxs-lookup"><span data-stu-id="64d20-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="64d20-182">`[Tag <IUpdateResourceTags>]`: Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="64d20-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="64d20-183">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="64d20-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="64d20-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn sie zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="64d20-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="64d20-185">Nach der Bereitstellung wird die Erweiterung jedoch nur dann ein Upgrade auf Nebenversionen durchführen, wenn sie erneut bereitgestellt wird, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64d20-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="64d20-186">`[ForceUpdateTag <String>]`: Wie der Erweiterungshandler erzwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="64d20-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="64d20-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="64d20-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="64d20-188">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="64d20-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="64d20-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="64d20-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="64d20-190">`[Type <String>]`: Gibt den Typ der Erweiterung an. Ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="64d20-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="64d20-191">`[TypeHandlerVersion <String>]`: Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="64d20-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="64d20-192">INPUTOBJECT <IConnectedMachineIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="64d20-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64d20-193">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="64d20-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="64d20-194">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="64d20-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64d20-195">`[Name <String>]`: Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="64d20-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="64d20-196">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64d20-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="64d20-197">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="64d20-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="64d20-198">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="64d20-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="64d20-199">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="64d20-199">RELATED LINKS</span></span>

