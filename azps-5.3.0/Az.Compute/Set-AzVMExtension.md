---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472945"
---
# <span data-ttu-id="1b27f-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1b27f-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="1b27f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b27f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b27f-103">Aktualisiert Erweiterungseigenschaften oder fügt einem virtuellen Computer eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1b27f-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="1b27f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b27f-104">SYNTAX</span></span>

### <span data-ttu-id="1b27f-105">Einstellungen (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b27f-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b27f-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="1b27f-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b27f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b27f-107">DESCRIPTION</span></span>
<span data-ttu-id="1b27f-108">Das **Cmdlet "Set-AzVMExtension"** aktualisiert Eigenschaften für vorhandene Virtual Machine Extensions oder fügt eine Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="1b27f-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="1b27f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b27f-109">EXAMPLES</span></span>

### <span data-ttu-id="1b27f-110">Beispiel 1: Ändern von Einstellungen mithilfe von Hashtabellen</span><span class="sxs-lookup"><span data-stu-id="1b27f-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="1b27f-111">Die ersten beiden Befehle verwenden die Windows PowerShell A0 zum Erstellen von Hashtabellen und speichern diese Hashtabellen dann in den $Settings und $ProtectedSettings Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b27f-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="1b27f-112">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help about_Hash_Tables` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="1b27f-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="1b27f-113">Der zweite Befehl enthält zwei Werte, die zuvor erstellt und in Variablen gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="1b27f-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="1b27f-114">Der letzte Befehl ändert eine Erweiterung des virtuellen Computers "VirtualMachine22" in ResourceGroup11 entsprechend den Inhalten $Settings und $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="1b27f-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="1b27f-115">Der Befehl gibt weitere erforderliche Informationen an, die den Herausgeber und den Erweiterungstyp enthalten.</span><span class="sxs-lookup"><span data-stu-id="1b27f-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="1b27f-116">Beispiel 2: Ändern von Einstellungen mithilfe von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="1b27f-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="1b27f-117">Die ersten beiden Befehle erstellen Zeichenfolgen, die Einstellungen enthalten, und speichern sie dann in den $SettingsString und $ProtectedSettingsString Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b27f-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="1b27f-118">Der letzte Befehl ändert eine Erweiterung des virtuellen Computers "VirtualMachine22" in ResourceGroup11 entsprechend den Inhalten $SettingsString und $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="1b27f-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="1b27f-119">Der Befehl gibt weitere erforderliche Informationen an, die den Herausgeber und den Erweiterungstyp enthalten.</span><span class="sxs-lookup"><span data-stu-id="1b27f-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="1b27f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b27f-120">PARAMETERS</span></span>

### <span data-ttu-id="1b27f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b27f-121">-AsJob</span></span>
<span data-ttu-id="1b27f-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1b27f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b27f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b27f-123">-DefaultProfile</span></span>
<span data-ttu-id="1b27f-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b27f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1b27f-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1b27f-126">Gibt an, dass dieses Cmdlet verhindert, dass der Azure-Gast-Agent die Erweiterungen automatisch auf eine neuere Nebenversion aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1b27f-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="1b27f-127">Standardmäßig ermöglicht dieses Cmdlet dem Gast-Agent, die Erweiterungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1b27f-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="1b27f-128">-ExtensionType</span></span>
<span data-ttu-id="1b27f-129">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-129">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1b27f-130">-ForceRerun</span></span>
<span data-ttu-id="1b27f-131">Gibt an, dass dieses Cmdlet eine Erneutes Ausführen derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne dass die Erweiterung deinstalliert und neu installiert wird.</span><span class="sxs-lookup"><span data-stu-id="1b27f-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1b27f-132">Bei dem Wert kann sich eine beliebige Zeichenfolge vom aktuellen Wert unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1b27f-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1b27f-133">Wenn "forceUpdateTag" nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="1b27f-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-134">-Location</span><span class="sxs-lookup"><span data-stu-id="1b27f-134">-Location</span></span>
<span data-ttu-id="1b27f-135">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-135">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-136">-Name</span><span class="sxs-lookup"><span data-stu-id="1b27f-136">-Name</span></span>
<span data-ttu-id="1b27f-137">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-137">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b27f-138">-NoWait</span></span>
<span data-ttu-id="1b27f-139">Startet den Vorgang und kehrt unmittelbar vor Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="1b27f-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1b27f-140">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="1b27f-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1b27f-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="1b27f-141">-ProtectedSettings</span></span>
<span data-ttu-id="1b27f-142">Gibt die private Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="1b27f-143">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b27f-143">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="1b27f-144">-ProtectedSettingString</span></span>
<span data-ttu-id="1b27f-145">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="1b27f-146">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b27f-146">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1b27f-147">-Publisher</span></span>
<span data-ttu-id="1b27f-148">Gibt den Namen des Erweiterungsherausgebers an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="1b27f-149">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="1b27f-149">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b27f-150">-ResourceGroupName</span></span>
<span data-ttu-id="1b27f-151">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-152">-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1b27f-152">-Settings</span></span>
<span data-ttu-id="1b27f-153">Gibt die öffentliche Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="1b27f-154">Mit diesem Cmdlet wird die öffentliche Konfiguration nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="1b27f-154">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-155">-SettingString</span><span class="sxs-lookup"><span data-stu-id="1b27f-155">-SettingString</span></span>
<span data-ttu-id="1b27f-156">Gibt die öffentliche Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="1b27f-157">Mit diesem Cmdlet wird die öffentliche Konfiguration nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="1b27f-157">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1b27f-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="1b27f-159">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b27f-159">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b27f-160">-VMName</span></span>
<span data-ttu-id="1b27f-161">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1b27f-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1b27f-162">Dieses Cmdlet ändert Erweiterungen für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1b27f-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b27f-163">-Confirm</span></span>
<span data-ttu-id="1b27f-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b27f-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1b27f-165">-WhatIf</span></span>
<span data-ttu-id="1b27f-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b27f-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b27f-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b27f-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b27f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b27f-168">CommonParameters</span></span>
<span data-ttu-id="1b27f-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b27f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b27f-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b27f-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b27f-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b27f-171">INPUTS</span></span>

### <span data-ttu-id="1b27f-172">System.String</span><span class="sxs-lookup"><span data-stu-id="1b27f-172">System.String</span></span>

### <span data-ttu-id="1b27f-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b27f-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1b27f-174">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b27f-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1b27f-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b27f-175">OUTPUTS</span></span>

### <span data-ttu-id="1b27f-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1b27f-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1b27f-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b27f-177">NOTES</span></span>

## <span data-ttu-id="1b27f-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b27f-178">RELATED LINKS</span></span>

[<span data-ttu-id="1b27f-179">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1b27f-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="1b27f-180">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1b27f-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


