---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005888"
---
# <span data-ttu-id="0a90f-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0a90f-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="0a90f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a90f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a90f-103">Aktiviert die Anwendungs Diagnose auf einer Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="0a90f-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="0a90f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a90f-104">SYNTAX</span></span>

### <span data-ttu-id="0a90f-105">Fileparameterset</span><span class="sxs-lookup"><span data-stu-id="0a90f-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a90f-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a90f-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0a90f-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a90f-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a90f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a90f-108">DESCRIPTION</span></span>
<span data-ttu-id="0a90f-109">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0a90f-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0a90f-110">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0a90f-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0a90f-111">Aktiviert die Anwendungs Diagnose auf einer Azure-Website und ermöglicht die Konfiguration des Speichers von Protokollen in einem Dateisystem oder auf Azure-Speicher.</span><span class="sxs-lookup"><span data-stu-id="0a90f-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="0a90f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a90f-112">EXAMPLES</span></span>

### <span data-ttu-id="0a90f-113">Beispiel 1: Aktivieren der Diagnose mithilfe des Dateisystems</span><span class="sxs-lookup"><span data-stu-id="0a90f-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="0a90f-114">In diesem Beispiel wird die Anwendungsprotokollierung im Dateisystem mit Verbose-Ebene aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0a90f-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="0a90f-115">Beispiel 2: Aktivieren der Protokollierung mithilfe des Azure-Speichers</span><span class="sxs-lookup"><span data-stu-id="0a90f-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="0a90f-116">In diesem Beispiel wird die Anwendungsprotokollierung mithilfe des speicherkontos mit dem Namen "MyAccount" aktiviert, wobei Protokollierungsstufe auf Informationen eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="0a90f-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="0a90f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a90f-117">PARAMETERS</span></span>

### <span data-ttu-id="0a90f-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="0a90f-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a90f-119">-Datei</span><span class="sxs-lookup"><span data-stu-id="0a90f-119">-File</span></span>
<span data-ttu-id="0a90f-120">Gibt an, dass Sie ein Dateisystem zum Speichern der Protokolldateien verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0a90f-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a90f-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="0a90f-121">-LogLevel</span></span>
<span data-ttu-id="0a90f-122">Die Protokollebene, die gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a90f-122">The log level to store.</span></span>
<span data-ttu-id="0a90f-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0a90f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a90f-124">Fehler</span><span class="sxs-lookup"><span data-stu-id="0a90f-124">Error</span></span>
- <span data-ttu-id="0a90f-125">Warnung</span><span class="sxs-lookup"><span data-stu-id="0a90f-125">Warning</span></span>
- <span data-ttu-id="0a90f-126">Informationen</span><span class="sxs-lookup"><span data-stu-id="0a90f-126">Information</span></span>
- <span data-ttu-id="0a90f-127">Ausführliche</span><span class="sxs-lookup"><span data-stu-id="0a90f-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a90f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0a90f-128">-Name</span></span>
<span data-ttu-id="0a90f-129">Gibt den Namen der Azure-Website an.</span><span class="sxs-lookup"><span data-stu-id="0a90f-129">Specifies the name of the Azure website.</span></span>

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

### <span data-ttu-id="0a90f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a90f-130">-PassThru</span></span>
<span data-ttu-id="0a90f-131">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0a90f-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0a90f-132">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0a90f-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a90f-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="0a90f-133">-Profile</span></span>
<span data-ttu-id="0a90f-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0a90f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a90f-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0a90f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a90f-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="0a90f-136">-Slot</span></span>
<span data-ttu-id="0a90f-137">Gibt den Namen des Steckplatzes an.</span><span class="sxs-lookup"><span data-stu-id="0a90f-137">Specifies the name of the slot.</span></span>

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

### <span data-ttu-id="0a90f-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0a90f-138">-StorageAccountName</span></span>
<span data-ttu-id="0a90f-139">Das für die Speicherung der Protokolle zu verwendende Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="0a90f-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="0a90f-140">Wenn keine Angabe erfolgt, wird der CurrentStorageAccount verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a90f-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a90f-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="0a90f-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a90f-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="0a90f-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a90f-143">-Speicher</span><span class="sxs-lookup"><span data-stu-id="0a90f-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a90f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a90f-144">CommonParameters</span></span>
<span data-ttu-id="0a90f-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a90f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a90f-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a90f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a90f-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a90f-147">INPUTS</span></span>

## <span data-ttu-id="0a90f-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a90f-148">OUTPUTS</span></span>

## <span data-ttu-id="0a90f-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a90f-149">NOTES</span></span>

## <span data-ttu-id="0a90f-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a90f-150">RELATED LINKS</span></span>

[<span data-ttu-id="0a90f-151">Deaktivieren-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0a90f-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="0a90f-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0a90f-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="0a90f-153">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0a90f-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="0a90f-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0a90f-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="0a90f-155">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0a90f-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


