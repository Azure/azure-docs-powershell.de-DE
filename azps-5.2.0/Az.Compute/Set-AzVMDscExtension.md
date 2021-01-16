---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294880"
---
# <span data-ttu-id="eda0b-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="eda0b-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="eda0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda0b-102">SYNOPSIS</span></span>
<span data-ttu-id="eda0b-103">Konfiguriert die DSC-Erweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="eda0b-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="eda0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eda0b-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda0b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eda0b-105">DESCRIPTION</span></span>
<span data-ttu-id="eda0b-106">Das **Cmdlet Set-AzVMDscExtension** konfiguriert die Windows PowerShell Desired State Configuration (DSC)-Erweiterung auf einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eda0b-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="eda0b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eda0b-107">EXAMPLES</span></span>

### <span data-ttu-id="eda0b-108">Beispiel 1: Festlegen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="eda0b-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="eda0b-109">Mit diesem Befehl wird die DSC-Erweiterung auf dem virtuellen Computer VM07 so festgelegt, dass sie Sample.ps1.zip aus dem Speicherkonto "Stg" und dem Standardcontainer heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="eda0b-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="eda0b-110">Der Befehl ruft die Konfiguration mit dem Namen "ConfigName" auf.</span><span class="sxs-lookup"><span data-stu-id="eda0b-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="eda0b-111">Die Sample.ps1.zip wurde zuvor mit **Publish-AzVMDscConfiguration hochgeladen.**</span><span class="sxs-lookup"><span data-stu-id="eda0b-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="eda0b-112">Beispiel 2: Festlegen einer DSC-Erweiterung mit Konfigurationsdaten</span><span class="sxs-lookup"><span data-stu-id="eda0b-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="eda0b-113">Dieser Befehl legt die Erweiterung auf dem virtuellen Computer VM13 fest, um Sample.ps1.zip aus dem Speicherkonto "Stg" und dem Container "WindowsPowerShellDSC" herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="eda0b-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="eda0b-114">Der Befehl der Konfiguration namens "ConfigName" und gibt Konfigurationsdaten und Argumente an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="eda0b-115">Die Sample.ps1.zip wurde zuvor mit **Publish-AzVMDscConfiguration hochgeladen.**</span><span class="sxs-lookup"><span data-stu-id="eda0b-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="eda0b-116">Beispiel 3: Festlegen einer DSC-Erweiterung mit Konfigurationsdaten, die über ein automatisches Update verfügt</span><span class="sxs-lookup"><span data-stu-id="eda0b-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="eda0b-117">Dieser Befehl legt die Erweiterung auf dem virtuellen Computer VM22 so fest, dass sie Sample.ps1.zip aus dem Speicherkonto "Stg" und dem Container "WindowsPowerShellDSC" heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="eda0b-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="eda0b-118">Der Befehl ruft die Konfiguration mit dem Namen "ConfigName" auf und gibt Konfigurationsdaten und Argumente an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="eda0b-119">Dieser Befehl ermöglicht auch die automatische Aktualisierung des Erweiterungshandlers auf die neueste Version.</span><span class="sxs-lookup"><span data-stu-id="eda0b-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="eda0b-120">Die Sample.ps1.zip wurde zuvor mithilfe von **Publish-AzVMDscConfiguration hochgeladen.**</span><span class="sxs-lookup"><span data-stu-id="eda0b-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="eda0b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eda0b-121">PARAMETERS</span></span>

