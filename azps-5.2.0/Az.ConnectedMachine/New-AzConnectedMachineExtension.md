---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290855"
---
# <span data-ttu-id="76049-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="76049-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="76049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76049-102">SYNOPSIS</span></span>
<span data-ttu-id="76049-103">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="76049-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76049-104">SYNTAX</span></span>

### <span data-ttu-id="76049-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="76049-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="76049-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="76049-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76049-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76049-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="76049-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76049-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76049-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76049-109">DESCRIPTION</span></span>
<span data-ttu-id="76049-110">Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="76049-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76049-111">EXAMPLES</span></span>

### <span data-ttu-id="76049-112">Beispiel 1: Hinzufügen einer neuen Erweiterung zu einem Computer</span><span class="sxs-lookup"><span data-stu-id="76049-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="76049-113">Legt eine Erweiterung auf einem Computer fest.</span><span class="sxs-lookup"><span data-stu-id="76049-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="76049-114">Beispiel 2: Hinzufügen einer neuen Erweiterung mit Erweiterungsparametern, die über die Pipeline angegeben werden</span><span class="sxs-lookup"><span data-stu-id="76049-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="76049-115">Dadurch wird eine neue Erweiterung mit den Erweiterungsparametern erstellt, die von dem über die Pipeline übergebenen Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="76049-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="76049-116">Dies ist ideal, wenn Sie die Parameter eines Computers übernehmen und auf einen anderen Computer anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="76049-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="76049-117">Beispiel 3: Hinzufügen einer neuen Erweiterung mit über die Pipeline angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="76049-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="76049-118">Dadurch wird eine neue Computererweiterung erstellt, indem die über die Pipeline bereitgestellte Identität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="76049-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="76049-119">Wahrscheinlich werden Sie dies nicht tun, aber es ist möglich.</span><span class="sxs-lookup"><span data-stu-id="76049-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="76049-120">Beispiel 4: Hinzufügen einer neuen Erweiterung mithilfe eines Erweiterungsobjekts als Speicherort und Parameter für die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="76049-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="76049-121">Dadurch wird eine neue Computererweiterung erstellt, indem die über die Pipeline bereitgestellte Identität und die Erweiterungsdetails des übergebenen Erweiterungsobjekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76049-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="76049-122">Wahrscheinlich werden Sie dies nicht tun, aber es ist möglich.</span><span class="sxs-lookup"><span data-stu-id="76049-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="76049-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76049-123">PARAMETERS</span></span>

### <span data-ttu-id="76049-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76049-124">-AsJob</span></span>
<span data-ttu-id="76049-125">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="76049-125">Run the command as a job</span></span>

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

### <span data-ttu-id="76049-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="76049-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="76049-127">Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="76049-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="76049-128">Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76049-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="76049-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76049-129">-DefaultProfile</span></span>
<span data-ttu-id="76049-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76049-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76049-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="76049-131">-ExtensionParameter</span></span>
<span data-ttu-id="76049-132">Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="76049-133">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="76049-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="76049-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="76049-134">-ExtensionType</span></span>
<span data-ttu-id="76049-135">Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="76049-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="76049-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="76049-136">-ForceRerun</span></span>
<span data-ttu-id="76049-137">Die Art und Weise, wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="76049-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="76049-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76049-138">-InputObject</span></span>
<span data-ttu-id="76049-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="76049-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="76049-140">-Location</span><span class="sxs-lookup"><span data-stu-id="76049-140">-Location</span></span>
<span data-ttu-id="76049-141">Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="76049-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="76049-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="76049-142">-MachineName</span></span>
<span data-ttu-id="76049-143">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="76049-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="76049-144">-Name</span><span class="sxs-lookup"><span data-stu-id="76049-144">-Name</span></span>
<span data-ttu-id="76049-145">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="76049-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="76049-146">-NoWait</span></span>
<span data-ttu-id="76049-147">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="76049-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76049-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="76049-148">-ProtectedSetting</span></span>
<span data-ttu-id="76049-149">Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="76049-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="76049-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="76049-150">-Publisher</span></span>
<span data-ttu-id="76049-151">Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="76049-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="76049-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76049-152">-ResourceGroupName</span></span>
<span data-ttu-id="76049-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76049-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="76049-154">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="76049-154">-Setting</span></span>
<span data-ttu-id="76049-155">Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="76049-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76049-156">-SubscriptionId</span></span>
<span data-ttu-id="76049-157">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="76049-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76049-158">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="76049-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="76049-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="76049-159">-Tag</span></span>
<span data-ttu-id="76049-160">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="76049-160">Resource tags.</span></span>

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

### <span data-ttu-id="76049-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="76049-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="76049-162">Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="76049-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="76049-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76049-163">-Confirm</span></span>
<span data-ttu-id="76049-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76049-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76049-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76049-165">-WhatIf</span></span>
<span data-ttu-id="76049-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76049-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76049-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76049-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76049-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76049-168">CommonParameters</span></span>
<span data-ttu-id="76049-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76049-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76049-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76049-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76049-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76049-171">INPUTS</span></span>

### <span data-ttu-id="76049-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="76049-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="76049-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="76049-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="76049-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76049-174">OUTPUTS</span></span>

### <span data-ttu-id="76049-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="76049-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="76049-176">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76049-176">NOTES</span></span>

<span data-ttu-id="76049-177">ALIASE</span><span class="sxs-lookup"><span data-stu-id="76049-177">ALIASES</span></span>

<span data-ttu-id="76049-178">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="76049-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76049-179">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="76049-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76049-180">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76049-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76049-181"><IMachineExtension>EXTENSIONPARAMETER: Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="76049-182">`Location <String>`: Der geo-Standort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="76049-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="76049-183">`[Tag <ITrackedResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="76049-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="76049-184">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="76049-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="76049-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="76049-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="76049-186">Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="76049-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="76049-187">`[ForceUpdateTag <String>]`: Wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="76049-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="76049-188">`[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="76049-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="76049-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="76049-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="76049-190">`[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.</span><span class="sxs-lookup"><span data-stu-id="76049-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="76049-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="76049-192">`[TypeHandlerVersion <String>]`: Gibt die Version des Skripthandlers an.</span><span class="sxs-lookup"><span data-stu-id="76049-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="76049-193">INPUTOBJECT <IConnectedMachineIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="76049-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76049-194">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="76049-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="76049-195">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="76049-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76049-196">`[Name <String>]`: Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="76049-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="76049-197">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76049-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="76049-198">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="76049-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76049-199">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="76049-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="76049-200">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76049-200">RELATED LINKS</span></span>

