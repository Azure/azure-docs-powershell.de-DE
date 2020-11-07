---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662580"
---
# <span data-ttu-id="ecfdd-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="ecfdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfdd-103">Lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecfdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecfdd-104">SYNTAX</span></span>

### <span data-ttu-id="ecfdd-105">NoDiagnosticLogging (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecfdd-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfdd-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="ecfdd-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecfdd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecfdd-107">DESCRIPTION</span></span>
<span data-ttu-id="ecfdd-108">Das Cmdlet " **Export-AzureRmDataLakeStoreItem** " lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="ecfdd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecfdd-109">EXAMPLES</span></span>

### <span data-ttu-id="ecfdd-110">Beispiel 1: Herunterladen eines Elements aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ecfdd-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="ecfdd-111">Dieser Befehl downloadet die Datei TestSource.csv aus dem Data Lake Store in C:\Test.csv mit einer Parallelität von 4.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="ecfdd-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecfdd-112">PARAMETERS</span></span>

### <span data-ttu-id="ecfdd-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="ecfdd-113">-Account</span></span>
<span data-ttu-id="ecfdd-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ecfdd-115">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="ecfdd-115">-Concurrency</span></span>
<span data-ttu-id="ecfdd-116">Gibt die Anzahl der Dateien oder Chunks an, die parallel heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="ecfdd-117">Der Standardwert wird basierend auf den Systemspezifikationen als optimaler Aufwand berechnet.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfdd-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="ecfdd-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="ecfdd-119">Gibt die maximale Anzahl von Dateien an, die für einen Ordner Download parallel heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="ecfdd-120">Der Standardwert wird als optimaler Aufwand basierend auf Ordner-und Dateigröße berechnet.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-120">Default will be computed as a best effort based on folder and file size</span></span>

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

### <span data-ttu-id="ecfdd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfdd-121">-DefaultProfile</span></span>
<span data-ttu-id="ecfdd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecfdd-123">-Ziel</span><span class="sxs-lookup"><span data-stu-id="ecfdd-123">-Destination</span></span>
<span data-ttu-id="ecfdd-124">Gibt den lokalen Dateipfad an, zu dem die Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-124">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="ecfdd-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="ecfdd-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="ecfdd-126">Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="ecfdd-127">Standard ist der Fehler.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-127">Default is Error.</span></span>

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

### <span data-ttu-id="ecfdd-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="ecfdd-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="ecfdd-129">Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="ecfdd-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ecfdd-130">-Force</span></span>
<span data-ttu-id="ecfdd-131">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfdd-132">-Path</span><span class="sxs-lookup"><span data-stu-id="ecfdd-132">-Path</span></span>
<span data-ttu-id="ecfdd-133">Gibt den Pfad des Elements an, das vom Data Lake Store heruntergeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="ecfdd-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfdd-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="ecfdd-134">-PerFileThreadCount</span></span>
<span data-ttu-id="ecfdd-135">Gibt die maximale Anzahl von Threads an, die pro Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="ecfdd-136">Der Standardwert wird als optimaler Aufwand basierend auf Ordner-und Dateigröße berechnet.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfdd-137">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="ecfdd-137">-Recurse</span></span>
<span data-ttu-id="ecfdd-138">Gibt an, dass ein Ordner Download rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-138">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="ecfdd-139">-Resume</span><span class="sxs-lookup"><span data-stu-id="ecfdd-139">-Resume</span></span>
<span data-ttu-id="ecfdd-140">Gibt an, dass die zu kopierenden Dateien eine Fortsetzung eines vorherigen Downloads sind.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="ecfdd-141">Dies bewirkt, dass das System versucht, aus der letzten Datei, die nicht vollständig heruntergeladen wurde, fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="ecfdd-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecfdd-142">-Confirm</span></span>
<span data-ttu-id="ecfdd-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfdd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecfdd-144">-WhatIf</span></span>
<span data-ttu-id="ecfdd-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecfdd-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfdd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfdd-147">CommonParameters</span></span>
<span data-ttu-id="ecfdd-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfdd-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfdd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfdd-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecfdd-150">INPUTS</span></span>

### <span data-ttu-id="ecfdd-151">Keine</span><span class="sxs-lookup"><span data-stu-id="ecfdd-151">None</span></span>
<span data-ttu-id="ecfdd-152">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ecfdd-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecfdd-153">OUTPUTS</span></span>

### <span data-ttu-id="ecfdd-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ecfdd-154">string</span></span>
<span data-ttu-id="ecfdd-155">Der Pfad, in den die Datei oder der Ordner heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="ecfdd-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="ecfdd-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecfdd-156">NOTES</span></span>

## <span data-ttu-id="ecfdd-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecfdd-157">RELATED LINKS</span></span>

[<span data-ttu-id="ecfdd-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ecfdd-159">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ecfdd-160">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ecfdd-161">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ecfdd-162">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ecfdd-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ecfdd-164">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ecfdd-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


