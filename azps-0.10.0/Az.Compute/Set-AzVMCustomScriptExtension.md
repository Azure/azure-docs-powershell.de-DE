---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 6fe34ae33ed70cebe4c8f76beb235e6fa7445fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844235"
---
# <span data-ttu-id="d7485-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d7485-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="d7485-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7485-102">SYNOPSIS</span></span>
<span data-ttu-id="d7485-103">Fügt eine benutzerdefinierte Skripterweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7485-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="d7485-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7485-104">SYNTAX</span></span>

### <span data-ttu-id="d7485-105">SetCustomScriptExtensionByContainerAndFileNames (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7485-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7485-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="d7485-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7485-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7485-107">DESCRIPTION</span></span>
<span data-ttu-id="d7485-108">Das Cmdlet " **Satz-AzVMCustomScriptExtension** " fügt eine benutzerdefinierte Skripterweiterung für virtuelle Computer zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7485-108">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="d7485-109">Mit dieser Erweiterung können Sie eigene Skripts auf dem virtuellen Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7485-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="d7485-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7485-110">EXAMPLES</span></span>

### <span data-ttu-id="d7485-111">Beispiel 1: Hinzufügen eines benutzerdefinierten Skripts</span><span class="sxs-lookup"><span data-stu-id="d7485-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="d7485-112">Mit diesem Befehl wird dem virtuellen Computer mit dem Namen VirtualMachine07 ein benutzerdefiniertes Skript hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d7485-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="d7485-113">Die Skriptdatei ist contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="d7485-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="d7485-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7485-114">PARAMETERS</span></span>

### <span data-ttu-id="d7485-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="d7485-115">-Argument</span></span>
<span data-ttu-id="d7485-116">Gibt Argumente an, die die Skripterweiterung an das Skript übergibt.</span><span class="sxs-lookup"><span data-stu-id="d7485-116">Specifies arguments that the script extension passes to the script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-117">-Containername</span><span class="sxs-lookup"><span data-stu-id="d7485-117">-ContainerName</span></span>
<span data-ttu-id="d7485-118">Gibt den Namen des Azure-Speichercontainers an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="d7485-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7485-119">-DefaultProfile</span></span>
<span data-ttu-id="d7485-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7485-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d7485-121">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="d7485-122">-FileName</span></span>
<span data-ttu-id="d7485-123">Gibt den Namen der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="d7485-123">Specifies the name of the script file.</span></span> <span data-ttu-id="d7485-124">Wenn die Datei im Azure BLOB-Speicher gespeichert ist, lautet der Dateiname Wert Case-senstive.</span><span class="sxs-lookup"><span data-stu-id="d7485-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="d7485-125">Bei Dateinamen von Dateien, die im Azure-Dateispeicher gespeichert sind, handelt es sich nicht um senstive.</span><span class="sxs-lookup"><span data-stu-id="d7485-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="d7485-126">-FileUri</span></span>
<span data-ttu-id="d7485-127">Gibt den URI der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="d7485-127">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d7485-128">-ForceRerun</span></span>
<span data-ttu-id="d7485-129">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d7485-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="d7485-130">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="d7485-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="d7485-131">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="d7485-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="d7485-132">-Location</span></span>
<span data-ttu-id="d7485-133">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="d7485-133">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d7485-134">-Name</span></span>
<span data-ttu-id="d7485-135">Gibt den Namen der benutzerdefinierten Skripterweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d7485-135">Specifies the name of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7485-136">-ResourceGroupName</span></span>
<span data-ttu-id="d7485-137">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d7485-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-138">-Run</span><span class="sxs-lookup"><span data-stu-id="d7485-138">-Run</span></span>
<span data-ttu-id="d7485-139">Gibt den Befehl an, mit dem das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7485-139">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="d7485-140">-SecureExecution</span></span>
<span data-ttu-id="d7485-141">Gibt an, dass dieses Cmdlet sicherstellt, dass der Wert des *Run* -Parameters nicht auf dem Server protokolliert oder mithilfe der Get-Erweiterungs-API an den Benutzer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7485-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="d7485-142">Der Wert von *Run* enthält möglicherweise Geheimnisse oder Kennwörter, die sicher an die Skriptdatei übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7485-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d7485-143">-StorageAccountKey</span></span>
<span data-ttu-id="d7485-144">Gibt den Schlüssel für den Azure-Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="d7485-144">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d7485-145">-StorageAccountName</span></span>
<span data-ttu-id="d7485-146">Gibt den Namen des Azure Storage-Kontos an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="d7485-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d7485-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="d7485-148">Gibt das Suffix für das Speicher Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="d7485-148">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d7485-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="d7485-150">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7485-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d7485-151">Führen Sie zum Abrufen der Version das Get-AzVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und VMAccessAgent für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="d7485-151">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="d7485-152">-VMName</span></span>
<span data-ttu-id="d7485-153">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="d7485-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d7485-154">Mit diesem Cmdlet wird die benutzerdefinierte Skripterweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d7485-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7485-155">-Confirm</span></span>
<span data-ttu-id="d7485-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7485-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7485-157">-WhatIf</span></span>
<span data-ttu-id="d7485-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7485-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d7485-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7485-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7485-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7485-160">CommonParameters</span></span>
<span data-ttu-id="d7485-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7485-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7485-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7485-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7485-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7485-163">INPUTS</span></span>

### <span data-ttu-id="d7485-164">Keine</span><span class="sxs-lookup"><span data-stu-id="d7485-164">None</span></span>
<span data-ttu-id="d7485-165">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d7485-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7485-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7485-166">OUTPUTS</span></span>

### <span data-ttu-id="d7485-167">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d7485-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d7485-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7485-168">NOTES</span></span>

## <span data-ttu-id="d7485-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7485-169">RELATED LINKS</span></span>

[<span data-ttu-id="d7485-170">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d7485-170">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="d7485-171">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d7485-171">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


