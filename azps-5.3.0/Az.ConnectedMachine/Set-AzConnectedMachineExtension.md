---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470801"
---
# <span data-ttu-id="b95f4-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="b95f4-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="b95f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b95f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b95f4-103">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b95f4-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="b95f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b95f4-104">SYNTAX</span></span>

### <span data-ttu-id="b95f4-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="b95f4-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b95f4-106">Update</span><span class="sxs-lookup"><span data-stu-id="b95f4-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b95f4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b95f4-107">DESCRIPTION</span></span>
<span data-ttu-id="b95f4-108">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b95f4-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="b95f4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b95f4-109">EXAMPLES</span></span>

### <span data-ttu-id="b95f4-110">Beispiel 1: Festlegen einer Erweiterung auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="b95f4-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="b95f4-111">Legt eine Erweiterung auf einem Computer fest.</span><span class="sxs-lookup"><span data-stu-id="b95f4-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="b95f4-112">Beispiel 2: Festlegen einer Erweiterung mit Erweiterungsparametern, die über die Pipeline angegeben werden</span><span class="sxs-lookup"><span data-stu-id="b95f4-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="b95f4-113">Dadurch wird eine Erweiterung mit den Erweiterungsparametern festgelegt, die von dem über die Pipeline übergebenen Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b95f4-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="b95f4-114">Dies ist ideal, wenn Sie die Parameter eines Computers übernehmen und auf einen anderen Computer anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b95f4-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="b95f4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b95f4-115">PARAMETERS</span></span>

### <span data-ttu-id="b95f4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b95f4-116">-AsJob</span></span>
<span data-ttu-id="b95f4-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b95f4-117">Run the command as a job</span></span>

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

### <span data-ttu-id="b95f4-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b95f4-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b95f4-119">Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b95f4-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="b95f4-120">Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b95f4-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95f4-121">-DefaultProfile</span></span>
<span data-ttu-id="b95f4-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b95f4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b95f4-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="b95f4-123">-ExtensionParameter</span></span>
<span data-ttu-id="b95f4-124">Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="b95f4-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="b95f4-125">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b95f4-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="b95f4-126">-ExtensionType</span></span>
<span data-ttu-id="b95f4-127">Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="b95f4-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="b95f4-128">-ForceRerun</span></span>
<span data-ttu-id="b95f4-129">Die Art und Weise, wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b95f4-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-130">-Location</span><span class="sxs-lookup"><span data-stu-id="b95f4-130">-Location</span></span>
<span data-ttu-id="b95f4-131">Der geo-Standort, in dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="b95f4-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="b95f4-132">-MachineName</span></span>
<span data-ttu-id="b95f4-133">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b95f4-133">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b95f4-134">-Name</span></span>
<span data-ttu-id="b95f4-135">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="b95f4-135">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b95f4-136">-NoWait</span></span>
<span data-ttu-id="b95f4-137">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b95f4-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b95f4-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="b95f4-138">-ProtectedSetting</span></span>
<span data-ttu-id="b95f4-139">Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b95f4-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b95f4-140">-Publisher</span></span>
<span data-ttu-id="b95f4-141">Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="b95f4-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b95f4-142">-ResourceGroupName</span></span>
<span data-ttu-id="b95f4-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b95f4-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-144">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="b95f4-144">-Setting</span></span>
<span data-ttu-id="b95f4-145">In Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b95f4-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b95f4-146">-SubscriptionId</span></span>
<span data-ttu-id="b95f4-147">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b95f4-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b95f4-148">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="b95f4-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="b95f4-149">-Tag</span></span>
<span data-ttu-id="b95f4-150">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="b95f4-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b95f4-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="b95f4-152">Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="b95f4-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95f4-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b95f4-153">-Confirm</span></span>
<span data-ttu-id="b95f4-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b95f4-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b95f4-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b95f4-155">-WhatIf</span></span>
<span data-ttu-id="b95f4-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b95f4-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b95f4-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b95f4-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b95f4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95f4-158">CommonParameters</span></span>
<span data-ttu-id="b95f4-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95f4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95f4-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b95f4-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95f4-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b95f4-161">INPUTS</span></span>

### <span data-ttu-id="b95f4-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="b95f4-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="b95f4-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b95f4-163">OUTPUTS</span></span>

### <span data-ttu-id="b95f4-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="b95f4-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="b95f4-165">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b95f4-165">NOTES</span></span>

<span data-ttu-id="b95f4-166">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b95f4-166">ALIASES</span></span>

<span data-ttu-id="b95f4-167">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b95f4-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b95f4-168">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b95f4-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b95f4-169">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b95f4-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b95f4-170">EXTENSIONPARAMETER <IMachineExtension> : Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="b95f4-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="b95f4-171">`Location <String>`: Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="b95f4-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="b95f4-172">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="b95f4-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="b95f4-173">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b95f4-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b95f4-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b95f4-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="b95f4-175">Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b95f4-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="b95f4-176">`[ForceUpdateTag <String>]`: Wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b95f4-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="b95f4-177">`[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="b95f4-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="b95f4-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b95f4-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="b95f4-179">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="b95f4-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="b95f4-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b95f4-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="b95f4-181">`[TypeHandlerVersion <String>]`: Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="b95f4-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="b95f4-182">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b95f4-182">RELATED LINKS</span></span>

