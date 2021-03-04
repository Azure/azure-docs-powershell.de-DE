---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: b1c7a45f538c10c2ef6c2f03809a127a21237fc9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933043"
---
# <span data-ttu-id="0519a-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0519a-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="0519a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0519a-102">SYNOPSIS</span></span>
<span data-ttu-id="0519a-103">Aktualisiert Erweiterungseigenschaften oder fügt einem virtuellen Computer eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0519a-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="0519a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0519a-104">SYNTAX</span></span>

### <span data-ttu-id="0519a-105">Einstellungen (Standard)</span><span class="sxs-lookup"><span data-stu-id="0519a-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0519a-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="0519a-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0519a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0519a-107">DESCRIPTION</span></span>
<span data-ttu-id="0519a-108">Das **Cmdlet Set-AzVMExtension** aktualisiert Eigenschaften für vorhandene Erweiterungen für virtuelle Computer oder fügt einem virtuellen Computer eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0519a-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="0519a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0519a-109">EXAMPLES</span></span>

### <span data-ttu-id="0519a-110">Beispiel 1: Ändern von Einstellungen mithilfe von Hashtabellen</span><span class="sxs-lookup"><span data-stu-id="0519a-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="0519a-111">Die ersten beiden Befehle verwenden die Standardsyntax Windows PowerShell zum Erstellen von Hashtabellen und speichern diese Hashtabellen dann in den $Settings und $ProtectedSettings Variablen.</span><span class="sxs-lookup"><span data-stu-id="0519a-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="0519a-112">Weitere Informationen finden Sie unter `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="0519a-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="0519a-113">Der zweite Befehl enthält zwei Werte, die zuvor erstellt und in Variablen gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="0519a-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="0519a-114">Der letzte Befehl ändert eine Erweiterung des virtuellen Computers mit dem Namen VirtualMachine22 in ResourceGroup11 entsprechend den Inhalten der $Settings und $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="0519a-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="0519a-115">Der Befehl gibt weitere erforderliche Informationen an, die den Herausgeber und den Erweiterungstyp enthalten.</span><span class="sxs-lookup"><span data-stu-id="0519a-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="0519a-116">Beispiel 2: Ändern von Einstellungen mithilfe von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="0519a-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="0519a-117">Die ersten beiden Befehle erstellen Zeichenfolgen, die Einstellungen enthalten, und speichern sie dann in $SettingsString und $ProtectedSettingsString Variablen.</span><span class="sxs-lookup"><span data-stu-id="0519a-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="0519a-118">Der letzte Befehl ändert eine Erweiterung des virtuellen Computers mit dem Namen VirtualMachine22 in ResourceGroup11 entsprechend den Inhalten der $SettingsString und $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="0519a-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="0519a-119">Der Befehl gibt weitere erforderliche Informationen an, die den Herausgeber und den Erweiterungstyp enthalten.</span><span class="sxs-lookup"><span data-stu-id="0519a-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="0519a-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0519a-120">PARAMETERS</span></span>

### <span data-ttu-id="0519a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0519a-121">-AsJob</span></span>
<span data-ttu-id="0519a-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0519a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0519a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0519a-123">-DefaultProfile</span></span>
<span data-ttu-id="0519a-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0519a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0519a-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0519a-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0519a-126">Gibt an, dass dieses Cmdlet verhindert, dass der Azure-Gast-Agent die Erweiterungen automatisch auf eine neuere Nebenversion aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0519a-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="0519a-127">Standardmäßig ermöglicht dieses Cmdlet dem Gast-Agent das Aktualisieren der Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="0519a-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="0519a-128">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="0519a-128">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="0519a-129">Gibt an, ob die Erweiterung automatisch von der Plattform aktualisiert werden soll, wenn eine neuere Version der Erweiterung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0519a-129">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0519a-130">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="0519a-130">-ExtensionType</span></span>
<span data-ttu-id="0519a-131">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="0519a-131">Specifies the extension type.</span></span>

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