### <span data-ttu-id="eda0b-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="eda0b-122">-ArchiveBlobName</span></span>
<span data-ttu-id="eda0b-123">Gibt den Namen der Konfigurationsdatei an, die zuvor vom Publish-AzVMDscConfiguration hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="eda0b-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="eda0b-124">-ArchiveContainerName</span></span>
<span data-ttu-id="eda0b-125">Artenname des Azure-Speichercontainers, in dem sich das Konfigurationsarchiv befindet.</span><span class="sxs-lookup"><span data-stu-id="eda0b-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda0b-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="eda0b-127">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält, das das Konfigurationsarchiv enthält.</span><span class="sxs-lookup"><span data-stu-id="eda0b-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="eda0b-128">Dieser Parameter ist optional, wenn sich das Speicherkonto und der virtuelle Computer in derselben Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="eda0b-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="eda0b-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="eda0b-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="eda0b-130">Gibt den Namen des Azure-Speicherkontos an, der zum Herunterladen von ArchiveBlobName verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eda0b-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="eda0b-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="eda0b-132">Gibt das Suffix des Speicherendpunkts an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="eda0b-133">-AutoUpdate</span></span>
<span data-ttu-id="eda0b-134">Gibt die durch den Parameter *"Version"* angegebene Version des Erweiterungshandlers an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="eda0b-135">Standardmäßig ist der Erweiterungshandler nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="eda0b-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="eda0b-136">Verwenden Sie *den Parameter "AutoUpdate",* um die automatische Aktualisierung des Erweiterungshandlers auf die neueste Version zu aktivieren, sobald diese verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eda0b-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="eda0b-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="eda0b-137">-ConfigurationArgument</span></span>
<span data-ttu-id="eda0b-138">Gibt eine Hashtabelle an, die die Argumente für die Konfigurationsfunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="eda0b-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="eda0b-139">-ConfigurationData</span></span>
<span data-ttu-id="eda0b-140">Gibt den Pfad einer PSD1-Datei an, der die Daten für die Konfiguration angibt.</span><span class="sxs-lookup"><span data-stu-id="eda0b-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="eda0b-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="eda0b-141">-ConfigurationName</span></span>
<span data-ttu-id="eda0b-142">Gibt den Namen der Konfiguration an, die von der DSC-Erweiterung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eda0b-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="eda0b-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="eda0b-143">-DataCollection</span></span>
<span data-ttu-id="eda0b-144">Gibt den Datensammlungstyp an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-144">Specifies the data collection type.</span></span>
<span data-ttu-id="eda0b-145">Die zulässigen Werte für diesen Parameter sind: Aktivieren und Deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="eda0b-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda0b-146">-DefaultProfile</span></span>
<span data-ttu-id="eda0b-147">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eda0b-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda0b-148">-Force</span><span class="sxs-lookup"><span data-stu-id="eda0b-148">-Force</span></span>
<span data-ttu-id="eda0b-149">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="eda0b-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eda0b-150">-Location</span><span class="sxs-lookup"><span data-stu-id="eda0b-150">-Location</span></span>
<span data-ttu-id="eda0b-151">Gibt den Pfad der Ressourcenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="eda0b-152">-Name</span><span class="sxs-lookup"><span data-stu-id="eda0b-152">-Name</span></span>
<span data-ttu-id="eda0b-153">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="eda0b-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="eda0b-154">Der Standardwert ist "Microsoft.Powershell.DSC".</span><span class="sxs-lookup"><span data-stu-id="eda0b-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="eda0b-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eda0b-155">-NoWait</span></span>
<span data-ttu-id="eda0b-156">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="eda0b-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="eda0b-157">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="eda0b-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="eda0b-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda0b-158">-ResourceGroupName</span></span>
<span data-ttu-id="eda0b-159">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-159">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-160">-Version</span><span class="sxs-lookup"><span data-stu-id="eda0b-160">-Version</span></span>
<span data-ttu-id="eda0b-161">Gibt die Version der DSC-Erweiterung an, auf die Set-AzVMDscExtension die Einstellungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="eda0b-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="eda0b-162">-VMName</span></span>
<span data-ttu-id="eda0b-163">Gibt den Namen des virtuellen Computers an, auf dem der DSC-Erweiterungshandler installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eda0b-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-164">-WMFVersion</span><span class="sxs-lookup"><span data-stu-id="eda0b-164">-WmfVersion</span></span>
<span data-ttu-id="eda0b-165">Gibt die WmF-Version an.</span><span class="sxs-lookup"><span data-stu-id="eda0b-165">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eda0b-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eda0b-166">-Confirm</span></span>
<span data-ttu-id="eda0b-167">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eda0b-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda0b-168">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="eda0b-168">-WhatIf</span></span>
<span data-ttu-id="eda0b-169">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eda0b-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda0b-170">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eda0b-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda0b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda0b-171">CommonParameters</span></span>
<span data-ttu-id="eda0b-172">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda0b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda0b-173">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eda0b-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda0b-174">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eda0b-174">INPUTS</span></span>

### <span data-ttu-id="eda0b-175">System.String</span><span class="sxs-lookup"><span data-stu-id="eda0b-175">System.String</span></span>

### <span data-ttu-id="eda0b-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eda0b-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eda0b-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eda0b-177">OUTPUTS</span></span>

### <span data-ttu-id="eda0b-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eda0b-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eda0b-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eda0b-179">NOTES</span></span>

## <span data-ttu-id="eda0b-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eda0b-180">RELATED LINKS</span></span>

[<span data-ttu-id="eda0b-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="eda0b-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="eda0b-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="eda0b-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="eda0b-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="eda0b-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


