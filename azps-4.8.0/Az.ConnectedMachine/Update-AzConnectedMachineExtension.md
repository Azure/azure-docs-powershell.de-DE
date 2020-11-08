---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009290"
---
# <span data-ttu-id="99c29-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="99c29-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="99c29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99c29-102">SYNOPSIS</span></span>
<span data-ttu-id="99c29-103">Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="99c29-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="99c29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c29-104">SYNTAX</span></span>

### <span data-ttu-id="99c29-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="99c29-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="99c29-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="99c29-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99c29-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99c29-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99c29-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="99c29-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99c29-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99c29-109">DESCRIPTION</span></span>
<span data-ttu-id="99c29-110">Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="99c29-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="99c29-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99c29-111">EXAMPLES</span></span>

### <span data-ttu-id="99c29-112">Beispiel 1: Aktualisieren einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="99c29-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="99c29-113">Aktualisiert eine Erweiterung auf einem bestimmten Computer.</span><span class="sxs-lookup"><span data-stu-id="99c29-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="99c29-114">Beispiel 2: Aktualisieren einer Erweiterung mit dem über die Pipeline angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="99c29-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="99c29-115">Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="99c29-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="99c29-116">Hier verwenden wir die Erweiterung, die über die Pipeline übergeben wurde, um uns zu helfen, zu ermitteln, welche Erweiterung wir betreiben möchten, und wir spezifizieren, was wir über die normalen Parameter (wie) ändern möchten. `-Settings`</span><span class="sxs-lookup"><span data-stu-id="99c29-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="99c29-117">Beispiel 3: Aktualisieren einer Erweiterung mit Erweiterungs Parametern, die über die Pipeline angegeben werden</span><span class="sxs-lookup"><span data-stu-id="99c29-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="99c29-118">Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="99c29-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="99c29-119">Hier verwenden wir die Erweiterung, die über die Pipeline übergeben wird, um die Änderungen bereitzustellen, die wir für die Erweiterung vornehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="99c29-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="99c29-120">Der Speicherort der Erweiterung wird nicht über die Pipeline abgerufen, sondern über die normalerweise angegebenen Parameter (durch den splat-Parameter).</span><span class="sxs-lookup"><span data-stu-id="99c29-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="99c29-121">Beispiel 4: Verwenden eines Erweiterungsobjekts als Speicherort und Parameter für die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="99c29-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="99c29-122">Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="99c29-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="99c29-123">Hier verwenden wir die Erweiterung, die über die Pipeline übergeben wurde, um uns zu helfen, die Erweiterung zu ermitteln, auf der wir arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="99c29-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="99c29-124">Darüber hinaus verwenden wir die Parameter des Extension-Objekts, um anzugeben, was aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="99c29-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="99c29-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="99c29-125">PARAMETERS</span></span>

### <span data-ttu-id="99c29-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99c29-126">-AsJob</span></span>
<span data-ttu-id="99c29-127">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="99c29-127">Run the command as a job</span></span>

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

