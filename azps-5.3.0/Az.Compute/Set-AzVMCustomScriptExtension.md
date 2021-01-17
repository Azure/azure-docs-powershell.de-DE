---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472952"
---
# <span data-ttu-id="7c21f-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7c21f-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="7c21f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c21f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c21f-103">Fügt einem virtuellen Computer eine benutzerdefinierte Skripterweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="7c21f-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="7c21f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c21f-104">SYNTAX</span></span>

### <span data-ttu-id="7c21f-105">ByNameWithContainerAndFileNamesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c21f-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c21f-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c21f-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c21f-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c21f-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c21f-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c21f-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c21f-109">ByResourceIdWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c21f-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c21f-110">ByResourceIdWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c21f-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c21f-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c21f-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c21f-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c21f-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c21f-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c21f-113">DESCRIPTION</span></span>
<span data-ttu-id="7c21f-114">Das **Cmdlet "Set-AzVMCustomScriptExtension"** fügt einem virtuellen Computer ein benutzerdefiniertes Skript "Virtual Machine Extension" hinzu.</span><span class="sxs-lookup"><span data-stu-id="7c21f-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="7c21f-115">Mit dieser Erweiterung können Sie eigene Skripts auf dem virtuellen Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c21f-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="7c21f-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c21f-116">EXAMPLES</span></span>

### <span data-ttu-id="7c21f-117">Beispiel 1: Hinzufügen eines benutzerdefinierten Skripts</span><span class="sxs-lookup"><span data-stu-id="7c21f-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="7c21f-118">Dieser Befehl fügt dem virtuellen Computer "VirtualMachine07" ein benutzerdefiniertes Skript hinzu.</span><span class="sxs-lookup"><span data-stu-id="7c21f-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="7c21f-119">Die Skriptdatei wird contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="7c21f-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="7c21f-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7c21f-120">Example 2</span></span>

<span data-ttu-id="7c21f-121">Fügt einem virtuellen Computer eine benutzerdefinierte Skripterweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="7c21f-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="7c21f-122">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="7c21f-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="7c21f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c21f-123">PARAMETERS</span></span>

### <span data-ttu-id="7c21f-124">-Argument</span><span class="sxs-lookup"><span data-stu-id="7c21f-124">-Argument</span></span>
<span data-ttu-id="7c21f-125">Gibt die Argumente an, die von der Skripterweiterung an das Skript übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7c21f-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="7c21f-126">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7c21f-126">-ContainerName</span></span>
<span data-ttu-id="7c21f-127">Gibt den Namen des Azure-Speichercontainers an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="7c21f-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="7c21f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c21f-128">-DefaultProfile</span></span>
<span data-ttu-id="7c21f-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c21f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c21f-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7c21f-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="7c21f-131">-FileName</span><span class="sxs-lookup"><span data-stu-id="7c21f-131">-FileName</span></span>
<span data-ttu-id="7c21f-132">Gibt den Namen der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-132">Specifies the name of the script file.</span></span> <span data-ttu-id="7c21f-133">Wenn die Datei im Azure-BLOB-Speicher gespeichert ist, wird beim Dateinamenwert die Zwischenschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="7c21f-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="7c21f-134">Bei Den Dateinamen von Dateien, die im Azure File Storage gespeichert sind, wird die Zwischen- und Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7c21f-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="7c21f-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="7c21f-135">-FileUri</span></span>
<span data-ttu-id="7c21f-136">Gibt den URI der Skriptdatei an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="7c21f-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="7c21f-137">-ForceRerun</span></span>
<span data-ttu-id="7c21f-138">Gibt an, dass dieses Cmdlet eine Erneutes Ausführen derselben Erweiterungskonfiguration auf dem virtuellen Computer erzwingt, ohne dass die Erweiterung deinstalliert und neu installiert wird.</span><span class="sxs-lookup"><span data-stu-id="7c21f-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="7c21f-139">Bei dem Wert kann sich eine beliebige Zeichenfolge vom aktuellen Wert unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7c21f-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="7c21f-140">Wenn "forceUpdateTag" nicht geändert wird, werden Updates an öffentlichen oder geschützten Einstellungen weiterhin vom Handler angewendet.</span><span class="sxs-lookup"><span data-stu-id="7c21f-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="7c21f-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c21f-141">-InputObject</span></span>
<span data-ttu-id="7c21f-142">VM-Erweiterungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7c21f-142">VM extension object.</span></span>

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

