---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296505"
---
# <span data-ttu-id="288e6-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="288e6-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="288e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="288e6-102">SYNOPSIS</span></span>
<span data-ttu-id="288e6-103">Aktualisiert Erweiterungseigenschaften oder fügt eine Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="288e6-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="288e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="288e6-104">SYNTAX</span></span>

### <span data-ttu-id="288e6-105">Einstellungen (Standard)</span><span class="sxs-lookup"><span data-stu-id="288e6-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="288e6-106">Setfunktion</span><span class="sxs-lookup"><span data-stu-id="288e6-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288e6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="288e6-107">DESCRIPTION</span></span>
<span data-ttu-id="288e6-108">Das Cmdlet " **Satz-AzVMExtension** " aktualisiert Eigenschaften für vorhandene Virtual Machine-Erweiterungen oder fügt eine Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="288e6-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="288e6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="288e6-109">EXAMPLES</span></span>

### <span data-ttu-id="288e6-110">Beispiel 1: Ändern von Einstellungen mithilfe von Hashtabellen</span><span class="sxs-lookup"><span data-stu-id="288e6-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="288e6-111">Die ersten beiden Befehle verwenden die Windows PowerShell-Standardsyntax zum Erstellen von Hashtabellen und speichern dann die Hashtabellen in den $Settings-und $ProtectedSettings Variablen.</span><span class="sxs-lookup"><span data-stu-id="288e6-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="288e6-112">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="288e6-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="288e6-113">Der zweite Befehl enthält zwei zuvor erstellte und in Variablen gespeicherte Werte.</span><span class="sxs-lookup"><span data-stu-id="288e6-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="288e6-114">Der endgültige Befehl ändert eine Erweiterung des virtuellen Computers mit dem Namen VirtualMachine22 in ResourceGroup11 entsprechend dem Inhalt $Settings und $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="288e6-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="288e6-115">Der Befehl gibt weitere erforderliche Informationen an, einschließlich des Herausgebers und des Erweiterungstyps.</span><span class="sxs-lookup"><span data-stu-id="288e6-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="288e6-116">Beispiel 2: Ändern von Einstellungen mithilfe von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="288e6-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="288e6-117">Die ersten beiden Befehle erstellen Zeichenfolgen, die Einstellungen enthalten, und speichern Sie dann in den Variablen $SettingsString und $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="288e6-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="288e6-118">Der endgültige Befehl ändert eine Erweiterung des virtuellen Computers mit dem Namen VirtualMachine22 in ResourceGroup11 entsprechend dem Inhalt $SettingsString und $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="288e6-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="288e6-119">Der Befehl gibt weitere erforderliche Informationen an, einschließlich des Herausgebers und des Erweiterungstyps.</span><span class="sxs-lookup"><span data-stu-id="288e6-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="288e6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="288e6-120">PARAMETERS</span></span>

### <span data-ttu-id="288e6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="288e6-121">-AsJob</span></span>
<span data-ttu-id="288e6-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="288e6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="288e6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288e6-123">-DefaultProfile</span></span>
<span data-ttu-id="288e6-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="288e6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="288e6-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="288e6-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="288e6-126">Gibt an, dass dieses Cmdlet verhindert, dass der Azure Guest-Agent die Erweiterungen automatisch auf eine neuere Nebenversion aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="288e6-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="288e6-127">Standardmäßig ermöglicht dieses Cmdlet dem Gast-Agent, die Erweiterungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="288e6-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="288e6-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="288e6-128">-ExtensionType</span></span>
<span data-ttu-id="288e6-129">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="288e6-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="288e6-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="288e6-130">-ForceRerun</span></span>
<span data-ttu-id="288e6-131">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="288e6-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="288e6-132">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="288e6-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="288e6-133">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="288e6-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="288e6-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="288e6-134">-Location</span></span>
<span data-ttu-id="288e6-135">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="288e6-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="288e6-136">-Name</span><span class="sxs-lookup"><span data-stu-id="288e6-136">-Name</span></span>
<span data-ttu-id="288e6-137">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="288e6-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="288e6-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="288e6-138">-NoWait</span></span>
<span data-ttu-id="288e6-139">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="288e6-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="288e6-140">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="288e6-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="288e6-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="288e6-141">-ProtectedSettings</span></span>
<span data-ttu-id="288e6-142">Gibt die private Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="288e6-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="288e6-143">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="288e6-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="288e6-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="288e6-144">-ProtectedSettingString</span></span>
<span data-ttu-id="288e6-145">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="288e6-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="288e6-146">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="288e6-146">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="288e6-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="288e6-147">-Publisher</span></span>
<span data-ttu-id="288e6-148">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="288e6-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="288e6-149">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="288e6-149">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="288e6-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288e6-150">-ResourceGroupName</span></span>
<span data-ttu-id="288e6-151">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="288e6-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="288e6-152">-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="288e6-152">-Settings</span></span>
<span data-ttu-id="288e6-153">Gibt die öffentliche Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="288e6-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="288e6-154">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="288e6-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="288e6-155">-Setfunktion</span><span class="sxs-lookup"><span data-stu-id="288e6-155">-SettingString</span></span>
<span data-ttu-id="288e6-156">Gibt die öffentliche Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="288e6-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="288e6-157">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="288e6-157">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="288e6-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="288e6-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="288e6-159">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="288e6-159">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="288e6-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="288e6-160">-VMName</span></span>
<span data-ttu-id="288e6-161">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="288e6-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="288e6-162">Dieses Cmdlet ändert die Erweiterungen für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="288e6-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="288e6-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="288e6-163">-Confirm</span></span>
<span data-ttu-id="288e6-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="288e6-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288e6-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288e6-165">-WhatIf</span></span>
<span data-ttu-id="288e6-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="288e6-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288e6-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="288e6-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288e6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288e6-168">CommonParameters</span></span>
<span data-ttu-id="288e6-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288e6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288e6-170">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="288e6-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288e6-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="288e6-171">INPUTS</span></span>

### <span data-ttu-id="288e6-172">System. String</span><span class="sxs-lookup"><span data-stu-id="288e6-172">System.String</span></span>

### <span data-ttu-id="288e6-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="288e6-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="288e6-174">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="288e6-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="288e6-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="288e6-175">OUTPUTS</span></span>

### <span data-ttu-id="288e6-176">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="288e6-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="288e6-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="288e6-177">NOTES</span></span>

## <span data-ttu-id="288e6-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="288e6-178">RELATED LINKS</span></span>

[<span data-ttu-id="288e6-179">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="288e6-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="288e6-180">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="288e6-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


