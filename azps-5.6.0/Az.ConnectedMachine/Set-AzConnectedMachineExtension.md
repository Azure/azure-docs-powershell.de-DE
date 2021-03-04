---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: accea82dd6594d71f627d6c3e32943d004fa35e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948787"
---
# <span data-ttu-id="37408-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="37408-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="37408-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37408-102">SYNOPSIS</span></span>
<span data-ttu-id="37408-103">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="37408-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="37408-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37408-104">SYNTAX</span></span>

### <span data-ttu-id="37408-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="37408-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="37408-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="37408-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37408-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37408-107">DESCRIPTION</span></span>
<span data-ttu-id="37408-108">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="37408-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="37408-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37408-109">EXAMPLES</span></span>

### <span data-ttu-id="37408-110">Beispiel 1: Festlegen einer Erweiterung auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="37408-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="37408-111">Legt eine Erweiterung auf einem Computer fest.</span><span class="sxs-lookup"><span data-stu-id="37408-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="37408-112">Beispiel 2: Festlegen einer Erweiterung mit über die Pipeline angegebenen Erweiterungsparametern</span><span class="sxs-lookup"><span data-stu-id="37408-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="37408-113">Dadurch wird eine Erweiterung mit den Erweiterungsparametern festgelegt, die vom über die Pipeline übergebenen Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="37408-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="37408-114">Dies ist großartig, wenn Sie die Parameter eines Computers übernehmen und auf einen anderen Computer anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="37408-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="37408-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="37408-115">PARAMETERS</span></span>

### <span data-ttu-id="37408-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37408-116">-AsJob</span></span>
<span data-ttu-id="37408-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="37408-117">Run the command as a job</span></span>

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

### <span data-ttu-id="37408-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="37408-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="37408-119">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn sie zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37408-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="37408-120">Nach der Bereitstellung wird die Erweiterung jedoch nur dann ein Upgrade auf Nebenversionen durchführen, wenn sie erneut bereitgestellt wird, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="37408-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="37408-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37408-121">-DefaultProfile</span></span>
<span data-ttu-id="37408-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37408-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37408-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="37408-123">-ExtensionParameter</span></span>
<span data-ttu-id="37408-124">Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="37408-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="37408-125">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="37408-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="37408-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="37408-126">-ExtensionType</span></span>
<span data-ttu-id="37408-127">Gibt den Typ der Erweiterung an. Ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="37408-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="37408-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="37408-128">-ForceRerun</span></span>
<span data-ttu-id="37408-129">So muss der Erweiterungshandler auch dann aktualisiert werden, wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="37408-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="37408-130">-Location</span><span class="sxs-lookup"><span data-stu-id="37408-130">-Location</span></span>
<span data-ttu-id="37408-131">Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="37408-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="37408-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="37408-132">-MachineName</span></span>
<span data-ttu-id="37408-133">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="37408-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="37408-134">-Name</span><span class="sxs-lookup"><span data-stu-id="37408-134">-Name</span></span>
<span data-ttu-id="37408-135">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="37408-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="37408-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="37408-136">-NoWait</span></span>
<span data-ttu-id="37408-137">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="37408-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="37408-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="37408-138">-ProtectedSetting</span></span>
<span data-ttu-id="37408-139">Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="37408-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="37408-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="37408-140">-Publisher</span></span>
<span data-ttu-id="37408-141">Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="37408-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="37408-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37408-142">-ResourceGroupName</span></span>
<span data-ttu-id="37408-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37408-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="37408-144">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="37408-144">-Setting</span></span>
<span data-ttu-id="37408-145">Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="37408-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="37408-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37408-146">-SubscriptionId</span></span>
<span data-ttu-id="37408-147">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="37408-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="37408-148">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="37408-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37408-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="37408-149">-Tag</span></span>
<span data-ttu-id="37408-150">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="37408-150">Resource tags.</span></span>

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

### <span data-ttu-id="37408-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="37408-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="37408-152">Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="37408-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="37408-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37408-153">-Confirm</span></span>
<span data-ttu-id="37408-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37408-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37408-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37408-155">-WhatIf</span></span>
<span data-ttu-id="37408-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37408-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37408-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37408-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37408-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37408-158">CommonParameters</span></span>
<span data-ttu-id="37408-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37408-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37408-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37408-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37408-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37408-161">INPUTS</span></span>

### <span data-ttu-id="37408-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="37408-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="37408-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37408-163">OUTPUTS</span></span>

### <span data-ttu-id="37408-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="37408-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="37408-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="37408-165">NOTES</span></span>

<span data-ttu-id="37408-166">ALIASE</span><span class="sxs-lookup"><span data-stu-id="37408-166">ALIASES</span></span>

<span data-ttu-id="37408-167">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="37408-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37408-168">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="37408-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37408-169">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37408-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37408-170">ERWEITERUNGSPARAMETER <IMachineExtension> : Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="37408-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="37408-171">`Location <String>`: Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="37408-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="37408-172">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="37408-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="37408-173">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="37408-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="37408-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn sie zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37408-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="37408-175">Nach der Bereitstellung wird die Erweiterung jedoch nur dann ein Upgrade auf Nebenversionen durchführen, wenn sie erneut bereitgestellt wird, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="37408-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="37408-176">`[ForceUpdateTag <String>]`: Wie der Erweiterungshandler erzwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="37408-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="37408-177">`[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an. Ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="37408-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="37408-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder gar keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="37408-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="37408-179">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="37408-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="37408-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="37408-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="37408-181">`[TypeHandlerVersion <String>]`: Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="37408-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="37408-182">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="37408-182">RELATED LINKS</span></span>

