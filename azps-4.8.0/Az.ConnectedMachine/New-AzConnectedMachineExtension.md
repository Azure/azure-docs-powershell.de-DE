---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175302"
---
# <span data-ttu-id="94301-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="94301-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="94301-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94301-102">SYNOPSIS</span></span>
<span data-ttu-id="94301-103">Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="94301-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="94301-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94301-104">SYNTAX</span></span>

### <span data-ttu-id="94301-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="94301-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="94301-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="94301-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="94301-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94301-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="94301-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="94301-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="94301-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94301-109">DESCRIPTION</span></span>
<span data-ttu-id="94301-110">Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="94301-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="94301-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94301-111">EXAMPLES</span></span>

### <span data-ttu-id="94301-112">Beispiel 1: Hinzufügen einer neuen Erweiterung zu einem Computer</span><span class="sxs-lookup"><span data-stu-id="94301-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="94301-113">Legt eine Erweiterung auf einem Computer fest.</span><span class="sxs-lookup"><span data-stu-id="94301-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="94301-114">Beispiel 2: Hinzufügen einer neuen Erweiterung mit Erweiterungs Parametern, die über die Pipeline angegeben werden</span><span class="sxs-lookup"><span data-stu-id="94301-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="94301-115">Dadurch wird eine neue Erweiterung mit den Erweiterungs Parametern erstellt, die von dem über die Pipeline übergebenen Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="94301-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="94301-116">Das ist großartig, wenn Sie die Parameter eines Rechners angreifen und auf einen anderen Computer anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="94301-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="94301-117">Beispiel 3: Hinzufügen einer neuen Erweiterung mit dem über die Pipeline angegebenen Speicherort</span><span class="sxs-lookup"><span data-stu-id="94301-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="94301-118">Dadurch wird eine neue Computererweiterung mithilfe der Identität erstellt, die über die Pipeline bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="94301-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="94301-119">Wahrscheinlich tun Sie dies nicht, aber es ist möglich.</span><span class="sxs-lookup"><span data-stu-id="94301-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="94301-120">Beispiel 4: Hinzufügen einer neuen Erweiterung mit einem Erweiterungsobjekt als Speicherort und Parameter für die Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="94301-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="94301-121">Dadurch wird eine neue Computererweiterung mithilfe der Identität erstellt, die über die Pipeline bereitgestellt wird, und die Erweiterungs Details, die vom übergebenen Erweiterungsobjekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="94301-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="94301-122">Wahrscheinlich tun Sie dies nicht, aber es ist möglich.</span><span class="sxs-lookup"><span data-stu-id="94301-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="94301-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="94301-123">PARAMETERS</span></span>

### <span data-ttu-id="94301-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94301-124">-AsJob</span></span>
<span data-ttu-id="94301-125">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="94301-125">Run the command as a job</span></span>

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

### <span data-ttu-id="94301-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="94301-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="94301-127">Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="94301-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="94301-128">Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="94301-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="94301-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94301-129">-DefaultProfile</span></span>
<span data-ttu-id="94301-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94301-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94301-131">-Extensionparameter</span><span class="sxs-lookup"><span data-stu-id="94301-131">-ExtensionParameter</span></span>
<span data-ttu-id="94301-132">Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="94301-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="94301-133">Informationen zu Konstrukten finden Sie unter Abschnitt "Notizen" für extensionparameter-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="94301-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="94301-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="94301-134">-ExtensionType</span></span>
<span data-ttu-id="94301-135">Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="94301-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="94301-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="94301-136">-ForceRerun</span></span>
<span data-ttu-id="94301-137">Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn die Erweiterungskonfiguration nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="94301-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="94301-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94301-138">-InputObject</span></span>
<span data-ttu-id="94301-139">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="94301-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94301-140">-Standort</span><span class="sxs-lookup"><span data-stu-id="94301-140">-Location</span></span>
<span data-ttu-id="94301-141">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="94301-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="94301-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="94301-142">-MachineName</span></span>
<span data-ttu-id="94301-143">Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="94301-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="94301-144">-Name</span><span class="sxs-lookup"><span data-stu-id="94301-144">-Name</span></span>
<span data-ttu-id="94301-145">Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="94301-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="94301-146">-Nowait</span><span class="sxs-lookup"><span data-stu-id="94301-146">-NoWait</span></span>
<span data-ttu-id="94301-147">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="94301-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="94301-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="94301-148">-ProtectedSetting</span></span>
<span data-ttu-id="94301-149">Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="94301-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="94301-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="94301-150">-Publisher</span></span>
<span data-ttu-id="94301-151">Der Name des Erweiterungs Handlers Publisher.</span><span class="sxs-lookup"><span data-stu-id="94301-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="94301-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94301-152">-ResourceGroupName</span></span>
<span data-ttu-id="94301-153">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94301-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="94301-154">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="94301-154">-Setting</span></span>
<span data-ttu-id="94301-155">Mit JSON formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="94301-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="94301-156">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="94301-156">-SubscriptionId</span></span>
<span data-ttu-id="94301-157">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="94301-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94301-158">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="94301-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94301-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="94301-159">-Tag</span></span>
<span data-ttu-id="94301-160">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="94301-160">Resource tags.</span></span>

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

### <span data-ttu-id="94301-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="94301-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="94301-162">Gibt die Version des Skript Handlers an.</span><span class="sxs-lookup"><span data-stu-id="94301-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="94301-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94301-163">-Confirm</span></span>
<span data-ttu-id="94301-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94301-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94301-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94301-165">-WhatIf</span></span>
<span data-ttu-id="94301-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94301-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94301-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94301-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94301-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94301-168">CommonParameters</span></span>
<span data-ttu-id="94301-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94301-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94301-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94301-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94301-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94301-171">INPUTS</span></span>

### <span data-ttu-id="94301-172">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="94301-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="94301-173">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="94301-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="94301-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94301-174">OUTPUTS</span></span>

### <span data-ttu-id="94301-175">Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="94301-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="94301-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="94301-176">NOTES</span></span>

<span data-ttu-id="94301-177">Aliase</span><span class="sxs-lookup"><span data-stu-id="94301-177">ALIASES</span></span>

<span data-ttu-id="94301-178">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94301-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94301-179">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="94301-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94301-180">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="94301-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94301-181">Extensionparameter <IMachineExtension> : Beschreibt eine Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="94301-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="94301-182">`Location <String>`: Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="94301-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="94301-183">`[Tag <ITrackedResourceTags>]`: Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="94301-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="94301-184">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="94301-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="94301-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="94301-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="94301-186">Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="94301-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="94301-187">`[ForceUpdateTag <String>]`: Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="94301-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="94301-188">`[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="94301-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="94301-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="94301-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="94301-190">`[Publisher <String>]`: Der Name des Erweiterungs Handlers Publisher.</span><span class="sxs-lookup"><span data-stu-id="94301-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="94301-191">`[Setting <IMachineExtensionPropertiesSettings>]`: JSON-formatierte öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="94301-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="94301-192">`[TypeHandlerVersion <String>]`: Gibt die Version des Skript Handlers an.</span><span class="sxs-lookup"><span data-stu-id="94301-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="94301-193">Inputobject <IConnectedMachineIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="94301-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94301-194">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="94301-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="94301-195">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="94301-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94301-196">`[Name <String>]`: Der Name der hybridmaschine.</span><span class="sxs-lookup"><span data-stu-id="94301-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="94301-197">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="94301-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="94301-198">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="94301-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94301-199">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="94301-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="94301-200">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94301-200">RELATED LINKS</span></span>

