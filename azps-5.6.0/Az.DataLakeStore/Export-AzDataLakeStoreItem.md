---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 72fcb1ecd78b2682fe678af8b75b36032ff58b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921267"
---
# <span data-ttu-id="03e61-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="03e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e61-102">SYNOPSIS</span></span>
<span data-ttu-id="03e61-103">Lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="03e61-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="03e61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03e61-104">SYNTAX</span></span>

### <span data-ttu-id="03e61-105">NoDiagnosticLogging (Standard)</span><span class="sxs-lookup"><span data-stu-id="03e61-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03e61-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="03e61-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03e61-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03e61-107">DESCRIPTION</span></span>
<span data-ttu-id="03e61-108">Das **Cmdlet Export-AzDataLakeStoreItem** lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="03e61-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="03e61-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03e61-109">EXAMPLES</span></span>

### <span data-ttu-id="03e61-110">Beispiel 1: Herunterladen eines Elements aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="03e61-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="03e61-111">Dieser Befehl lädt die Datei aus TestSource.csv Data Lake Store herunter, um C:\Test.csv parallel zu 4 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="03e61-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="03e61-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="03e61-112">PARAMETERS</span></span>

### <span data-ttu-id="03e61-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="03e61-113">-Account</span></span>
<span data-ttu-id="03e61-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="03e61-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="03e61-115">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="03e61-115">-Concurrency</span></span>
<span data-ttu-id="03e61-116">Gibt die Anzahl der Dateien oder Abschnitte an, die parallel heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="03e61-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="03e61-117">Der Standardwert wird als optimaler Aufwand basierend auf Systemspezifikationen berechnet.</span><span class="sxs-lookup"><span data-stu-id="03e61-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="03e61-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e61-118">-DefaultProfile</span></span>
<span data-ttu-id="03e61-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03e61-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e61-120">-Ziel</span><span class="sxs-lookup"><span data-stu-id="03e61-120">-Destination</span></span>
<span data-ttu-id="03e61-121">Gibt den lokalen Dateipfad an, in den die Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="03e61-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="03e61-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="03e61-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="03e61-123">Gibt optional die Diagnoseprotokollebene an, die zum Aufzeichnen von Ereignissen während des Datei- oder Ordnerimports verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="03e61-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="03e61-124">Standard ist Fehler.</span><span class="sxs-lookup"><span data-stu-id="03e61-124">Default is Error.</span></span>

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

### <span data-ttu-id="03e61-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="03e61-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="03e61-126">Gibt den Pfad für das Diagnoseprotokoll zum Aufzeichnen von Ereignissen während des Datei- oder Ordnerimports an.</span><span class="sxs-lookup"><span data-stu-id="03e61-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="03e61-127">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="03e61-127">-Force</span></span>
<span data-ttu-id="03e61-128">Gibt an, dass die Zieldatei durch diesen Vorgang überschrieben werden kann, wenn sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="03e61-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="03e61-129">-Path</span><span class="sxs-lookup"><span data-stu-id="03e61-129">-Path</span></span>
<span data-ttu-id="03e61-130">Gibt den Pfad des Elements an, das aus dem Data Lake Store heruntergeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="03e61-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="03e61-131">-Rekursieren</span><span class="sxs-lookup"><span data-stu-id="03e61-131">-Recurse</span></span>
<span data-ttu-id="03e61-132">Gibt an, dass ein Ordnerdownload rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="03e61-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="03e61-133">-Lebenslauf</span><span class="sxs-lookup"><span data-stu-id="03e61-133">-Resume</span></span>
<span data-ttu-id="03e61-134">Gibt an, dass die kopierten Dateien eine Fortsetzung eines vorherigen Downloads sind.</span><span class="sxs-lookup"><span data-stu-id="03e61-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="03e61-135">Dies hat zur Ursache, dass das System versucht, aus der letzten Datei, die nicht vollständig heruntergeladen wurde, die Fortsetzung zu versuchen.</span><span class="sxs-lookup"><span data-stu-id="03e61-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="03e61-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03e61-136">-Confirm</span></span>
<span data-ttu-id="03e61-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03e61-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e61-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e61-138">-WhatIf</span></span>
<span data-ttu-id="03e61-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03e61-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e61-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03e61-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e61-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e61-141">CommonParameters</span></span>
<span data-ttu-id="03e61-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03e61-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e61-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e61-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e61-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03e61-144">INPUTS</span></span>

### <span data-ttu-id="03e61-145">System.String</span><span class="sxs-lookup"><span data-stu-id="03e61-145">System.String</span></span>

### <span data-ttu-id="03e61-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="03e61-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="03e61-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="03e61-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="03e61-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="03e61-148">System.Int32</span></span>

### <span data-ttu-id="03e61-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="03e61-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="03e61-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03e61-150">OUTPUTS</span></span>

### <span data-ttu-id="03e61-151">System.String</span><span class="sxs-lookup"><span data-stu-id="03e61-151">System.String</span></span>

## <span data-ttu-id="03e61-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="03e61-152">NOTES</span></span>

## <span data-ttu-id="03e61-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="03e61-153">RELATED LINKS</span></span>

[<span data-ttu-id="03e61-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="03e61-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="03e61-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="03e61-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="03e61-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="03e61-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="03e61-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03e61-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


