---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501906"
---
# <span data-ttu-id="b04f6-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b04f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b04f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b04f6-103">Lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="b04f6-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b04f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b04f6-104">SYNTAX</span></span>

### <span data-ttu-id="b04f6-105">Keine Diagnoseprotokollierung (Standard)</span><span class="sxs-lookup"><span data-stu-id="b04f6-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04f6-106">Einbeziehen der Diagnoseprotokollierung</span><span class="sxs-lookup"><span data-stu-id="b04f6-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b04f6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b04f6-107">DESCRIPTION</span></span>
<span data-ttu-id="b04f6-108">Das Cmdlet " **Export-AzureRmDataLakeStoreItem** " lädt eine Datei aus dem Data Lake Store herunter.</span><span class="sxs-lookup"><span data-stu-id="b04f6-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="b04f6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b04f6-109">EXAMPLES</span></span>

### <span data-ttu-id="b04f6-110">Beispiel 1: Herunterladen eines Elements aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="b04f6-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="b04f6-111">Dieser Befehl downloadet die Datei TestSource.csv aus dem Data Lake Store in C:\Test.csv.</span><span class="sxs-lookup"><span data-stu-id="b04f6-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="b04f6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b04f6-112">PARAMETERS</span></span>

### <span data-ttu-id="b04f6-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="b04f6-113">-Account</span></span>
<span data-ttu-id="b04f6-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b04f6-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b04f6-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="b04f6-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="b04f6-116">Gibt die maximale Anzahl von Dateien an, die für einen Ordner Download parallel heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b04f6-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="b04f6-117">Der Standardwert ist Five (5).</span><span class="sxs-lookup"><span data-stu-id="b04f6-117">The default value is five (5).</span></span>

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

### <span data-ttu-id="b04f6-118">-Ziel</span><span class="sxs-lookup"><span data-stu-id="b04f6-118">-Destination</span></span>
<span data-ttu-id="b04f6-119">Gibt den lokalen Dateipfad an, zu dem die Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b04f6-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="b04f6-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="b04f6-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="b04f6-121">Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b04f6-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="b04f6-122">Standard ist der Fehler.</span><span class="sxs-lookup"><span data-stu-id="b04f6-122">Default is Error.</span></span>

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

### <span data-ttu-id="b04f6-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="b04f6-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="b04f6-124">Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b04f6-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="b04f6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b04f6-125">-Force</span></span>
<span data-ttu-id="b04f6-126">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b04f6-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="b04f6-127">-Path</span><span class="sxs-lookup"><span data-stu-id="b04f6-127">-Path</span></span>
<span data-ttu-id="b04f6-128">Gibt den Pfad des Elements an, das vom Data Lake Store heruntergeladen werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="b04f6-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="b04f6-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="b04f6-129">-PerFileThreadCount</span></span>
<span data-ttu-id="b04f6-130">Gibt die maximale Anzahl von Threads an, die pro Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b04f6-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="b04f6-131">Der Standardwert ist 10 (10).</span><span class="sxs-lookup"><span data-stu-id="b04f6-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04f6-132">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="b04f6-132">-Recurse</span></span>
<span data-ttu-id="b04f6-133">Gibt an, dass ein Ordner Download rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="b04f6-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="b04f6-134">-Resume</span><span class="sxs-lookup"><span data-stu-id="b04f6-134">-Resume</span></span>
<span data-ttu-id="b04f6-135">Gibt an, dass die zu kopierenden Dateien eine Fortsetzung eines vorherigen Downloads sind.</span><span class="sxs-lookup"><span data-stu-id="b04f6-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="b04f6-136">Der Download versucht, aus der letzten Datei, die nicht vollständig heruntergeladen wurde, fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="b04f6-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="b04f6-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b04f6-137">-Confirm</span></span>
<span data-ttu-id="b04f6-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b04f6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04f6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04f6-139">-WhatIf</span></span>
<span data-ttu-id="b04f6-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b04f6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b04f6-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b04f6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04f6-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04f6-142">-DefaultProfile</span></span>
<span data-ttu-id="b04f6-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b04f6-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b04f6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04f6-144">CommonParameters</span></span>
<span data-ttu-id="b04f6-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04f6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04f6-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04f6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04f6-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b04f6-147">INPUTS</span></span>

## <span data-ttu-id="b04f6-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b04f6-148">OUTPUTS</span></span>

### <span data-ttu-id="b04f6-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b04f6-149">string</span></span>
<span data-ttu-id="b04f6-150">Der Pfad, in den die Datei oder der Ordner heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b04f6-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="b04f6-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="b04f6-151">NOTES</span></span>

## <span data-ttu-id="b04f6-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b04f6-152">RELATED LINKS</span></span>

[<span data-ttu-id="b04f6-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b04f6-154">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b04f6-155">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b04f6-156">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b04f6-157">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b04f6-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b04f6-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b04f6-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


