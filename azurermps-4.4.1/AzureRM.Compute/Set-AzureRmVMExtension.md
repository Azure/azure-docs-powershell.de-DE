---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497110"
---
# <span data-ttu-id="43369-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="43369-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="43369-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43369-102">SYNOPSIS</span></span>
<span data-ttu-id="43369-103">Aktualisiert Erweiterungseigenschaften oder fügt eine Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="43369-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43369-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43369-104">SYNTAX</span></span>

### <span data-ttu-id="43369-105">Einstellungen (Standard)</span><span class="sxs-lookup"><span data-stu-id="43369-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43369-106">Setfunktion</span><span class="sxs-lookup"><span data-stu-id="43369-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43369-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43369-107">DESCRIPTION</span></span>
<span data-ttu-id="43369-108">Das Cmdlet " **Satz-AzureRmVMExtension** " aktualisiert Eigenschaften für vorhandene Virtual Machine-Erweiterungen oder fügt eine Erweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="43369-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="43369-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43369-109">EXAMPLES</span></span>

### <span data-ttu-id="43369-110">Beispiel 1: Ändern von Einstellungen mithilfe von Hashtabellen</span><span class="sxs-lookup"><span data-stu-id="43369-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="43369-111">Die ersten beiden Befehle verwenden die Windows PowerShell-Standardsyntax zum Erstellen von Hashtabellen und speichern dann die Hashtabellen in den $Settings-und $ProtectedSettings Variablen.</span><span class="sxs-lookup"><span data-stu-id="43369-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="43369-112">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="43369-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="43369-113">Der zweite Befehl enthält zwei zuvor erstellte und in Variablen gespeicherte Werte.</span><span class="sxs-lookup"><span data-stu-id="43369-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="43369-114">Der endgültige Befehl ändert eine Erweiterung des virtuellen Computers mit dem Namen VirtualMachine22 in ResourceGroup11 entsprechend dem Inhalt $Settings und $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="43369-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="43369-115">Der Befehl gibt weitere erforderliche Informationen an, einschließlich des Herausgebers und des Erweiterungstyps.</span><span class="sxs-lookup"><span data-stu-id="43369-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="43369-116">Beispiel 2: Ändern von Einstellungen mithilfe von Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="43369-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="43369-117">Die ersten beiden Befehle erstellen Zeichenfolgen, die Einstellungen enthalten, und speichern Sie dann in den Variablen $SettingsString und $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="43369-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="43369-118">Der endgültige Befehl ändert eine Erweiterung des virtuellen Computers mit dem Namen VirtualMachine22 in ResourceGroup11 entsprechend dem Inhalt $SettingsString und $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="43369-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="43369-119">Der Befehl gibt weitere erforderliche Informationen an, einschließlich des Herausgebers und des Erweiterungstyps.</span><span class="sxs-lookup"><span data-stu-id="43369-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="43369-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="43369-120">PARAMETERS</span></span>

### <span data-ttu-id="43369-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43369-121">-DefaultProfile</span></span>
<span data-ttu-id="43369-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43369-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43369-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="43369-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="43369-124">Gibt an, dass dieses Cmdlet verhindert, dass der Azure Guest-Agent die Erweiterungen automatisch auf eine neuere Nebenversion aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="43369-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="43369-125">Standardmäßig ermöglicht dieses Cmdlet dem Gast-Agent, die Erweiterungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="43369-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="43369-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="43369-126">-ExtensionType</span></span>
<span data-ttu-id="43369-127">Gibt den Erweiterungstyp an.</span><span class="sxs-lookup"><span data-stu-id="43369-127">Specifies the extension type.</span></span>

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

### <span data-ttu-id="43369-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="43369-128">-ForceRerun</span></span>
<span data-ttu-id="43369-129">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="43369-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="43369-130">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="43369-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="43369-131">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="43369-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="43369-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="43369-132">-Location</span></span>
<span data-ttu-id="43369-133">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="43369-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="43369-134">-Name</span><span class="sxs-lookup"><span data-stu-id="43369-134">-Name</span></span>
<span data-ttu-id="43369-135">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="43369-135">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="43369-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="43369-136">-ProtectedSettings</span></span>
<span data-ttu-id="43369-137">Gibt die private Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="43369-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="43369-138">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="43369-138">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="43369-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="43369-139">-ProtectedSettingString</span></span>
<span data-ttu-id="43369-140">Gibt die private Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="43369-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="43369-141">Dieses Cmdlet verschlüsselt die private Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="43369-141">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="43369-142">-Publisher</span><span class="sxs-lookup"><span data-stu-id="43369-142">-Publisher</span></span>
<span data-ttu-id="43369-143">Gibt den Namen des Erweiterungs Herausgebers an.</span><span class="sxs-lookup"><span data-stu-id="43369-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="43369-144">Der Herausgeber gibt einen Namen an, wenn der Herausgeber eine Erweiterung registriert.</span><span class="sxs-lookup"><span data-stu-id="43369-144">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="43369-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43369-145">-ResourceGroupName</span></span>
<span data-ttu-id="43369-146">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="43369-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="43369-147">-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="43369-147">-Settings</span></span>
<span data-ttu-id="43369-148">Gibt die öffentliche Konfiguration für die Erweiterung als Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="43369-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="43369-149">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="43369-149">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="43369-150">-Setfunktion</span><span class="sxs-lookup"><span data-stu-id="43369-150">-SettingString</span></span>
<span data-ttu-id="43369-151">Gibt die öffentliche Konfiguration für die Erweiterung als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="43369-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="43369-152">Dieses Cmdlet verschlüsselt keine öffentliche Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="43369-152">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="43369-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="43369-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="43369-154">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43369-154">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="43369-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="43369-155">-VMName</span></span>
<span data-ttu-id="43369-156">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="43369-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="43369-157">Dieses Cmdlet ändert die Erweiterungen für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="43369-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="43369-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43369-158">-Confirm</span></span>
<span data-ttu-id="43369-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43369-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43369-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43369-160">-WhatIf</span></span>
<span data-ttu-id="43369-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43369-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="43369-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43369-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43369-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43369-163">CommonParameters</span></span>
<span data-ttu-id="43369-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43369-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43369-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43369-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43369-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43369-166">INPUTS</span></span>

## <span data-ttu-id="43369-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43369-167">OUTPUTS</span></span>

## <span data-ttu-id="43369-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="43369-168">NOTES</span></span>

## <span data-ttu-id="43369-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43369-169">RELATED LINKS</span></span>

[<span data-ttu-id="43369-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="43369-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="43369-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="43369-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


