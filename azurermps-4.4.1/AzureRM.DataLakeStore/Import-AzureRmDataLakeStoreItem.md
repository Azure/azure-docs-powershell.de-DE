---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663951"
---
# <span data-ttu-id="7e7e7-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="7e7e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7e7-103">Lädt eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hoch.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e7e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e7e7-104">SYNTAX</span></span>

### <span data-ttu-id="7e7e7-105">Keine Diagnoseprotokollierung (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e7e7-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7e7-106">Einbeziehen der Diagnoseprotokollierung</span><span class="sxs-lookup"><span data-stu-id="7e7e7-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e7e7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e7e7-107">DESCRIPTION</span></span>
<span data-ttu-id="7e7e7-108">Mit dem Cmdlet " **Import-AzureRmDataLakeStoreItem** " wird eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="7e7e7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e7e7-109">EXAMPLES</span></span>

### <span data-ttu-id="7e7e7-110">Beispiel 1: Hochladen einer Datei</span><span class="sxs-lookup"><span data-stu-id="7e7e7-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="7e7e7-111">Mit diesem Befehl wird die Datei SrcFile.csv hochgeladen und dem Ordner "meine Dateien" im Data Lake Store als File.csv hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="7e7e7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e7e7-112">PARAMETERS</span></span>

### <span data-ttu-id="7e7e7-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="7e7e7-113">-Account</span></span>
<span data-ttu-id="7e7e7-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="7e7e7-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="7e7e7-116">Geben Sie die maximale Anzahl von Dateien an, die parallel für einen Ordner Upload hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="7e7e7-117">Der Standardwert ist Five (5).</span><span class="sxs-lookup"><span data-stu-id="7e7e7-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-118">-Ziel</span><span class="sxs-lookup"><span data-stu-id="7e7e7-118">-Destination</span></span>
<span data-ttu-id="7e7e7-119">Gibt den Daten See-Speicherpfad an, zu dem eine Datei oder ein Ordner hochgeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="7e7e7-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="7e7e7-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="7e7e7-121">Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="7e7e7-122">Standard ist der Fehler.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="7e7e7-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="7e7e7-124">Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7e7e7-125">-Force</span></span>
<span data-ttu-id="7e7e7-126">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="7e7e7-127">-ForceBinary</span></span>
<span data-ttu-id="7e7e7-128">Gibt an, dass dieser Vorgang die Datei als Binärdatei hochlädt.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-128">Indicates that this operation uploads the file as a binary file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-129">-Path</span><span class="sxs-lookup"><span data-stu-id="7e7e7-129">-Path</span></span>
<span data-ttu-id="7e7e7-130">Gibt den lokalen Pfad der Datei oder des Ordners an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-130">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="7e7e7-131">-PerFileThreadCount</span></span>
<span data-ttu-id="7e7e7-132">Gibt die maximale Anzahl von Threads an, die pro Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="7e7e7-133">Der Standardwert ist 10 (10).</span><span class="sxs-lookup"><span data-stu-id="7e7e7-133">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-134">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="7e7e7-134">-Recurse</span></span>
<span data-ttu-id="7e7e7-135">Gibt an, dass dieser Vorgang alle Elemente in allen Unterordnern hochladen soll.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-135">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-136">-Resume</span><span class="sxs-lookup"><span data-stu-id="7e7e7-136">-Resume</span></span>
<span data-ttu-id="7e7e7-137">Gibt an, dass dieser Vorgang einen zuvor abgebrochenen oder fehlgeschlagenen Upload wieder aufnehmen soll.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e7e7-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e7e7-138">-Confirm</span></span>
<span data-ttu-id="7e7e7-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e7e7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e7e7-140">-WhatIf</span></span>
<span data-ttu-id="7e7e7-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e7e7-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e7e7-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7e7-143">-DefaultProfile</span></span>
<span data-ttu-id="7e7e7-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e7e7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7e7-145">CommonParameters</span></span>
<span data-ttu-id="7e7e7-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7e7-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e7e7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7e7-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e7e7-148">INPUTS</span></span>

## <span data-ttu-id="7e7e7-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e7e7-149">OUTPUTS</span></span>

### <span data-ttu-id="7e7e7-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7e7e7-150">string</span></span>
<span data-ttu-id="7e7e7-151">Der vollständige Pfad im Daten Lake Store-Konto für die hochgeladene Datei oder den geuploadeten Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e7e7-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="7e7e7-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e7e7-152">NOTES</span></span>

## <span data-ttu-id="7e7e7-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e7e7-153">RELATED LINKS</span></span>

[<span data-ttu-id="7e7e7-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7e7e7-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7e7e7-156">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7e7e7-157">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7e7e7-158">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7e7e7-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7e7e7-160">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7e7e7-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


