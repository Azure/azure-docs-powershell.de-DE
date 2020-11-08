---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178938"
---
# <span data-ttu-id="f0bd1-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f0bd1-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="f0bd1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bd1-103">Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="f0bd1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0bd1-104">SYNTAX</span></span>

### <span data-ttu-id="f0bd1-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0bd1-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f0bd1-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="f0bd1-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0bd1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0bd1-107">DESCRIPTION</span></span>
<span data-ttu-id="f0bd1-108">Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="f0bd1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0bd1-109">EXAMPLES</span></span>

### <span data-ttu-id="f0bd1-110">Beispiel 1: Einrichten einer Erweiterung auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="f0bd1-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="f0bd1-111">Legt eine Erweiterung auf einem Computer fest.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="f0bd1-112">Beispiel 2: Einrichten einer Erweiterung mit den über die Pipeline angegebenen Erweiterungs Parametern</span><span class="sxs-lookup"><span data-stu-id="f0bd1-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="f0bd1-113">Dadurch wird eine Erweiterung mit den Erweiterungs Parametern festgelegt, die von dem über die Pipeline übergebenen Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="f0bd1-114">Das ist großartig, wenn Sie die Parameter eines Rechners angreifen und auf einen anderen Computer anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="f0bd1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0bd1-115">PARAMETERS</span></span>

### <span data-ttu-id="f0bd1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0bd1-116">-AsJob</span></span>
<span data-ttu-id="f0bd1-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f0bd1-117">Run the command as a job</span></span>

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

### <span data-ttu-id="f0bd1-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f0bd1-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f0bd1-119">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="f0bd1-120">Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="f0bd1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bd1-121">-DefaultProfile</span></span>
<span data-ttu-id="f0bd1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0bd1-123">-Extensionparameter</span><span class="sxs-lookup"><span data-stu-id="f0bd1-123">-ExtensionParameter</span></span>
<span data-ttu-id="f0bd1-124">Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="f0bd1-125">Informationen zu Konstrukten finden Sie unter Abschnitt "Notizen" für extensionparameter-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="f0bd1-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f0bd1-126">-ExtensionType</span></span>
<span data-ttu-id="f0bd1-127">Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="f0bd1-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="f0bd1-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f0bd1-128">-ForceRerun</span></span>
<span data-ttu-id="f0bd1-129">Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn die Erweiterungskonfiguration nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="f0bd1-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="f0bd1-130">-Location</span></span>
<span data-ttu-id="f0bd1-131">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="f0bd1-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="f0bd1-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="f0bd1-132">-MachineName</span></span>
<span data-ttu-id="f0bd1-133">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="f0bd1-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f0bd1-134">-Name</span></span>
<span data-ttu-id="f0bd1-135">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="f0bd1-136">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f0bd1-136">-NoWait</span></span>
<span data-ttu-id="f0bd1-137">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f0bd1-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f0bd1-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="f0bd1-138">-ProtectedSetting</span></span>
<span data-ttu-id="f0bd1-139">Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="f0bd1-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f0bd1-140">-Publisher</span></span>
<span data-ttu-id="f0bd1-141">Der Name des Erweiterungs Handlers Publisher.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="f0bd1-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0bd1-142">-ResourceGroupName</span></span>
<span data-ttu-id="f0bd1-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0bd1-144">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="f0bd1-144">-Setting</span></span>
<span data-ttu-id="f0bd1-145">Mit JSON formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="f0bd1-146">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f0bd1-146">-SubscriptionId</span></span>
<span data-ttu-id="f0bd1-147">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f0bd1-148">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f0bd1-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0bd1-149">-Tag</span></span>
<span data-ttu-id="f0bd1-150">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-150">Resource tags.</span></span>

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

### <span data-ttu-id="f0bd1-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f0bd1-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="f0bd1-152">Gibt die Version des Skript Handlers an.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="f0bd1-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0bd1-153">-Confirm</span></span>
<span data-ttu-id="f0bd1-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0bd1-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0bd1-155">-WhatIf</span></span>
<span data-ttu-id="f0bd1-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0bd1-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0bd1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bd1-158">CommonParameters</span></span>
<span data-ttu-id="f0bd1-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bd1-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0bd1-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bd1-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0bd1-161">INPUTS</span></span>

### <span data-ttu-id="f0bd1-162">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f0bd1-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="f0bd1-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0bd1-163">OUTPUTS</span></span>

### <span data-ttu-id="f0bd1-164">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f0bd1-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="f0bd1-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0bd1-165">NOTES</span></span>

<span data-ttu-id="f0bd1-166">Aliase</span><span class="sxs-lookup"><span data-stu-id="f0bd1-166">ALIASES</span></span>

<span data-ttu-id="f0bd1-167">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0bd1-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0bd1-168">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0bd1-169">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0bd1-170">Extensionparameter <IMachineExtension> : Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="f0bd1-171">`Location <String>`: Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="f0bd1-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="f0bd1-172">`[Tag <ITrackedResourceTags>]`: Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f0bd1-173">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f0bd1-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="f0bd1-175">Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="f0bd1-176">`[ForceUpdateTag <String>]`: Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="f0bd1-177">`[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="f0bd1-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="f0bd1-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="f0bd1-179">`[Publisher <String>]`: Der Name des Erweiterungs Handlers Publisher.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="f0bd1-180">`[Setting <IMachineExtensionPropertiesSettings>]`: JSON-formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="f0bd1-181">`[TypeHandlerVersion <String>]`: Gibt die Version des Skript Handlers an.</span><span class="sxs-lookup"><span data-stu-id="f0bd1-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="f0bd1-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0bd1-182">RELATED LINKS</span></span>

