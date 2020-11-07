---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: f858ee5992c633674e52118a7d92554190107f75
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651918"
---
# <span data-ttu-id="ead4e-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ead4e-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="ead4e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ead4e-102">SYNOPSIS</span></span>
<span data-ttu-id="ead4e-103">Fügt eine benutzerdefinierte Skripterweiterung zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="ead4e-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="ead4e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ead4e-104">SYNTAX</span></span>

### <span data-ttu-id="ead4e-105">ByNameWithContainerAndFileNamesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ead4e-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead4e-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead4e-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead4e-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead4e-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead4e-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead4e-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead4e-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead4e-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead4e-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead4e-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ead4e-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead4e-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ead4e-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ead4e-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ead4e-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ead4e-113">DESCRIPTION</span></span>
<span data-ttu-id="ead4e-114">Das Cmdlet " **Satz-AzVMCustomScriptExtension** " fügt eine benutzerdefinierte Skripterweiterung für virtuelle Computer zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="ead4e-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="ead4e-115">Mit dieser Erweiterung können Sie eigene Skripts auf dem virtuellen Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="ead4e-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="ead4e-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ead4e-116">EXAMPLES</span></span>

### <span data-ttu-id="ead4e-117">Beispiel 1: Hinzufügen eines benutzerdefinierten Skripts</span><span class="sxs-lookup"><span data-stu-id="ead4e-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="ead4e-118">Mit diesem Befehl wird dem virtuellen Computer mit dem Namen VirtualMachine07 ein benutzerdefiniertes Skript hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ead4e-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ead4e-119">Die Skriptdatei ist contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="ead4e-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="ead4e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ead4e-120">PARAMETERS</span></span>