### <span data-ttu-id="99c29-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="99c29-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="99c29-129">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="99c29-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="99c29-130">Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="99c29-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="99c29-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c29-131">-DefaultProfile</span></span>
<span data-ttu-id="99c29-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99c29-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c29-133">-Extensionparameter</span><span class="sxs-lookup"><span data-stu-id="99c29-133">-ExtensionParameter</span></span>
<span data-ttu-id="99c29-134">Beschreibt eine Aktualisierung der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="99c29-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="99c29-135">Informationen zu Konstrukten finden Sie unter Abschnitt "Notizen" für extensionparameter-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="99c29-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="99c29-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="99c29-136">-ForceRerun</span></span>
<span data-ttu-id="99c29-137">Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn die Erweiterungskonfiguration nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="99c29-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="99c29-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="99c29-138">-InputObject</span></span>
<span data-ttu-id="99c29-139">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="99c29-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99c29-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="99c29-140">-MachineName</span></span>
<span data-ttu-id="99c29-141">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="99c29-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="99c29-142">-Name</span><span class="sxs-lookup"><span data-stu-id="99c29-142">-Name</span></span>
<span data-ttu-id="99c29-143">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="99c29-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="99c29-144">-Nowait</span><span class="sxs-lookup"><span data-stu-id="99c29-144">-NoWait</span></span>
<span data-ttu-id="99c29-145">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="99c29-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="99c29-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="99c29-146">-ProtectedSetting</span></span>
<span data-ttu-id="99c29-147">Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="99c29-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="99c29-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="99c29-148">-Publisher</span></span>
<span data-ttu-id="99c29-149">Der Name des Erweiterungs Handlers Publisher.</span><span class="sxs-lookup"><span data-stu-id="99c29-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="99c29-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c29-150">-ResourceGroupName</span></span>
<span data-ttu-id="99c29-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99c29-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="99c29-152">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="99c29-152">-Setting</span></span>
<span data-ttu-id="99c29-153">Mit JSON formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="99c29-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="99c29-154">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="99c29-154">-SubscriptionId</span></span>
<span data-ttu-id="99c29-155">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="99c29-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99c29-156">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="99c29-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99c29-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="99c29-157">-Tag</span></span>
<span data-ttu-id="99c29-158">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="99c29-158">Resource tags</span></span>

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

### <span data-ttu-id="99c29-159">-Typ</span><span class="sxs-lookup"><span data-stu-id="99c29-159">-Type</span></span>
<span data-ttu-id="99c29-160">Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="99c29-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="99c29-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="99c29-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="99c29-162">Gibt die Version des Skript Handlers an.</span><span class="sxs-lookup"><span data-stu-id="99c29-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="99c29-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99c29-163">-Confirm</span></span>
<span data-ttu-id="99c29-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99c29-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c29-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c29-165">-WhatIf</span></span>
<span data-ttu-id="99c29-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99c29-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c29-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99c29-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c29-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c29-168">CommonParameters</span></span>
<span data-ttu-id="99c29-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c29-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c29-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99c29-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c29-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99c29-171">INPUTS</span></span>

### <span data-ttu-id="99c29-172">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="99c29-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="99c29-173">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="99c29-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="99c29-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99c29-174">OUTPUTS</span></span>

### <span data-ttu-id="99c29-175">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="99c29-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="99c29-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="99c29-176">NOTES</span></span>

<span data-ttu-id="99c29-177">Aliase</span><span class="sxs-lookup"><span data-stu-id="99c29-177">ALIASES</span></span>

<span data-ttu-id="99c29-178">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99c29-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99c29-179">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99c29-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99c29-180">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="99c29-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99c29-181">Extensionparameter <IMachineExtensionUpdate> : Beschreibt eine Computer Erweiterungs Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="99c29-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="99c29-182">`[Tag <IUpdateResourceTags>]`: Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="99c29-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="99c29-183">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="99c29-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="99c29-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="99c29-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="99c29-185">Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="99c29-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="99c29-186">`[ForceUpdateTag <String>]`: Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="99c29-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="99c29-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="99c29-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="99c29-188">`[Publisher <String>]`: Der Name des Erweiterungs Handlers Publisher.</span><span class="sxs-lookup"><span data-stu-id="99c29-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="99c29-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: JSON-formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="99c29-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="99c29-190">`[Type <String>]`: Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="99c29-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="99c29-191">`[TypeHandlerVersion <String>]`: Gibt die Version des Skript Handlers an.</span><span class="sxs-lookup"><span data-stu-id="99c29-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="99c29-192">Inputobject <IConnectedMachineIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="99c29-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99c29-193">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="99c29-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="99c29-194">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="99c29-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99c29-195">`[Name <String>]`: Der Name der hybridmaschine.</span><span class="sxs-lookup"><span data-stu-id="99c29-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="99c29-196">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99c29-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="99c29-197">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="99c29-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="99c29-198">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="99c29-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="99c29-199">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99c29-199">RELATED LINKS</span></span>

