---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458096"
---
# <span data-ttu-id="f895a-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f895a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f895a-102">SYNOPSIS</span></span>
<span data-ttu-id="f895a-103">Lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="f895a-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="f895a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f895a-104">SYNTAX</span></span>

### <span data-ttu-id="f895a-105">NoDiagnosticLogging (Standard)</span><span class="sxs-lookup"><span data-stu-id="f895a-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f895a-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="f895a-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f895a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f895a-107">DESCRIPTION</span></span>
<span data-ttu-id="f895a-108">Das **Cmdlet "Export-AzDataLakeStoreItem"** lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="f895a-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="f895a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f895a-109">EXAMPLES</span></span>

### <span data-ttu-id="f895a-110">Beispiel 1: Herunterladen eines Elements aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="f895a-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="f895a-111">Mit diesem Befehl wird die TestSource.csv aus dem Data Lake Store in C:\Test.csv mit der Parallelität 4 heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="f895a-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="f895a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f895a-112">PARAMETERS</span></span>

### <span data-ttu-id="f895a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="f895a-113">-Account</span></span>
<span data-ttu-id="f895a-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f895a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f895a-115">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="f895a-115">-Concurrency</span></span>
<span data-ttu-id="f895a-116">Gibt die Anzahl der Dateien oder Abschnitte an, die parallel heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f895a-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="f895a-117">Der Standardwert wird als beste Leistung basierend auf den Systemspezifikationen berechnet.</span><span class="sxs-lookup"><span data-stu-id="f895a-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="f895a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f895a-118">-DefaultProfile</span></span>
<span data-ttu-id="f895a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f895a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f895a-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="f895a-120">-Destination</span></span>
<span data-ttu-id="f895a-121">Gibt den lokalen Dateipfad an, in den die Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f895a-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="f895a-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="f895a-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="f895a-123">Gibt optional die Diagnoseprotokollebene an, die zum Aufzeichnen von Ereignissen während des Datei- oder Ordnerimports verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f895a-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="f895a-124">Der Standardwert ist "Fehler".</span><span class="sxs-lookup"><span data-stu-id="f895a-124">Default is Error.</span></span>

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

### <span data-ttu-id="f895a-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="f895a-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="f895a-126">Gibt den Pfad für das Diagnoseprotokoll an, auf den Ereignisse während des Datei- oder Ordnerimports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f895a-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="f895a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f895a-127">-Force</span></span>
<span data-ttu-id="f895a-128">Gibt an, dass die Zieldatei durch diesen Vorgang überschrieben werden kann, wenn sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f895a-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="f895a-129">-Path</span><span class="sxs-lookup"><span data-stu-id="f895a-129">-Path</span></span>
<span data-ttu-id="f895a-130">Gibt den Pfad des Elements an, das aus dem Data Lake Store heruntergeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="f895a-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="f895a-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="f895a-131">-Recurse</span></span>
<span data-ttu-id="f895a-132">Gibt an, dass ein Ordnerdownload rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="f895a-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="f895a-133">-Resume</span><span class="sxs-lookup"><span data-stu-id="f895a-133">-Resume</span></span>
<span data-ttu-id="f895a-134">Gibt an, dass die kopierten Dateien eine Fortsetzung eines vorherigen Downloads sind.</span><span class="sxs-lookup"><span data-stu-id="f895a-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="f895a-135">Dies verursacht, dass das System versucht, aus der letzten Datei, die nicht vollständig heruntergeladen wurde, fortgesetzt zu werden.</span><span class="sxs-lookup"><span data-stu-id="f895a-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="f895a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f895a-136">-Confirm</span></span>
<span data-ttu-id="f895a-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f895a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f895a-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f895a-138">-WhatIf</span></span>
<span data-ttu-id="f895a-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f895a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f895a-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f895a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f895a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f895a-141">CommonParameters</span></span>
<span data-ttu-id="f895a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f895a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f895a-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f895a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f895a-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f895a-144">INPUTS</span></span>

### <span data-ttu-id="f895a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f895a-145">System.String</span></span>

### <span data-ttu-id="f895a-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f895a-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f895a-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f895a-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f895a-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f895a-148">System.Int32</span></span>

### <span data-ttu-id="f895a-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="f895a-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="f895a-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f895a-150">OUTPUTS</span></span>

### <span data-ttu-id="f895a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f895a-151">System.String</span></span>

## <span data-ttu-id="f895a-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f895a-152">NOTES</span></span>

## <span data-ttu-id="f895a-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f895a-153">RELATED LINKS</span></span>

[<span data-ttu-id="f895a-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="f895a-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f895a-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="f895a-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="f895a-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f895a-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f895a-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f895a-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


