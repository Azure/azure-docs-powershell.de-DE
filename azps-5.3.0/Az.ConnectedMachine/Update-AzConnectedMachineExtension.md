---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472894"
---
# <span data-ttu-id="6be9c-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6be9c-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="6be9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6be9c-102">SYNOPSIS</span></span>
<span data-ttu-id="6be9c-103">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="6be9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6be9c-104">SYNTAX</span></span>

### <span data-ttu-id="6be9c-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="6be9c-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6be9c-106">Update</span><span class="sxs-lookup"><span data-stu-id="6be9c-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6be9c-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6be9c-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6be9c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6be9c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6be9c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6be9c-109">DESCRIPTION</span></span>
<span data-ttu-id="6be9c-110">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="6be9c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6be9c-111">EXAMPLES</span></span>

### <span data-ttu-id="6be9c-112">Beispiel 1: Aktualisieren einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="6be9c-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="6be9c-113">Aktualisiert eine Erweiterung auf einem bestimmten Computer.</span><span class="sxs-lookup"><span data-stu-id="6be9c-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="6be9c-114">Beispiel 2: Aktualisieren einer Erweiterung mit dem über die Pipeline angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="6be9c-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="6be9c-115">Aktualisiert eine bestimmte, über die Pipeline übergebene Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="6be9c-116">Hier verwenden wir die über die Pipeline übergebene Erweiterung, um uns zu identifizieren, mit welcher Erweiterung wir arbeiten möchten, und geben an, was wir mithilfe der normalen Parameter ändern möchten (z. B. `-Settings` )</span><span class="sxs-lookup"><span data-stu-id="6be9c-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="6be9c-117">Beispiel 3: Aktualisieren einer Erweiterung mit Erweiterungsparametern, die über die Pipeline angegeben werden</span><span class="sxs-lookup"><span data-stu-id="6be9c-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="6be9c-118">Aktualisiert eine bestimmte, über die Pipeline übergebene Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="6be9c-119">Hier verwenden wir die über die Pipeline übergebene Erweiterung, um die Änderungen vorzunehmen, die wir an der Erweiterung vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="6be9c-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="6be9c-120">Der Speicherort der Erweiterung wird nicht über die Pipeline abgerufen, sondern über die normal angegebenen Parameter (durch den Parameter "splat").</span><span class="sxs-lookup"><span data-stu-id="6be9c-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="6be9c-121">Beispiel 4: Verwenden eines Erweiterungsobjekts als Speicherort und Parameter für die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="6be9c-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="6be9c-122">Aktualisiert eine bestimmte, über die Pipeline übergebene Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="6be9c-123">Hier verwenden wir die über die Pipeline übergebene Erweiterung, um uns zu identifizieren, mit welcher Erweiterung wir arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="6be9c-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="6be9c-124">Darüber hinaus verwenden wir die Parameter des Erweiterungsobjekts, um anzugeben, was aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6be9c-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="6be9c-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6be9c-125">PARAMETERS</span></span>

### <span data-ttu-id="6be9c-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6be9c-126">-AsJob</span></span>
<span data-ttu-id="6be9c-127">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="6be9c-127">Run the command as a job</span></span>

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

### <span data-ttu-id="6be9c-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6be9c-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6be9c-129">Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6be9c-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="6be9c-130">Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6be9c-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="6be9c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be9c-131">-DefaultProfile</span></span>
<span data-ttu-id="6be9c-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6be9c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be9c-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="6be9c-133">-ExtensionParameter</span></span>
<span data-ttu-id="6be9c-134">Beschreibt ein Computererweiterungsupdate.</span><span class="sxs-lookup"><span data-stu-id="6be9c-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="6be9c-135">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6be9c-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="6be9c-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="6be9c-136">-ForceRerun</span></span>
<span data-ttu-id="6be9c-137">Die Art und Weise, wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6be9c-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="6be9c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6be9c-138">-InputObject</span></span>
<span data-ttu-id="6be9c-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="6be9c-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6be9c-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="6be9c-140">-MachineName</span></span>
<span data-ttu-id="6be9c-141">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6be9c-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="6be9c-142">-Name</span><span class="sxs-lookup"><span data-stu-id="6be9c-142">-Name</span></span>
<span data-ttu-id="6be9c-143">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="6be9c-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6be9c-144">-NoWait</span></span>
<span data-ttu-id="6be9c-145">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="6be9c-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6be9c-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="6be9c-146">-ProtectedSetting</span></span>
<span data-ttu-id="6be9c-147">Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6be9c-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="6be9c-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6be9c-148">-Publisher</span></span>
<span data-ttu-id="6be9c-149">Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="6be9c-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="6be9c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be9c-150">-ResourceGroupName</span></span>
<span data-ttu-id="6be9c-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6be9c-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="6be9c-152">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="6be9c-152">-Setting</span></span>
<span data-ttu-id="6be9c-153">Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="6be9c-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6be9c-154">-SubscriptionId</span></span>
<span data-ttu-id="6be9c-155">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6be9c-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6be9c-156">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="6be9c-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6be9c-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="6be9c-157">-Tag</span></span>
<span data-ttu-id="6be9c-158">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="6be9c-158">Resource tags</span></span>

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

### <span data-ttu-id="6be9c-159">-Type</span><span class="sxs-lookup"><span data-stu-id="6be9c-159">-Type</span></span>
<span data-ttu-id="6be9c-160">Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="6be9c-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="6be9c-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6be9c-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="6be9c-162">Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="6be9c-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="6be9c-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6be9c-163">-Confirm</span></span>
<span data-ttu-id="6be9c-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6be9c-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6be9c-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6be9c-165">-WhatIf</span></span>
<span data-ttu-id="6be9c-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6be9c-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6be9c-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6be9c-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6be9c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be9c-168">CommonParameters</span></span>
<span data-ttu-id="6be9c-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6be9c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be9c-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6be9c-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be9c-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6be9c-171">INPUTS</span></span>

### <span data-ttu-id="6be9c-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="6be9c-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="6be9c-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="6be9c-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="6be9c-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6be9c-174">OUTPUTS</span></span>

### <span data-ttu-id="6be9c-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6be9c-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="6be9c-176">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6be9c-176">NOTES</span></span>

<span data-ttu-id="6be9c-177">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6be9c-177">ALIASES</span></span>

<span data-ttu-id="6be9c-178">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6be9c-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6be9c-179">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6be9c-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6be9c-180">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6be9c-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6be9c-181"><IMachineExtensionUpdate>EXTENSIONPARAMETER: Beschreibt ein Computererweiterungsupdate.</span><span class="sxs-lookup"><span data-stu-id="6be9c-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="6be9c-182">`[Tag <IUpdateResourceTags>]`: Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="6be9c-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="6be9c-183">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="6be9c-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6be9c-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6be9c-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="6be9c-185">Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6be9c-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="6be9c-186">`[ForceUpdateTag <String>]`: Wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6be9c-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="6be9c-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6be9c-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="6be9c-188">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="6be9c-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="6be9c-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="6be9c-190">`[Type <String>]`: Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="6be9c-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="6be9c-191">`[TypeHandlerVersion <String>]`: Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="6be9c-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="6be9c-192">INPUTOBJECT <IConnectedMachineIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="6be9c-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6be9c-193">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="6be9c-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="6be9c-194">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6be9c-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6be9c-195">`[Name <String>]`: Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="6be9c-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="6be9c-196">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6be9c-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6be9c-197">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6be9c-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6be9c-198">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="6be9c-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6be9c-199">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6be9c-199">RELATED LINKS</span></span>

