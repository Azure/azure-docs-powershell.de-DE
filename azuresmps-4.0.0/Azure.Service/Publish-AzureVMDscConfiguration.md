---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006088"
---
# <span data-ttu-id="7ebeb-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ebeb-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="7ebeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ebeb-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebeb-103">Veröffentlicht ein gewünschtes Zustands Konfigurationsskript im Azure BLOB-Speicher.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="7ebeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ebeb-104">SYNTAX</span></span>

### <span data-ttu-id="7ebeb-105">UploadArchive (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ebeb-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ebeb-106">Createarchiv</span><span class="sxs-lookup"><span data-stu-id="7ebeb-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebeb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ebeb-107">DESCRIPTION</span></span>
<span data-ttu-id="7ebeb-108">Das Cmdlet " **Publish-AzureVMDscConfiguration** " veröffentlicht ein gewünschtes Zustands Konfigurationsskript im Azure BLOB-Speicher, das später auf Azure Virtual Machines mithilfe des Cmdlets " **setAzureVMDscExtension** " angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="7ebeb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ebeb-109">EXAMPLES</span></span>

### <span data-ttu-id="7ebeb-110">Beispiel 1: Veröffentlichen eines Zustands Konfigurationsskripts in BLOB-Speicher</span><span class="sxs-lookup"><span data-stu-id="7ebeb-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="7ebeb-111">Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und in den Azure-Speicher hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="7ebeb-112">Beispiel 2: Veröffentlichen eines Zustands Konfigurationsskripts in einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="7ebeb-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="7ebeb-113">Mit diesem Befehl wird ein ZIP-Paket für das angegebene Skript und alle abhängigen Ressourcenmodule erstellt und im lokalen Datei .\MyConfiguration.ps1.zip gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="7ebeb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ebeb-114">PARAMETERS</span></span>

### <span data-ttu-id="7ebeb-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="7ebeb-115">-AdditionalPath</span></span>
<span data-ttu-id="7ebeb-116">Gibt ein Array zusätzlicher Pfade an.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-116">Specifies an array of additional paths.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="7ebeb-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="7ebeb-118">Gibt den Pfad einer lokalen ZIP-Datei an, die von diesem Cmdlet in das Konfigurations Archiv geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="7ebeb-119">Wenn Sie diesen Parameter verwenden, wird das Konfigurationsskript nicht in den Azure BLOB-Speicher hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="7ebeb-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="7ebeb-121">Gibt einen Konfigurationsdaten Pfad an.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="7ebeb-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="7ebeb-122">-ConfigurationPath</span></span>
<span data-ttu-id="7ebeb-123">Gibt den Pfad einer Datei an, die eine oder mehrere Konfigurationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="7ebeb-124">Bei der Datei kann es sich um ein Windows PowerShell-Skript (PS1-Datei), ein Modul (psm1-Datei) oder ein Archiv (ZIP-Datei) mit einer Reihe von Windows PowerShell-Modulen mit jedem Modul in einem separaten Verzeichnis handeln.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-125">-Containername</span><span class="sxs-lookup"><span data-stu-id="7ebeb-125">-ContainerName</span></span>
<span data-ttu-id="7ebeb-126">Gibt den Namen des Azure-Speichercontainers an, in den die Konfiguration hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7ebeb-127">-Force</span></span>
<span data-ttu-id="7ebeb-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ebeb-129">-Information</span><span class="sxs-lookup"><span data-stu-id="7ebeb-129">-InformationAction</span></span>
<span data-ttu-id="7ebeb-130">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7ebeb-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7ebeb-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7ebeb-132">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="7ebeb-132">Continue</span></span>
- <span data-ttu-id="7ebeb-133">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="7ebeb-133">Ignore</span></span>
- <span data-ttu-id="7ebeb-134">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="7ebeb-134">Inquire</span></span>
- <span data-ttu-id="7ebeb-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7ebeb-135">SilentlyContinue</span></span>
- <span data-ttu-id="7ebeb-136">Beenden</span><span class="sxs-lookup"><span data-stu-id="7ebeb-136">Stop</span></span>
- <span data-ttu-id="7ebeb-137">Anhalten</span><span class="sxs-lookup"><span data-stu-id="7ebeb-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7ebeb-138">-InformationVariable</span></span>
<span data-ttu-id="7ebeb-139">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ebeb-140">-PassThru</span></span>
<span data-ttu-id="7ebeb-141">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7ebeb-142">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7ebeb-143">-Profil</span><span class="sxs-lookup"><span data-stu-id="7ebeb-143">-Profile</span></span>
<span data-ttu-id="7ebeb-144">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7ebeb-145">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="7ebeb-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="7ebeb-147">Gibt an, dass dieses Cmdlet die Abhängigkeits Erkennung überspringt.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="7ebeb-148">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="7ebeb-148">-StorageContext</span></span>
<span data-ttu-id="7ebeb-149">Gibt den Azure-Speicherkontext an, der die Sicherheitseinstellungen zum Hochladen des Konfigurationsskripts in den Container bereitstellt, der durch den *Containername* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="7ebeb-150">Dieser Kontext bietet Schreibzugriff auf den Container.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7ebeb-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="7ebeb-152">Gibt das Suffix für den Speicher Endpunkt an, beispielsweise Core.contoso.net</span><span class="sxs-lookup"><span data-stu-id="7ebeb-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ebeb-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ebeb-153">-Confirm</span></span>
<span data-ttu-id="7ebeb-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ebeb-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebeb-155">-WhatIf</span></span>
<span data-ttu-id="7ebeb-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebeb-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ebeb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebeb-158">CommonParameters</span></span>
<span data-ttu-id="7ebeb-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebeb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebeb-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ebeb-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebeb-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ebeb-161">INPUTS</span></span>

## <span data-ttu-id="7ebeb-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ebeb-162">OUTPUTS</span></span>

## <span data-ttu-id="7ebeb-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ebeb-163">NOTES</span></span>

## <span data-ttu-id="7ebeb-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ebeb-164">RELATED LINKS</span></span>

[<span data-ttu-id="7ebeb-165">Satz-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7ebeb-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


