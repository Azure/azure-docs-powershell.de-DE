---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: a7bffb3b1387c084ef3b29ad6feb3962c724278f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481306"
---
# <span data-ttu-id="aa7b7-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="aa7b7-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="aa7b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa7b7-103">Konfiguriert die DSC-Erweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa7b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa7b7-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa7b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa7b7-105">DESCRIPTION</span></span>
<span data-ttu-id="aa7b7-106">Das Cmdlet " **festlegen-AzureRmVMDscExtension** " konfiguriert die Windows PowerShell-Erweiterung "desired state Configuration (DSC)" auf einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="aa7b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa7b7-107">EXAMPLES</span></span>

### <span data-ttu-id="aa7b7-108">Beispiel 1: Einrichten einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="aa7b7-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="aa7b7-109">Mit diesem Befehl wird die DSC-Erweiterung auf dem virtuellen Computer mit dem Namen VM07 so festgelegt, dass Sample.ps1.zip aus dem Speicherkonto "STG" und dem Standardcontainer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="aa7b7-110">Der Befehl ruft die Konfiguration mit dem Namen configname auf.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="aa7b7-111">Die Sample.ps1.zip-Datei wurde zuvor mithilfe von **Publish-AzureRmVMDscConfiguration** hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="aa7b7-112">Beispiel 2: Einrichten einer DSC-Erweiterung mit Konfigurationsdaten</span><span class="sxs-lookup"><span data-stu-id="aa7b7-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="aa7b7-113">Mit diesem Befehl wird die Erweiterung auf dem virtuellen Computer mit dem Namen VM13 festgelegt, um Sample.ps1.zip aus dem Speicherkonto mit dem Namen STG und dem Container mit dem Namen WindowsPowerShellDSC herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="aa7b7-114">Der Befehl die Konfiguration mit dem Namen configname und gibt Konfigurationsdaten und-Argumente an.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="aa7b7-115">Die Sample.ps1.zip-Datei wurde zuvor mithilfe von **Publish-AzureRmVMDscConfiguration** hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="aa7b7-116">Beispiel 3: Einrichten einer DSC-Erweiterung mit Konfigurationsdaten, die automatisch aktualisiert werden</span><span class="sxs-lookup"><span data-stu-id="aa7b7-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="aa7b7-117">Mit diesem Befehl wird die Erweiterung auf dem virtuellen Computer mit dem Namen VM22 festgelegt, um Sample.ps1.zip aus dem Speicherkonto mit dem Namen STG und dem Container mit dem Namen WindowsPowerShellDSC herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="aa7b7-118">Der Befehl ruft die Konfiguration mit dem Namen configname auf und gibt Konfigurationsdaten und-Argumente an.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="aa7b7-119">Dieser Befehl ermöglicht auch die automatische Aktualisierung des Erweiterungs Handlers auf die neueste Version.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="aa7b7-120">Die Sample.ps1.zip wurde zuvor mithilfe von **Publish-AzureRmVMDscConfiguration** hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="aa7b7-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa7b7-121">PARAMETERS</span></span>

