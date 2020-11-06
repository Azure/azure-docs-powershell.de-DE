---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 91e7969600f387a95f46cad02f87cf6466f2c642
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480334"
---
# <span data-ttu-id="fc4be-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="fc4be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc4be-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4be-103">Lädt eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hoch.</span><span class="sxs-lookup"><span data-stu-id="fc4be-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc4be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc4be-104">SYNTAX</span></span>

### <span data-ttu-id="fc4be-105">NoDiagnosticLogging (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc4be-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4be-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="fc4be-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc4be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc4be-107">DESCRIPTION</span></span>
<span data-ttu-id="fc4be-108">Mit dem Cmdlet " **Import-AzureRmDataLakeStoreItem** " wird eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="fc4be-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="fc4be-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc4be-109">EXAMPLES</span></span>

### <span data-ttu-id="fc4be-110">Beispiel 1: Hochladen einer Datei</span><span class="sxs-lookup"><span data-stu-id="fc4be-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="fc4be-111">Mit diesem Befehl wird die Datei SrcFile.csv hochgeladen und dem Ordner "meine Dateien" im Data Lake Store als File.csv mit einer Parallelität von 4 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fc4be-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="fc4be-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc4be-112">PARAMETERS</span></span>

### <span data-ttu-id="fc4be-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="fc4be-113">-Account</span></span>
<span data-ttu-id="fc4be-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="fc4be-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fc4be-115">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="fc4be-115">-Concurrency</span></span>
<span data-ttu-id="fc4be-116">Gibt die Anzahl der Dateien oder Chunks an, die parallel hochgeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc4be-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="fc4be-117">Der Standardwert wird basierend auf den Systemspezifikationen als optimaler Aufwand berechnet.</span><span class="sxs-lookup"><span data-stu-id="fc4be-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="fc4be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4be-118">-DefaultProfile</span></span>
<span data-ttu-id="fc4be-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc4be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc4be-120">-Ziel</span><span class="sxs-lookup"><span data-stu-id="fc4be-120">-Destination</span></span>
<span data-ttu-id="fc4be-121">Gibt den Daten See-Speicherpfad an, zu dem eine Datei oder ein Ordner hochgeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="fc4be-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fc4be-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="fc4be-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="fc4be-123">Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc4be-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="fc4be-124">Standard ist der Fehler.</span><span class="sxs-lookup"><span data-stu-id="fc4be-124">Default is Error.</span></span>

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

### <span data-ttu-id="fc4be-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="fc4be-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="fc4be-126">Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="fc4be-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="fc4be-127">-Force</span><span class="sxs-lookup"><span data-stu-id="fc4be-127">-Force</span></span>
<span data-ttu-id="fc4be-128">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fc4be-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="fc4be-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="fc4be-129">-ForceBinary</span></span>
<span data-ttu-id="fc4be-130">Gibt an, dass die zu kopierenden Dateien ohne Rücksicht auf die Beibehaltung der neuen Zeile über appends kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc4be-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="fc4be-131">-Path</span><span class="sxs-lookup"><span data-stu-id="fc4be-131">-Path</span></span>
<span data-ttu-id="fc4be-132">Gibt den lokalen Pfad der Datei oder des Ordners an, die hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc4be-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="fc4be-133">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="fc4be-133">-Recurse</span></span>
<span data-ttu-id="fc4be-134">Gibt an, dass dieser Vorgang alle Elemente in allen Unterordnern hochladen soll.</span><span class="sxs-lookup"><span data-stu-id="fc4be-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="fc4be-135">-Resume</span><span class="sxs-lookup"><span data-stu-id="fc4be-135">-Resume</span></span>
<span data-ttu-id="fc4be-136">Gibt an, dass die zu kopierenden Dateien eine Fortsetzung eines vorherigen Uploads sind.</span><span class="sxs-lookup"><span data-stu-id="fc4be-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="fc4be-137">Dies bewirkt, dass das System versucht, aus der letzten Datei, die nicht vollständig hochgeladen wurde, fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="fc4be-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="fc4be-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc4be-138">-Confirm</span></span>
<span data-ttu-id="fc4be-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc4be-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4be-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4be-140">-WhatIf</span></span>
<span data-ttu-id="fc4be-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc4be-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4be-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc4be-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4be-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4be-143">CommonParameters</span></span>
<span data-ttu-id="fc4be-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4be-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4be-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc4be-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4be-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc4be-146">INPUTS</span></span>

### <span data-ttu-id="fc4be-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fc4be-147">System.String</span></span>

### <span data-ttu-id="fc4be-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fc4be-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fc4be-149">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fc4be-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fc4be-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fc4be-150">System.Int32</span></span>

### <span data-ttu-id="fc4be-151">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="fc4be-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="fc4be-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc4be-152">OUTPUTS</span></span>

### <span data-ttu-id="fc4be-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fc4be-153">System.String</span></span>
<span data-ttu-id="fc4be-154">Der vollständige Pfad im Daten Lake Store-Konto für die hochgeladene Datei oder den geuploadeten Ordner.</span><span class="sxs-lookup"><span data-stu-id="fc4be-154">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="fc4be-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc4be-155">NOTES</span></span>

## <span data-ttu-id="fc4be-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc4be-156">RELATED LINKS</span></span>

[<span data-ttu-id="fc4be-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc4be-158">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc4be-159">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-159">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc4be-160">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-160">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc4be-161">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-161">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc4be-162">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-162">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc4be-163">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc4be-163">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


