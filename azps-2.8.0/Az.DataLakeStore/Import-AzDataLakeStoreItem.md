---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ccb538446e7cb179e15f3af17d0cde03c4ab44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651541"
---
# <span data-ttu-id="05504-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="05504-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05504-102">SYNOPSIS</span></span>
<span data-ttu-id="05504-103">Lädt eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hoch.</span><span class="sxs-lookup"><span data-stu-id="05504-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="05504-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05504-104">SYNTAX</span></span>

### <span data-ttu-id="05504-105">NoDiagnosticLogging (Standard)</span><span class="sxs-lookup"><span data-stu-id="05504-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05504-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="05504-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05504-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05504-107">DESCRIPTION</span></span>
<span data-ttu-id="05504-108">Mit dem Cmdlet " **Import-AzDataLakeStoreItem** " wird eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="05504-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="05504-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05504-109">EXAMPLES</span></span>

### <span data-ttu-id="05504-110">Beispiel 1: Hochladen einer Datei</span><span class="sxs-lookup"><span data-stu-id="05504-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="05504-111">Mit diesem Befehl wird die Datei SrcFile.csv hochgeladen und dem Ordner "meine Dateien" im Data Lake Store als File.csv mit einer Parallelität von 4 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="05504-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="05504-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="05504-112">PARAMETERS</span></span>

### <span data-ttu-id="05504-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="05504-113">-Account</span></span>
<span data-ttu-id="05504-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="05504-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="05504-115">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="05504-115">-Concurrency</span></span>
<span data-ttu-id="05504-116">Gibt die Anzahl der Dateien oder Chunks an, die parallel hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="05504-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="05504-117">Der Standardwert wird basierend auf den Systemspezifikationen als optimaler Aufwand berechnet.</span><span class="sxs-lookup"><span data-stu-id="05504-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05504-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05504-118">-DefaultProfile</span></span>
<span data-ttu-id="05504-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05504-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05504-120">-Ziel</span><span class="sxs-lookup"><span data-stu-id="05504-120">-Destination</span></span>
<span data-ttu-id="05504-121">Gibt den Daten See-Speicherpfad an, zu dem eine Datei oder ein Ordner hochgeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="05504-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="05504-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="05504-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="05504-123">Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="05504-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="05504-124">Standard ist der Fehler.</span><span class="sxs-lookup"><span data-stu-id="05504-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05504-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="05504-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="05504-126">Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="05504-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05504-127">-Force</span><span class="sxs-lookup"><span data-stu-id="05504-127">-Force</span></span>
<span data-ttu-id="05504-128">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="05504-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="05504-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="05504-129">-ForceBinary</span></span>
<span data-ttu-id="05504-130">Gibt an, dass die zu kopierenden Dateien ohne Rücksicht auf die Beibehaltung der neuen Zeile über appends kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="05504-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="05504-131">-Path</span><span class="sxs-lookup"><span data-stu-id="05504-131">-Path</span></span>
<span data-ttu-id="05504-132">Gibt den lokalen Pfad der Datei oder des Ordners an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="05504-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="05504-133">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="05504-133">-Recurse</span></span>
<span data-ttu-id="05504-134">Gibt an, dass dieser Vorgang alle Elemente in allen Unterordnern hochladen soll.</span><span class="sxs-lookup"><span data-stu-id="05504-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="05504-135">-Resume</span><span class="sxs-lookup"><span data-stu-id="05504-135">-Resume</span></span>
<span data-ttu-id="05504-136">Gibt an, dass die zu kopierenden Dateien eine Fortsetzung eines vorherigen Uploads sind.</span><span class="sxs-lookup"><span data-stu-id="05504-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="05504-137">Dies bewirkt, dass das System versucht, aus der letzten Datei, die nicht vollständig hochgeladen wurde, fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="05504-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="05504-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05504-138">-Confirm</span></span>
<span data-ttu-id="05504-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05504-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05504-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05504-140">-WhatIf</span></span>
<span data-ttu-id="05504-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05504-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05504-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05504-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05504-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05504-143">CommonParameters</span></span>
<span data-ttu-id="05504-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05504-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05504-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05504-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05504-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05504-146">INPUTS</span></span>

### <span data-ttu-id="05504-147">System. String</span><span class="sxs-lookup"><span data-stu-id="05504-147">System.String</span></span>

### <span data-ttu-id="05504-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="05504-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="05504-149">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="05504-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="05504-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="05504-150">System.Int32</span></span>

### <span data-ttu-id="05504-151">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="05504-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="05504-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05504-152">OUTPUTS</span></span>

### <span data-ttu-id="05504-153">System. String</span><span class="sxs-lookup"><span data-stu-id="05504-153">System.String</span></span>

## <span data-ttu-id="05504-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="05504-154">NOTES</span></span>

## <span data-ttu-id="05504-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05504-155">RELATED LINKS</span></span>

[<span data-ttu-id="05504-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="05504-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="05504-158">Teilnehmen – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="05504-159">Verschieben-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="05504-160">Neu – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="05504-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="05504-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05504-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