### <span data-ttu-id="0519a-132">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="0519a-132">-ForceRerun</span></span>
<span data-ttu-id="0519a-133">Gibt an, dass dieses Cmdlet eine Erneutes Ausführen derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="0519a-133">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="0519a-134">Der Wert kann eine beliebige Zeichenfolge sein, die sich vom aktuellen Wert ab unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="0519a-134">The value can be any string different from the current value.</span></span>
<span data-ttu-id="0519a-135">Wenn forceUpdateTag nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="0519a-135">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="0519a-136">-Location</span><span class="sxs-lookup"><span data-stu-id="0519a-136">-Location</span></span>
<span data-ttu-id="0519a-137">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="0519a-137">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="0519a-138">-Name</span><span class="sxs-lookup"><span data-stu-id="0519a-138">-Name</span></span>
<span data-ttu-id="0519a-139">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="0519a-139">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="0519a-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0519a-140">-NoWait</span></span>
<span data-ttu-id="0519a-141">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0519a-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0519a-142">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0519a-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0519a-143">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="0519a-143">-ProtectedSettings</span></span>
<span data-ttu-id="0519a-144">Gibt die private Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="0519a-144">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="0519a-145">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0519a-145">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="0519a-146">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="0519a-146">-ProtectedSettingString</span></span>
<span data-ttu-id="0519a-147">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="0519a-147">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="0519a-148">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0519a-148">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="0519a-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0519a-149">-Publisher</span></span>
<span data-ttu-id="0519a-150">Gibt den Namen des Erweiterungsherausgebers an.</span><span class="sxs-lookup"><span data-stu-id="0519a-150">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="0519a-151">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="0519a-151">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="0519a-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0519a-152">-ResourceGroupName</span></span>
<span data-ttu-id="0519a-153">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="0519a-153">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0519a-154">-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0519a-154">-Settings</span></span>
<span data-ttu-id="0519a-155">Gibt die öffentliche Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="0519a-155">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="0519a-156">Dieses Cmdlet verschlüsselt die öffentliche Konfiguration nicht.</span><span class="sxs-lookup"><span data-stu-id="0519a-156">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="0519a-157">-SettingString</span><span class="sxs-lookup"><span data-stu-id="0519a-157">-SettingString</span></span>
<span data-ttu-id="0519a-158">Gibt die öffentliche Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="0519a-158">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="0519a-159">Dieses Cmdlet verschlüsselt die öffentliche Konfiguration nicht.</span><span class="sxs-lookup"><span data-stu-id="0519a-159">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="0519a-160">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0519a-160">-TypeHandlerVersion</span></span>
<span data-ttu-id="0519a-161">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0519a-161">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="0519a-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="0519a-162">-VMName</span></span>
<span data-ttu-id="0519a-163">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="0519a-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0519a-164">Dieses Cmdlet ändert Erweiterungen für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0519a-164">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0519a-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0519a-165">-Confirm</span></span>
<span data-ttu-id="0519a-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0519a-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0519a-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0519a-167">-WhatIf</span></span>
<span data-ttu-id="0519a-168">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0519a-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0519a-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0519a-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0519a-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0519a-170">CommonParameters</span></span>
<span data-ttu-id="0519a-171">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0519a-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0519a-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0519a-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0519a-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0519a-173">INPUTS</span></span>

### <span data-ttu-id="0519a-174">System.String</span><span class="sxs-lookup"><span data-stu-id="0519a-174">System.String</span></span>

### <span data-ttu-id="0519a-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0519a-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0519a-176">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0519a-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0519a-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0519a-177">OUTPUTS</span></span>

### <span data-ttu-id="0519a-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0519a-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0519a-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0519a-179">NOTES</span></span>

## <span data-ttu-id="0519a-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0519a-180">RELATED LINKS</span></span>

[<span data-ttu-id="0519a-181">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0519a-181">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="0519a-182">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0519a-182">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