### <span data-ttu-id="ead4e-121">-Argument</span><span class="sxs-lookup"><span data-stu-id="ead4e-121">-Argument</span></span>
<span data-ttu-id="ead4e-122">Gibt Argumente an, die die Skripterweiterung an das Skript übergibt.</span><span class="sxs-lookup"><span data-stu-id="ead4e-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="ead4e-123">-Containername</span><span class="sxs-lookup"><span data-stu-id="ead4e-123">-ContainerName</span></span>
<span data-ttu-id="ead4e-124">Gibt den Namen des Azure-Speichercontainers an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="ead4e-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ead4e-125">-DefaultProfile</span></span>
<span data-ttu-id="ead4e-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ead4e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ead4e-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ead4e-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="ead4e-128">-FileName</span><span class="sxs-lookup"><span data-stu-id="ead4e-128">-FileName</span></span>
<span data-ttu-id="ead4e-129">Gibt den Namen der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-129">Specifies the name of the script file.</span></span> <span data-ttu-id="ead4e-130">Wenn die Datei im Azure BLOB-Speicher gespeichert ist, wird bei dem Dateinamen Wert die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="ead4e-130">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="ead4e-131">Bei Dateinamen von Dateien, die im Azure-Dateispeicher gespeichert sind, wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ead4e-131">File names of files stored in Azure File storage are not case-sensitive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="ead4e-132">-FileUri</span></span>
<span data-ttu-id="ead4e-133">Gibt den URI der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-133">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="ead4e-134">-ForceRerun</span></span>
<span data-ttu-id="ead4e-135">Gibt an, dass dieses Cmdlet eine erneute Ausführung derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne die Erweiterung zu deinstallieren und erneut zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ead4e-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="ead4e-136">Der Wert kann eine beliebige Zeichenfolge sein, die vom aktuellen Wert abweicht.</span><span class="sxs-lookup"><span data-stu-id="ead4e-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="ead4e-137">Wenn forceUpdateTag nicht geändert wird, werden Updates für öffentliche oder geschützte Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="ead4e-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="ead4e-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ead4e-138">-InputObject</span></span>
<span data-ttu-id="ead4e-139">VM-Erweiterungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ead4e-139">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-140">-Standort</span><span class="sxs-lookup"><span data-stu-id="ead4e-140">-Location</span></span>
<span data-ttu-id="ead4e-141">Gibt den Speicherort der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ead4e-142">-Name</span><span class="sxs-lookup"><span data-stu-id="ead4e-142">-Name</span></span>
<span data-ttu-id="ead4e-143">Gibt den Namen der benutzerdefinierten Skripterweiterung an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-143">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-144">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ead4e-144">-NoWait</span></span>
<span data-ttu-id="ead4e-145">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ead4e-145">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ead4e-146">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ead4e-146">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ead4e-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ead4e-147">-ResourceGroupName</span></span>
<span data-ttu-id="ead4e-148">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-149">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ead4e-149">-ResourceId</span></span>
<span data-ttu-id="ead4e-150">VM-Erweiterung-Quell-Nr.</span><span class="sxs-lookup"><span data-stu-id="ead4e-150">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-151">-Run</span><span class="sxs-lookup"><span data-stu-id="ead4e-151">-Run</span></span>
<span data-ttu-id="ead4e-152">Gibt den Befehl an, mit dem das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ead4e-152">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="ead4e-153">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="ead4e-153">-SecureExecution</span></span>
<span data-ttu-id="ead4e-154">Gibt an, dass dieses Cmdlet sicherstellt, dass der Wert des *Run* -Parameters nicht auf dem Server protokolliert oder mithilfe der Get-Erweiterungs-API an den Benutzer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ead4e-154">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="ead4e-155">Der Wert von *Run* enthält möglicherweise Geheimnisse oder Kennwörter, die sicher an die Skriptdatei übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ead4e-155">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="ead4e-156">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ead4e-156">-StorageAccountKey</span></span>
<span data-ttu-id="ead4e-157">Gibt den Schlüssel für den Azure-Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-157">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-158">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ead4e-158">-StorageAccountName</span></span>
<span data-ttu-id="ead4e-159">Gibt den Namen des Azure Storage-Kontos an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="ead4e-159">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-160">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ead4e-160">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ead4e-161">Gibt das Suffix für das Speicher Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-161">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-162">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ead4e-162">-TypeHandlerVersion</span></span>
<span data-ttu-id="ead4e-163">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ead4e-163">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ead4e-164">Führen Sie zum Abrufen der Version das Get-AzVMExtensionImage-Cmdlet mit dem Wert Microsoft. Compute für den *PublisherName* -Parameter und CustomScriptExtension für den *Type* -Parameter aus.</span><span class="sxs-lookup"><span data-stu-id="ead4e-164">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="ead4e-165">-VMName</span><span class="sxs-lookup"><span data-stu-id="ead4e-165">-VMName</span></span>
<span data-ttu-id="ead4e-166">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="ead4e-166">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ead4e-167">Mit diesem Cmdlet wird die benutzerdefinierte Skripterweiterung für den virtuellen Computer, den dieser Parameter angibt, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ead4e-167">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-168">-VMObject</span><span class="sxs-lookup"><span data-stu-id="ead4e-168">-VMObject</span></span>
<span data-ttu-id="ead4e-169">VM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ead4e-169">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ead4e-170">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ead4e-170">-Confirm</span></span>
<span data-ttu-id="ead4e-171">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ead4e-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ead4e-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ead4e-172">-WhatIf</span></span>
<span data-ttu-id="ead4e-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ead4e-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ead4e-174">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ead4e-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ead4e-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ead4e-175">CommonParameters</span></span>
<span data-ttu-id="ead4e-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ead4e-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ead4e-177">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ead4e-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ead4e-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ead4e-178">INPUTS</span></span>

### <span data-ttu-id="ead4e-179">System. String</span><span class="sxs-lookup"><span data-stu-id="ead4e-179">System.String</span></span>

### <span data-ttu-id="ead4e-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="ead4e-180">System.String[]</span></span>

### <span data-ttu-id="ead4e-181">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ead4e-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ead4e-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ead4e-182">OUTPUTS</span></span>

### <span data-ttu-id="ead4e-183">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ead4e-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ead4e-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="ead4e-184">NOTES</span></span>

## <span data-ttu-id="ead4e-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ead4e-185">RELATED LINKS</span></span>

[<span data-ttu-id="ead4e-186">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ead4e-186">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="ead4e-187">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ead4e-187">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


