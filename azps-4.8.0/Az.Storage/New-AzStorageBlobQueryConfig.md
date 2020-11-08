---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174004"
---
# <span data-ttu-id="3e62b-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="3e62b-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="3e62b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e62b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e62b-103">Erstellt ein BLOB Query Configuration-Objekt, das in Get-AzStorageBlobQueryResult verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3e62b-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="3e62b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e62b-104">SYNTAX</span></span>

### <span data-ttu-id="3e62b-105">CSV (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e62b-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="3e62b-106">JSON</span><span class="sxs-lookup"><span data-stu-id="3e62b-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="3e62b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e62b-107">DESCRIPTION</span></span>
<span data-ttu-id="3e62b-108">Das Cmdlet **New-AzStorageBlobQueryConfig** erstellt ein BLOB Query Configuration-Objekt, das in Get-AzStorageBlobQueryResult verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3e62b-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="3e62b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e62b-109">EXAMPLES</span></span>

### <span data-ttu-id="3e62b-110">Beispiel 1: Erstellen einer BLOB-Abfrage konfiguriert und Abfragen eines BLOB</span><span class="sxs-lookup"><span data-stu-id="3e62b-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="3e62b-111">Mit diesem Befehl können Sie zunächst das Eingabe Konfigurationsobjekt als CSV-Datei und das Ausgabe Konfigurationsobjekt als JSON erstellen und dann die beiden Konfigurationen verwenden, um BLOB abzufragen.</span><span class="sxs-lookup"><span data-stu-id="3e62b-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="3e62b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e62b-112">PARAMETERS</span></span>

### <span data-ttu-id="3e62b-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="3e62b-113">-AsCsv</span></span>
<span data-ttu-id="3e62b-114">Geben Sie an, dass eine BLOB-Abfrage Konfiguration für CSV erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e62b-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e62b-115">-AsJob</span></span>
<span data-ttu-id="3e62b-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3e62b-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-117">-JSON</span><span class="sxs-lookup"><span data-stu-id="3e62b-117">-AsJson</span></span>
<span data-ttu-id="3e62b-118">Geben Sie an, dass eine BLOB-Abfrage Konfiguration für JSON erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e62b-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="3e62b-119">-ColumnSeparator</span></span>
<span data-ttu-id="3e62b-120">Optional.</span><span class="sxs-lookup"><span data-stu-id="3e62b-120">Optional.</span></span>
<span data-ttu-id="3e62b-121">Die zum Trennen von Spalten verwendete Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3e62b-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="3e62b-122">-EscapeCharacter</span></span>
<span data-ttu-id="3e62b-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="3e62b-123">Optional.</span></span>
<span data-ttu-id="3e62b-124">Das als Escapezeichen verwendete Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3e62b-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="3e62b-125">-HasHeader</span></span>
<span data-ttu-id="3e62b-126">Optional.</span><span class="sxs-lookup"><span data-stu-id="3e62b-126">Optional.</span></span>
<span data-ttu-id="3e62b-127">Geben Sie an, dass die Daten Überschriften aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3e62b-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="3e62b-128">-QuotationCharacter</span></span>
<span data-ttu-id="3e62b-129">Optional.</span><span class="sxs-lookup"><span data-stu-id="3e62b-129">Optional.</span></span>
<span data-ttu-id="3e62b-130">Das Zeichen, das zum Zitieren eines bestimmten Felds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e62b-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="3e62b-131">-RecordSeparator</span></span>
<span data-ttu-id="3e62b-132">Optional.</span><span class="sxs-lookup"><span data-stu-id="3e62b-132">Optional.</span></span>
<span data-ttu-id="3e62b-133">Die Zeichenfolge, mit der Datensätze getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="3e62b-133">The string used to separate records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e62b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e62b-134">CommonParameters</span></span>
<span data-ttu-id="3e62b-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e62b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e62b-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e62b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e62b-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e62b-137">INPUTS</span></span>

### <span data-ttu-id="3e62b-138">Keine</span><span class="sxs-lookup"><span data-stu-id="3e62b-138">None</span></span>

## <span data-ttu-id="3e62b-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e62b-139">OUTPUTS</span></span>

### <span data-ttu-id="3e62b-140">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e62b-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="3e62b-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e62b-141">NOTES</span></span>

## <span data-ttu-id="3e62b-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e62b-142">RELATED LINKS</span></span>
