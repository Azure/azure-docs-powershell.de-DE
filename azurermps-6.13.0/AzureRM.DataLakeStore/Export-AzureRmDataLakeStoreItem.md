---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 508a7619374b7e245b8df99c929f161ce1966288
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499566"
---
# <span data-ttu-id="5cc6a-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5cc6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc6a-103">Lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cc6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cc6a-104">SYNTAX</span></span>

### <span data-ttu-id="5cc6a-105">NoDiagnosticLogging (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cc6a-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cc6a-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="5cc6a-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cc6a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc6a-107">DESCRIPTION</span></span>
<span data-ttu-id="5cc6a-108">Das Cmdlet " **Export-AzureRmDataLakeStoreItem** " lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="5cc6a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cc6a-109">EXAMPLES</span></span>

### <span data-ttu-id="5cc6a-110">Beispiel 1: Herunterladen eines Elements aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5cc6a-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="5cc6a-111">Dieser Befehl downloadet die Datei TestSource.csv aus dem Data Lake Store in C:\Test.csv mit einer Parallelität von 4.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="5cc6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cc6a-112">PARAMETERS</span></span>

### <span data-ttu-id="5cc6a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="5cc6a-113">-Account</span></span>
<span data-ttu-id="5cc6a-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5cc6a-115">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="5cc6a-115">-Concurrency</span></span>
<span data-ttu-id="5cc6a-116">Gibt die Anzahl der Dateien oder Chunks an, die parallel heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="5cc6a-117">Der Standardwert wird basierend auf den Systemspezifikationen als optimaler Aufwand berechnet.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="5cc6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc6a-118">-DefaultProfile</span></span>
<span data-ttu-id="5cc6a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cc6a-120">-Ziel</span><span class="sxs-lookup"><span data-stu-id="5cc6a-120">-Destination</span></span>
<span data-ttu-id="5cc6a-121">Gibt den lokalen Dateipfad an, zu dem die Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="5cc6a-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="5cc6a-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="5cc6a-123">Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="5cc6a-124">Standard ist der Fehler.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-124">Default is Error.</span></span>

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

### <span data-ttu-id="5cc6a-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="5cc6a-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="5cc6a-126">Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="5cc6a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5cc6a-127">-Force</span></span>
<span data-ttu-id="5cc6a-128">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc6a-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5cc6a-129">-Path</span></span>
<span data-ttu-id="5cc6a-130">Gibt den Pfad des Elements an, das vom Data Lake Store heruntergeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="5cc6a-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cc6a-131">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="5cc6a-131">-Recurse</span></span>
<span data-ttu-id="5cc6a-132">Gibt an, dass ein Ordner Download rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="5cc6a-133">-Resume</span><span class="sxs-lookup"><span data-stu-id="5cc6a-133">-Resume</span></span>
<span data-ttu-id="5cc6a-134">Gibt an, dass die zu kopierenden Dateien eine Fortsetzung eines vorherigen Downloads sind.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="5cc6a-135">Dies bewirkt, dass das System versucht, aus der letzten Datei, die nicht vollständig heruntergeladen wurde, fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="5cc6a-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cc6a-136">-Confirm</span></span>
<span data-ttu-id="5cc6a-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc6a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc6a-138">-WhatIf</span></span>
<span data-ttu-id="5cc6a-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc6a-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc6a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc6a-141">CommonParameters</span></span>
<span data-ttu-id="5cc6a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc6a-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc6a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc6a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cc6a-144">INPUTS</span></span>

### <span data-ttu-id="5cc6a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5cc6a-145">System.String</span></span>

### <span data-ttu-id="5cc6a-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5cc6a-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5cc6a-147">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5cc6a-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5cc6a-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5cc6a-148">System.Int32</span></span>

### <span data-ttu-id="5cc6a-149">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="5cc6a-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="5cc6a-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cc6a-150">OUTPUTS</span></span>

### <span data-ttu-id="5cc6a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5cc6a-151">System.String</span></span>
<span data-ttu-id="5cc6a-152">Der Pfad, in den die Datei oder der Ordner heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="5cc6a-152">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="5cc6a-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cc6a-153">NOTES</span></span>

## <span data-ttu-id="5cc6a-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cc6a-154">RELATED LINKS</span></span>

[<span data-ttu-id="5cc6a-155">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-155">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5cc6a-156">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5cc6a-157">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-157">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5cc6a-158">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-158">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5cc6a-159">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-159">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5cc6a-160">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-160">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5cc6a-161">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5cc6a-161">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