### <span data-ttu-id="aa7b7-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="aa7b7-122">-ArchiveBlobName</span></span>
<span data-ttu-id="aa7b7-123">Gibt den Namen der Konfigurationsdatei an, die zuvor vom Publish-AzureRmVMDscConfiguration-Cmdlet hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="aa7b7-124">-ArchiveContainerName</span></span>
<span data-ttu-id="aa7b7-125">Arten Name des Azure-Speichercontainers, in dem sich das Konfigurations Archiv befindet.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa7b7-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="aa7b7-127">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält, das das Konfigurations Archiv enthält.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="aa7b7-128">Dieser Parameter ist optional, wenn sich das Speicherkonto und der virtuelle Computer beide in derselben Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="aa7b7-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa7b7-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="aa7b7-130">Gibt den Namen des Azure-speicherkontos an, das zum Herunterladen der ArchiveBlobName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="aa7b7-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="aa7b7-132">Gibt das Suffix für das Speicher Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="aa7b7-133">-AutoUpdate</span></span>
<span data-ttu-id="aa7b7-134">Gibt die Version des Erweiterungs Handlers an, die vom *Version* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="aa7b7-135">Standardmäßig wird der Erweiterungshandler nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="aa7b7-136">Verwenden Sie *den AutoUpdate-Parameter,* um die automatische Aktualisierung des Erweiterungs Handlers auf die neueste Version zu aktivieren, sobald diese verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="aa7b7-137">-ConfigurationArgument</span></span>
<span data-ttu-id="aa7b7-138">Gibt eine Hashtabelle an, die die Argumente für die Konfigurationsfunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="aa7b7-139">-ConfigurationData</span></span>
<span data-ttu-id="aa7b7-140">Gibt den Pfad einer psd1-Datei an, die die Daten für die Konfiguration angibt.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="aa7b7-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="aa7b7-141">-ConfigurationName</span></span>
<span data-ttu-id="aa7b7-142">Gibt den Namen der Konfiguration an, die von der DSC-Erweiterung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="aa7b7-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="aa7b7-143">-DataCollection</span></span>
<span data-ttu-id="aa7b7-144">Gibt den Typ der Datensammlung an.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-144">Specifies the data collection type.</span></span>
<span data-ttu-id="aa7b7-145">Die zulässigen Werte für diesen Parameter sind: Aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-146">-Force</span><span class="sxs-lookup"><span data-stu-id="aa7b7-146">-Force</span></span>
<span data-ttu-id="aa7b7-147">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-147">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-148">-Standort</span><span class="sxs-lookup"><span data-stu-id="aa7b7-148">-Location</span></span>
<span data-ttu-id="aa7b7-149">Gibt den Pfad der Ressourcenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-149">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="aa7b7-150">-Name</span><span class="sxs-lookup"><span data-stu-id="aa7b7-150">-Name</span></span>
<span data-ttu-id="aa7b7-151">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="aa7b7-152">Der Standardwert ist Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-152">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="aa7b7-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa7b7-153">-ResourceGroupName</span></span>
<span data-ttu-id="aa7b7-154">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-154">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-155">-Version</span><span class="sxs-lookup"><span data-stu-id="aa7b7-155">-Version</span></span>
<span data-ttu-id="aa7b7-156">Gibt die Version der DSC-Erweiterung an, auf die die Einstellungen Set-AzureRmVMDscExtension angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-156">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="aa7b7-157">-VMName</span></span>
<span data-ttu-id="aa7b7-158">Gibt den Namen des virtuellen Computers an, auf dem der DSC-Erweiterungshandler installiert ist.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-158">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-159">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="aa7b7-159">-WmfVersion</span></span>
<span data-ttu-id="aa7b7-160">Gibt die WMF-Version an.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-160">Specifies the WMF version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa7b7-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa7b7-161">-Confirm</span></span>
<span data-ttu-id="aa7b7-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa7b7-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa7b7-163">-WhatIf</span></span>
<span data-ttu-id="aa7b7-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-164">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="aa7b7-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa7b7-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7b7-166">CommonParameters</span></span>
<span data-ttu-id="aa7b7-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7b7-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa7b7-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7b7-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa7b7-169">INPUTS</span></span>

### <span data-ttu-id="aa7b7-170">Keine</span><span class="sxs-lookup"><span data-stu-id="aa7b7-170">None</span></span>
<span data-ttu-id="aa7b7-171">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="aa7b7-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa7b7-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa7b7-172">OUTPUTS</span></span>

## <span data-ttu-id="aa7b7-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa7b7-173">NOTES</span></span>

## <span data-ttu-id="aa7b7-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa7b7-174">RELATED LINKS</span></span>

[<span data-ttu-id="aa7b7-175">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="aa7b7-175">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="aa7b7-176">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="aa7b7-176">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="aa7b7-177">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa7b7-177">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)


