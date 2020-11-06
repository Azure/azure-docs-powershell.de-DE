---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499873"
---
# <span data-ttu-id="b60cb-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b60cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b60cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b60cb-103">Lädt eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hoch.</span><span class="sxs-lookup"><span data-stu-id="b60cb-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b60cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b60cb-104">SYNTAX</span></span>

### <span data-ttu-id="b60cb-105">NoDiagnosticLogging (Standard)</span><span class="sxs-lookup"><span data-stu-id="b60cb-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b60cb-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="b60cb-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60cb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b60cb-107">DESCRIPTION</span></span>
<span data-ttu-id="b60cb-108">Mit dem Cmdlet " **Import-AzureRmDataLakeStoreItem** " wird eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="b60cb-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="b60cb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b60cb-109">EXAMPLES</span></span>

### <span data-ttu-id="b60cb-110">Beispiel 1: Hochladen einer Datei</span><span class="sxs-lookup"><span data-stu-id="b60cb-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="b60cb-111">Mit diesem Befehl wird die Datei SrcFile.csv hochgeladen und dem Ordner "meine Dateien" im Data Lake Store als File.csv mit einer Parallelität von 4 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b60cb-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="b60cb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b60cb-112">PARAMETERS</span></span>

### <span data-ttu-id="b60cb-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="b60cb-113">-Account</span></span>
<span data-ttu-id="b60cb-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b60cb-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-115">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="b60cb-115">-Concurrency</span></span>
<span data-ttu-id="b60cb-116">Gibt die Anzahl der Dateien oder Chunks an, die parallel hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b60cb-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="b60cb-117">Der Standardwert wird basierend auf den Systemspezifikationen als optimaler Aufwand berechnet.</span><span class="sxs-lookup"><span data-stu-id="b60cb-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="b60cb-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="b60cb-119">Gibt die maximale Anzahl von Dateien an, die parallel für einen Ordner Upload hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b60cb-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="b60cb-120">Der Standardwert wird als optimaler Aufwand basierend auf Ordner-und Dateigröße berechnet.</span><span class="sxs-lookup"><span data-stu-id="b60cb-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60cb-121">-DefaultProfile</span></span>
<span data-ttu-id="b60cb-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b60cb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60cb-123">-Ziel</span><span class="sxs-lookup"><span data-stu-id="b60cb-123">-Destination</span></span>
<span data-ttu-id="b60cb-124">Gibt den Daten See-Speicherpfad an, zu dem eine Datei oder ein Ordner hochgeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="b60cb-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="b60cb-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="b60cb-126">Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b60cb-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="b60cb-127">Standard ist der Fehler.</span><span class="sxs-lookup"><span data-stu-id="b60cb-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="b60cb-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="b60cb-129">Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b60cb-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b60cb-130">-Force</span></span>
<span data-ttu-id="b60cb-131">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b60cb-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="b60cb-132">-ForceBinary</span></span>
<span data-ttu-id="b60cb-133">Gibt an, dass die zu kopierenden Dateien ohne Rücksicht auf die Beibehaltung der neuen Zeile über appends kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b60cb-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-134">-Path</span><span class="sxs-lookup"><span data-stu-id="b60cb-134">-Path</span></span>
<span data-ttu-id="b60cb-135">Gibt den lokalen Pfad der Datei oder des Ordners an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b60cb-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="b60cb-136">-PerFileThreadCount</span></span>
<span data-ttu-id="b60cb-137">Gibt die maximale Anzahl von Threads an, die pro Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b60cb-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="b60cb-138">Der Standardwert wird als optimaler Aufwand basierend auf Ordner-und Dateigröße berechnet.</span><span class="sxs-lookup"><span data-stu-id="b60cb-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-139">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="b60cb-139">-Recurse</span></span>
<span data-ttu-id="b60cb-140">Gibt an, dass dieser Vorgang alle Elemente in allen Unterordnern hochladen soll.</span><span class="sxs-lookup"><span data-stu-id="b60cb-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-141">-Resume</span><span class="sxs-lookup"><span data-stu-id="b60cb-141">-Resume</span></span>
<span data-ttu-id="b60cb-142">Gibt an, dass die zu kopierenden Dateien eine Fortsetzung eines vorherigen Uploads sind.</span><span class="sxs-lookup"><span data-stu-id="b60cb-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="b60cb-143">Dies bewirkt, dass das System versucht, aus der letzten Datei, die nicht vollständig hochgeladen wurde, fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="b60cb-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b60cb-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b60cb-144">-Confirm</span></span>
<span data-ttu-id="b60cb-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b60cb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60cb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60cb-146">-WhatIf</span></span>
<span data-ttu-id="b60cb-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b60cb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b60cb-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b60cb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60cb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60cb-149">CommonParameters</span></span>
<span data-ttu-id="b60cb-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60cb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60cb-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60cb-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60cb-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b60cb-152">INPUTS</span></span>

### <span data-ttu-id="b60cb-153">Keine</span><span class="sxs-lookup"><span data-stu-id="b60cb-153">None</span></span>
<span data-ttu-id="b60cb-154">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b60cb-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b60cb-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b60cb-155">OUTPUTS</span></span>

### <span data-ttu-id="b60cb-156">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b60cb-156">string</span></span>
<span data-ttu-id="b60cb-157">Der vollständige Pfad im Daten Lake Store-Konto für die hochgeladene Datei oder den geuploadeten Ordner.</span><span class="sxs-lookup"><span data-stu-id="b60cb-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="b60cb-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="b60cb-158">NOTES</span></span>

## <span data-ttu-id="b60cb-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b60cb-159">RELATED LINKS</span></span>

[<span data-ttu-id="b60cb-160">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60cb-161">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60cb-162">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60cb-163">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60cb-164">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60cb-165">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b60cb-166">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b60cb-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


