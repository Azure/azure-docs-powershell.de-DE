---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: ccad3d793ec5763a4c7db44d2b5ff3583b35402b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844208"
---
# <span data-ttu-id="4d77b-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4d77b-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="4d77b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d77b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d77b-103">Konfiguriert die DSC-Erweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4d77b-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="4d77b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d77b-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d77b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d77b-105">DESCRIPTION</span></span>
<span data-ttu-id="4d77b-106">Das Cmdlet " **festlegen-AzVMDscExtension** " konfiguriert die Windows PowerShell-Erweiterung "desired state Configuration (DSC)" auf einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d77b-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="4d77b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d77b-107">EXAMPLES</span></span>

### <span data-ttu-id="4d77b-108">Beispiel 1: Einrichten einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="4d77b-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="4d77b-109">Mit diesem Befehl wird die DSC-Erweiterung auf dem virtuellen Computer mit dem Namen VM07 so festgelegt, dass Sample.ps1.zip aus dem Speicherkonto "STG" und dem Standardcontainer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="4d77b-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="4d77b-110">Der Befehl ruft die Konfiguration mit dem Namen configname auf.</span><span class="sxs-lookup"><span data-stu-id="4d77b-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="4d77b-111">Die Sample.ps1.zip-Datei wurde zuvor mithilfe von **Publish-AzVMDscConfiguration** hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="4d77b-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="4d77b-112">Beispiel 2: Einrichten einer DSC-Erweiterung mit Konfigurationsdaten</span><span class="sxs-lookup"><span data-stu-id="4d77b-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="4d77b-113">Mit diesem Befehl wird die Erweiterung auf dem virtuellen Computer mit dem Namen VM13 festgelegt, um Sample.ps1.zip aus dem Speicherkonto mit dem Namen STG und dem Container mit dem Namen WindowsPowerShellDSC herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4d77b-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="4d77b-114">Der Befehl die Konfiguration mit dem Namen configname und gibt Konfigurationsdaten und-Argumente an.</span><span class="sxs-lookup"><span data-stu-id="4d77b-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="4d77b-115">Die Sample.ps1.zip-Datei wurde zuvor mithilfe von **Publish-AzVMDscConfiguration** hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="4d77b-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="4d77b-116">Beispiel 3: Einrichten einer DSC-Erweiterung mit Konfigurationsdaten, die automatisch aktualisiert werden</span><span class="sxs-lookup"><span data-stu-id="4d77b-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="4d77b-117">Mit diesem Befehl wird die Erweiterung auf dem virtuellen Computer mit dem Namen VM22 festgelegt, um Sample.ps1.zip aus dem Speicherkonto mit dem Namen STG und dem Container mit dem Namen WindowsPowerShellDSC herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4d77b-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="4d77b-118">Der Befehl ruft die Konfiguration mit dem Namen configname auf und gibt Konfigurationsdaten und-Argumente an.</span><span class="sxs-lookup"><span data-stu-id="4d77b-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="4d77b-119">Dieser Befehl ermöglicht auch die automatische Aktualisierung des Erweiterungs Handlers auf die neueste Version.</span><span class="sxs-lookup"><span data-stu-id="4d77b-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="4d77b-120">Die Sample.ps1.zip wurde zuvor mithilfe von **Publish-AzVMDscConfiguration** hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="4d77b-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="4d77b-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d77b-121">PARAMETERS</span></span>

