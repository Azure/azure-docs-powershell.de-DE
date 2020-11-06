---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: a9d03bd7f506c7210eeee90c379f90dd0833818e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477229"
---
# <span data-ttu-id="46e3f-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="46e3f-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="46e3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="46e3f-103">Fügt eine benutzerdefinierte Skripterweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="46e3f-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e3f-104">SYNTAX</span></span>

### <span data-ttu-id="46e3f-105">SetCustomScriptExtensionByContainerAndFileNames (Standard)</span><span class="sxs-lookup"><span data-stu-id="46e3f-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e3f-106">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="46e3f-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e3f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46e3f-107">DESCRIPTION</span></span>
<span data-ttu-id="46e3f-108">Das Cmdlet " **Satz-AzureRmVMCustomScriptExtension** " fügt eine benutzerdefinierte Skripterweiterung für virtuelle Computer zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="46e3f-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="46e3f-109">Mit dieser Erweiterung können Sie eigene Skripts auf dem virtuellen Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="46e3f-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="46e3f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46e3f-110">EXAMPLES</span></span>

### <span data-ttu-id="46e3f-111">Beispiel 1: Hinzufügen eines benutzerdefinierten Skripts</span><span class="sxs-lookup"><span data-stu-id="46e3f-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="46e3f-112">Mit diesem Befehl wird dem virtuellen Computer mit dem Namen VirtualMachine07 ein benutzerdefiniertes Skript hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="46e3f-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="46e3f-113">Die Skriptdatei ist contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="46e3f-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="46e3f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e3f-114">PARAMETERS</span></span>

### <span data-ttu-id="46e3f-115">-Argument</span><span class="sxs-lookup"><span data-stu-id="46e3f-115">-Argument</span></span>
<span data-ttu-id="46e3f-116">Gibt Argumente an, die die Skripterweiterung an das Skript übergibt.</span><span class="sxs-lookup"><span data-stu-id="46e3f-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="46e3f-117">-Containername</span><span class="sxs-lookup"><span data-stu-id="46e3f-117">-ContainerName</span></span>
<span data-ttu-id="46e3f-118">Gibt den Namen des Azure-Speichercontainers an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="46e3f-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e3f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e3f-119">-DefaultProfile</span></span>
<span data-ttu-id="46e3f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46e3f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e3f-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="46e3f-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="46e3f-122">-FileName</span><span class="sxs-lookup"><span data-stu-id="46e3f-122">-FileName</span></span>
<span data-ttu-id="46e3f-123">Gibt den Namen der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-123">Specifies the name of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e3f-124">-FileUri</span><span class="sxs-lookup"><span data-stu-id="46e3f-124">-FileUri</span></span>
<span data-ttu-id="46e3f-125">Gibt den URI der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-125">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e3f-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="46e3f-126">-ForceRerun</span></span>
<span data-ttu-id="46e3f-127">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="46e3f-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="46e3f-128">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="46e3f-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="46e3f-129">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="46e3f-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="46e3f-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="46e3f-130">-Location</span></span>
<span data-ttu-id="46e3f-131">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="46e3f-132">-Name</span><span class="sxs-lookup"><span data-stu-id="46e3f-132">-Name</span></span>
<span data-ttu-id="46e3f-133">Gibt den Namen der benutzerdefinierten Skripterweiterung an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-133">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="46e3f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e3f-134">-ResourceGroupName</span></span>
<span data-ttu-id="46e3f-135">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="46e3f-136">-Run</span><span class="sxs-lookup"><span data-stu-id="46e3f-136">-Run</span></span>
<span data-ttu-id="46e3f-137">Gibt den Befehl an, mit dem das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46e3f-137">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e3f-138">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="46e3f-138">-SecureExecution</span></span>
<span data-ttu-id="46e3f-139">Gibt an, dass dieses Cmdlet sicherstellt, dass der Wert des *Run* -Parameters nicht auf dem Server protokolliert oder mithilfe der Get-Erweiterungs-API an den Benutzer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="46e3f-139">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="46e3f-140">Der Wert von *Run* enthält möglicherweise Geheimnisse oder Kennwörter, die sicher an die Skriptdatei übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="46e3f-140">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="46e3f-141">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="46e3f-141">-StorageAccountKey</span></span>
<span data-ttu-id="46e3f-142">Gibt den Schlüssel für den Azure-Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-142">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e3f-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="46e3f-143">-StorageAccountName</span></span>
<span data-ttu-id="46e3f-144">Gibt den Namen des Azure Storage-Kontos an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="46e3f-144">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e3f-145">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="46e3f-145">-StorageEndpointSuffix</span></span>
<span data-ttu-id="46e3f-146">Gibt das Suffix für das Speicher Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-146">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e3f-147">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="46e3f-147">-TypeHandlerVersion</span></span>
<span data-ttu-id="46e3f-148">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="46e3f-148">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="46e3f-149">Führen Sie zum Abrufen der Version das Get-AzureRmVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und VMAccessAgent für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="46e3f-149">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="46e3f-150">-VMName</span><span class="sxs-lookup"><span data-stu-id="46e3f-150">-VMName</span></span>
<span data-ttu-id="46e3f-151">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="46e3f-151">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="46e3f-152">Mit diesem Cmdlet wird die benutzerdefinierte Skripterweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="46e3f-152">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="46e3f-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46e3f-153">-Confirm</span></span>
<span data-ttu-id="46e3f-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46e3f-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e3f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e3f-155">-WhatIf</span></span>
<span data-ttu-id="46e3f-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46e3f-156">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="46e3f-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46e3f-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e3f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e3f-158">CommonParameters</span></span>
<span data-ttu-id="46e3f-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e3f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e3f-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e3f-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e3f-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46e3f-161">INPUTS</span></span>

## <span data-ttu-id="46e3f-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46e3f-162">OUTPUTS</span></span>

## <span data-ttu-id="46e3f-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="46e3f-163">NOTES</span></span>

## <span data-ttu-id="46e3f-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46e3f-164">RELATED LINKS</span></span>

[<span data-ttu-id="46e3f-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="46e3f-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="46e3f-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="46e3f-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