### <span data-ttu-id="7c21f-143">-Location</span><span class="sxs-lookup"><span data-stu-id="7c21f-143">-Location</span></span>
<span data-ttu-id="7c21f-144">Gibt den Speicherort des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7c21f-145">-Name</span><span class="sxs-lookup"><span data-stu-id="7c21f-145">-Name</span></span>
<span data-ttu-id="7c21f-146">Gibt den Namen der benutzerdefinierten Skripterweiterung an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="7c21f-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c21f-147">-NoWait</span></span>
<span data-ttu-id="7c21f-148">Startet den Vorgang und kehrt unmittelbar vor Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="7c21f-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7c21f-149">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7c21f-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7c21f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c21f-150">-ResourceGroupName</span></span>
<span data-ttu-id="7c21f-151">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7c21f-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c21f-152">-ResourceId</span></span>
<span data-ttu-id="7c21f-153">VM extension ResourceID.</span><span class="sxs-lookup"><span data-stu-id="7c21f-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="7c21f-154">-Run</span><span class="sxs-lookup"><span data-stu-id="7c21f-154">-Run</span></span>
<span data-ttu-id="7c21f-155">Gibt den Befehl an, mit dem das Skript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c21f-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="7c21f-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="7c21f-156">-SecureExecution</span></span>
<span data-ttu-id="7c21f-157">Zeigt an, dass mit diesem Cmdlet sichergestellt wird, dass der Wert des Parameters *"Ausführen"* nicht auf dem Server protokolliert oder mithilfe der GET-Erweiterungs-API an den Benutzer zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7c21f-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="7c21f-158">Der Wert von *"Ausführen"* enthält möglicherweise geheime Daten oder Kennwörter, die sicher an die Skriptdatei übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c21f-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="7c21f-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7c21f-159">-StorageAccountKey</span></span>
<span data-ttu-id="7c21f-160">Gibt den Schlüssel für den Azure -Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="7c21f-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c21f-161">-StorageAccountName</span></span>
<span data-ttu-id="7c21f-162">Gibt den Namen des Azure-Speicherkontos an, in dem dieses Cmdlet das Skript speichert.</span><span class="sxs-lookup"><span data-stu-id="7c21f-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="7c21f-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7c21f-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="7c21f-164">Gibt das Suffix des Speicherendpunkts an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="7c21f-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7c21f-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="7c21f-166">Gibt die Version der Erweiterung an, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c21f-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="7c21f-167">Führen Sie zum Abrufen der Version das cmdlet Get-AzVMExtensionImage mit dem Wert "Microsoft.Compute" für den Parameter *"PublisherName"* und "CustomScriptExtension" für den Parameter *"Type"* aus.</span><span class="sxs-lookup"><span data-stu-id="7c21f-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="7c21f-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c21f-168">-VMName</span></span>
<span data-ttu-id="7c21f-169">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7c21f-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7c21f-170">Dieses Cmdlet fügt die benutzerdefinierte Skripterweiterung für den virtuellen Computer hinzu, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7c21f-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c21f-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="7c21f-171">-VMObject</span></span>
<span data-ttu-id="7c21f-172">VM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7c21f-172">VM object.</span></span>

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

### <span data-ttu-id="7c21f-173">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c21f-173">-Confirm</span></span>
<span data-ttu-id="7c21f-174">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c21f-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c21f-175">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7c21f-175">-WhatIf</span></span>
<span data-ttu-id="7c21f-176">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c21f-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c21f-177">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c21f-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c21f-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c21f-178">CommonParameters</span></span>
<span data-ttu-id="7c21f-179">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c21f-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c21f-180">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c21f-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c21f-181">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c21f-181">INPUTS</span></span>

### <span data-ttu-id="7c21f-182">System.String</span><span class="sxs-lookup"><span data-stu-id="7c21f-182">System.String</span></span>

### <span data-ttu-id="7c21f-183">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7c21f-183">System.String[]</span></span>

### <span data-ttu-id="7c21f-184">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7c21f-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7c21f-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c21f-185">OUTPUTS</span></span>

### <span data-ttu-id="7c21f-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7c21f-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7c21f-187">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c21f-187">NOTES</span></span>

## <span data-ttu-id="7c21f-188">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c21f-188">RELATED LINKS</span></span>

[<span data-ttu-id="7c21f-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7c21f-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="7c21f-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7c21f-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