### <span data-ttu-id="4d77b-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="4d77b-122">-ArchiveBlobName</span></span>
<span data-ttu-id="4d77b-123">Gibt den Namen der Konfigurationsdatei an, die zuvor vom Publish-AzVMDscConfiguration-Cmdlet hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="4d77b-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="4d77b-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="4d77b-124">-ArchiveContainerName</span></span>
<span data-ttu-id="4d77b-125">Arten Name des Azure-Speichercontainers, in dem sich das Konfigurations Archiv befindet.</span><span class="sxs-lookup"><span data-stu-id="4d77b-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="4d77b-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d77b-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="4d77b-127">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält, das das Konfigurations Archiv enthält.</span><span class="sxs-lookup"><span data-stu-id="4d77b-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="4d77b-128">Dieser Parameter ist optional, wenn sich das Speicherkonto und der virtuelle Computer beide in derselben Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="4d77b-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="4d77b-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4d77b-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="4d77b-130">Gibt den Namen des Azure-speicherkontos an, das zum Herunterladen der ArchiveBlobName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d77b-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="4d77b-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d77b-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="4d77b-132">Gibt das Suffix für das Speicher Endpunkt an.</span><span class="sxs-lookup"><span data-stu-id="4d77b-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="4d77b-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4d77b-133">-AutoUpdate</span></span>
<span data-ttu-id="4d77b-134">Gibt die Version des Erweiterungs Handlers an, die vom *Version* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d77b-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="4d77b-135">Standardmäßig wird der Erweiterungshandler nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4d77b-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="4d77b-136">Verwenden Sie *den AutoUpdate-Parameter,* um die automatische Aktualisierung des Erweiterungs Handlers auf die neueste Version zu aktivieren, sobald diese verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4d77b-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="4d77b-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="4d77b-137">-ConfigurationArgument</span></span>
<span data-ttu-id="4d77b-138">Gibt eine Hashtabelle an, die die Argumente für die Konfigurationsfunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="4d77b-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="4d77b-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="4d77b-139">-ConfigurationData</span></span>
<span data-ttu-id="4d77b-140">Gibt den Pfad einer psd1-Datei an, die die Daten für die Konfiguration angibt.</span><span class="sxs-lookup"><span data-stu-id="4d77b-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="4d77b-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4d77b-141">-ConfigurationName</span></span>
<span data-ttu-id="4d77b-142">Gibt den Namen der Konfiguration an, die von der DSC-Erweiterung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4d77b-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="4d77b-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="4d77b-143">-DataCollection</span></span>
<span data-ttu-id="4d77b-144">Gibt den Typ der Datensammlung an.</span><span class="sxs-lookup"><span data-stu-id="4d77b-144">Specifies the data collection type.</span></span>
<span data-ttu-id="4d77b-145">Die zulässigen Werte für diesen Parameter sind: Aktivieren und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4d77b-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="4d77b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d77b-146">-DefaultProfile</span></span>
<span data-ttu-id="4d77b-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d77b-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d77b-148">-Force</span><span class="sxs-lookup"><span data-stu-id="4d77b-148">-Force</span></span>
<span data-ttu-id="4d77b-149">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4d77b-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d77b-150">-Standort</span><span class="sxs-lookup"><span data-stu-id="4d77b-150">-Location</span></span>
<span data-ttu-id="4d77b-151">Gibt den Pfad der Ressourcenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="4d77b-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="4d77b-152">-Name</span><span class="sxs-lookup"><span data-stu-id="4d77b-152">-Name</span></span>
<span data-ttu-id="4d77b-153">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="4d77b-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="4d77b-154">Der Standardwert ist Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="4d77b-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="4d77b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d77b-155">-ResourceGroupName</span></span>
<span data-ttu-id="4d77b-156">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4d77b-156">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4d77b-157">-Version</span><span class="sxs-lookup"><span data-stu-id="4d77b-157">-Version</span></span>
<span data-ttu-id="4d77b-158">Gibt die Version der DSC-Erweiterung an, auf die die Einstellungen Set-AzVMDscExtension angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d77b-158">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="4d77b-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="4d77b-159">-VMName</span></span>
<span data-ttu-id="4d77b-160">Gibt den Namen des virtuellen Computers an, auf dem der DSC-Erweiterungshandler installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4d77b-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="4d77b-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="4d77b-161">-WmfVersion</span></span>
<span data-ttu-id="4d77b-162">Gibt die WMF-Version an.</span><span class="sxs-lookup"><span data-stu-id="4d77b-162">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="4d77b-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d77b-163">-Confirm</span></span>
<span data-ttu-id="4d77b-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d77b-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d77b-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d77b-165">-WhatIf</span></span>
<span data-ttu-id="4d77b-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d77b-166">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4d77b-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d77b-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d77b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d77b-168">CommonParameters</span></span>
<span data-ttu-id="4d77b-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d77b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d77b-170">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d77b-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d77b-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d77b-171">INPUTS</span></span>

### <span data-ttu-id="4d77b-172">Keine</span><span class="sxs-lookup"><span data-stu-id="4d77b-172">None</span></span>
<span data-ttu-id="4d77b-173">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4d77b-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d77b-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d77b-174">OUTPUTS</span></span>

### <span data-ttu-id="4d77b-175">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4d77b-175">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4d77b-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d77b-176">NOTES</span></span>

## <span data-ttu-id="4d77b-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d77b-177">RELATED LINKS</span></span>

[<span data-ttu-id="4d77b-178">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4d77b-178">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="4d77b-179">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4d77b-179">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="4d77b-180">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d77b-180">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


