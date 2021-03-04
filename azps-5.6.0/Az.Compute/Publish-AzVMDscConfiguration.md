---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: a57ed6bb12a1357ebd8d9b4f090bd1d551f3c554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937099"
---
# <span data-ttu-id="46c80-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="46c80-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="46c80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46c80-102">SYNOPSIS</span></span>
<span data-ttu-id="46c80-103">Lädt ein DSC-Skript in den Azure-Blobspeicher hoch.</span><span class="sxs-lookup"><span data-stu-id="46c80-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="46c80-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46c80-104">SYNTAX</span></span>

### <span data-ttu-id="46c80-105">UploadArchive (Standard)</span><span class="sxs-lookup"><span data-stu-id="46c80-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c80-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="46c80-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46c80-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46c80-107">DESCRIPTION</span></span>
<span data-ttu-id="46c80-108">Das **Cmdlet Publish-AzVMDscConfiguration** lädt ein Dsc-Skript (Desired State Configuration) in azure blob storage hoch, das später mithilfe des Set-AzVMDscExtension-Cmdlets auf virtuelle Azure-Computer angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="46c80-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="46c80-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="46c80-109">EXAMPLES</span></span>

### <span data-ttu-id="46c80-110">Beispiel 1: Erstellen eines ZIP-Pakets, um es in den Azure-Speicher hochzuladen</span><span class="sxs-lookup"><span data-stu-id="46c80-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="46c80-111">Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in den Azure-Speicher hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="46c80-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="46c80-112">Beispiel 2: Erstellen eines ZIP-Pakets und Speichern in einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="46c80-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="46c80-113">Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in der lokalen Datei mit dem Namen .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="46c80-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="46c80-114">Beispiel 3: Hinzufügen einer Konfiguration zum Archiv und Hochladen in den Speicher</span><span class="sxs-lookup"><span data-stu-id="46c80-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="46c80-115">Mit diesem Befehl wird die Konfiguration Sample.ps1 dem Konfigurationsarchiv zum Hochladen in den Azure-Speicher und abhängige Ressourcenmodule übersprungen.</span><span class="sxs-lookup"><span data-stu-id="46c80-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="46c80-116">Beispiel 4: Hinzufügen von Konfigurations- und Konfigurationsdaten zum Archiv und anschließendes Hochladen in den Speicher</span><span class="sxs-lookup"><span data-stu-id="46c80-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="46c80-117">Mit diesem Befehl werden dem Konfigurationsarchiv Sample.ps1 Konfigurationsdaten SampleData.psd1 zum Hochladen in den Azure-Speicher hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="46c80-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="46c80-118">Beispiel 5: Hinzufügen von Konfigurations-, Konfigurationsdaten und zusätzlichen Inhalten zum Archiv und anschließendes Hochladen in den Speicher</span><span class="sxs-lookup"><span data-stu-id="46c80-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="46c80-119">Mit diesem Befehl werden konfiguration namens Sample.ps1, Konfigurationsdaten SampleData.psd1 und zusätzliche Inhalte zum Konfigurationsarchiv zum Hochladen in den Azure-Speicher addiert.</span><span class="sxs-lookup"><span data-stu-id="46c80-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="46c80-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="46c80-120">PARAMETERS</span></span>

### <span data-ttu-id="46c80-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="46c80-121">-AdditionalPath</span></span>
<span data-ttu-id="46c80-122">Gibt den Pfad einer Datei oder eines Verzeichnisses an, der in das Konfigurationsarchiv ein-/ausg.</span><span class="sxs-lookup"><span data-stu-id="46c80-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="46c80-123">Sie wird zusammen mit der Konfiguration auf den virtuellen Computer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="46c80-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c80-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="46c80-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="46c80-125">Gibt den Pfad einer PSD1-Datei an, der die Daten für die Konfiguration angibt.</span><span class="sxs-lookup"><span data-stu-id="46c80-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="46c80-126">Dies wird dem Konfigurationsarchiv hinzugefügt und dann an die Konfigurationsfunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="46c80-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="46c80-127">Sie wird vom Konfigurationsdatenpfad überschrieben, der über das cmdlet Set-AzVMDscExtension wird.</span><span class="sxs-lookup"><span data-stu-id="46c80-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="46c80-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="46c80-128">-ConfigurationPath</span></span>
<span data-ttu-id="46c80-129">Gibt den Pfad einer Datei an, die eine oder mehrere Konfigurationen enthält.</span><span class="sxs-lookup"><span data-stu-id="46c80-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="46c80-130">Bei der Datei kann es sich Windows PowerShell -Skriptdatei (PS1) oder Windows PowerShell -Moduldatei (PSM1) um eine datei.</span><span class="sxs-lookup"><span data-stu-id="46c80-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46c80-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="46c80-131">-ContainerName</span></span>
<span data-ttu-id="46c80-132">Gibt den Namen des Azure-Speichercontainers an, in den die Konfiguration hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="46c80-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c80-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c80-133">-DefaultProfile</span></span>
<span data-ttu-id="46c80-134">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46c80-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c80-135">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="46c80-135">-Force</span></span>
<span data-ttu-id="46c80-136">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="46c80-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46c80-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="46c80-137">-OutputArchivePath</span></span>
<span data-ttu-id="46c80-138">Gibt den Pfad einer lokalen ZIP-Datei an, in die das Konfigurationsarchiv geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="46c80-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="46c80-139">Wenn dieser Parameter verwendet wird, wird das Konfigurationsskript nicht in den Azure-Blobspeicher hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="46c80-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c80-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c80-140">-ResourceGroupName</span></span>
<span data-ttu-id="46c80-141">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="46c80-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c80-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="46c80-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="46c80-143">Gibt an, dass dieses Cmdlet DSC-Ressourcenabhängigkeiten aus dem Konfigurationsarchiv ausschließt.</span><span class="sxs-lookup"><span data-stu-id="46c80-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="46c80-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="46c80-144">-StorageAccountName</span></span>
<span data-ttu-id="46c80-145">Gibt den Namen des Azure-Speicherkontos an, der zum Hochladen des Konfigurationsskripts in den Container verwendet wird, der vom *Parameter ContainerName angegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="46c80-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c80-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="46c80-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="46c80-147">Gibt das Suffix für den Speicherendpunkt an.</span><span class="sxs-lookup"><span data-stu-id="46c80-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c80-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46c80-148">-Confirm</span></span>
<span data-ttu-id="46c80-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46c80-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c80-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c80-150">-WhatIf</span></span>
<span data-ttu-id="46c80-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46c80-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c80-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46c80-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c80-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c80-153">CommonParameters</span></span>
<span data-ttu-id="46c80-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c80-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c80-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46c80-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c80-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="46c80-156">INPUTS</span></span>

### <span data-ttu-id="46c80-157">System.String</span><span class="sxs-lookup"><span data-stu-id="46c80-157">System.String</span></span>

### <span data-ttu-id="46c80-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="46c80-158">System.String[]</span></span>

## <span data-ttu-id="46c80-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="46c80-159">OUTPUTS</span></span>

### <span data-ttu-id="46c80-160">System.String</span><span class="sxs-lookup"><span data-stu-id="46c80-160">System.String</span></span>

## <span data-ttu-id="46c80-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="46c80-161">NOTES</span></span>

## <span data-ttu-id="46c80-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="46c80-162">RELATED LINKS</span></span>

[<span data-ttu-id="46c80-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="46c80-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="46c80-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="46c80-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="46c80-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="46c80-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


