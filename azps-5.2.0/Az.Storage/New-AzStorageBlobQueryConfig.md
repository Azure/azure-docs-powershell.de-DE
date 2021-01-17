---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304120"
---
# <span data-ttu-id="176dc-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="176dc-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="176dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176dc-102">SYNOPSIS</span></span>
<span data-ttu-id="176dc-103">Erstellt ein Blob Query-Konfigurationsobjekt, das in Get-AzStorageBlobQueryResult verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="176dc-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="176dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="176dc-104">SYNTAX</span></span>

### <span data-ttu-id="176dc-105">CSV (Standard)</span><span class="sxs-lookup"><span data-stu-id="176dc-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="176dc-106">Json</span><span class="sxs-lookup"><span data-stu-id="176dc-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="176dc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="176dc-107">DESCRIPTION</span></span>
<span data-ttu-id="176dc-108">Das **Cmdlet "New-AzStorageBlobQueryConfig"** erstellt ein BLOB-Abfrage-Konfigurationsobjekt, das in Get-AzStorageBlobQueryResult verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="176dc-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="176dc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="176dc-109">EXAMPLES</span></span>

### <span data-ttu-id="176dc-110">Beispiel 1: Erstellen von Konfigurieren von BLOB-Abfragen und Abfragen eines BLOB</span><span class="sxs-lookup"><span data-stu-id="176dc-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="176dc-111">Dieser Befehl erstellt zuerst das Eingabekonfigurationsobjekt als CSV und das Ausgabekonfigurationsobjekt als JSON und verwendet dann die beiden Konfigurationen zum Abfragen des BLOB.</span><span class="sxs-lookup"><span data-stu-id="176dc-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="176dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176dc-112">PARAMETERS</span></span>

### <span data-ttu-id="176dc-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="176dc-113">-AsCsv</span></span>
<span data-ttu-id="176dc-114">Angeben, dass eine Blob Query-Konfiguration für CSV erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="176dc-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="176dc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="176dc-115">-AsJob</span></span>
<span data-ttu-id="176dc-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="176dc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="176dc-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="176dc-117">-AsJson</span></span>
<span data-ttu-id="176dc-118">Geben Sie an, dass eine Blob Query Configuration für Json erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="176dc-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="176dc-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="176dc-119">-ColumnSeparator</span></span>
<span data-ttu-id="176dc-120">Optional.</span><span class="sxs-lookup"><span data-stu-id="176dc-120">Optional.</span></span>
<span data-ttu-id="176dc-121">Die Zeichenfolge, die zum Trennen von Spalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="176dc-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="176dc-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="176dc-122">-EscapeCharacter</span></span>
<span data-ttu-id="176dc-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="176dc-123">Optional.</span></span>
<span data-ttu-id="176dc-124">Das Zeichen, das als Escapezeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="176dc-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="176dc-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="176dc-125">-HasHeader</span></span>
<span data-ttu-id="176dc-126">Optional.</span><span class="sxs-lookup"><span data-stu-id="176dc-126">Optional.</span></span>
<span data-ttu-id="176dc-127">Angeben, dass die Daten Überschriften haben.</span><span class="sxs-lookup"><span data-stu-id="176dc-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="176dc-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="176dc-128">-QuotationCharacter</span></span>
<span data-ttu-id="176dc-129">Optional.</span><span class="sxs-lookup"><span data-stu-id="176dc-129">Optional.</span></span>
<span data-ttu-id="176dc-130">Das Zeichen, das zum Zitieren eines bestimmten Felds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="176dc-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="176dc-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="176dc-131">-RecordSeparator</span></span>
<span data-ttu-id="176dc-132">Optional.</span><span class="sxs-lookup"><span data-stu-id="176dc-132">Optional.</span></span>
<span data-ttu-id="176dc-133">Die Zeichenfolge, die zum Trennen von Datensätzen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="176dc-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="176dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176dc-134">CommonParameters</span></span>
<span data-ttu-id="176dc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176dc-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176dc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176dc-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="176dc-137">INPUTS</span></span>

### <span data-ttu-id="176dc-138">Keine</span><span class="sxs-lookup"><span data-stu-id="176dc-138">None</span></span>

## <span data-ttu-id="176dc-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="176dc-139">OUTPUTS</span></span>

### <span data-ttu-id="176dc-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="176dc-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="176dc-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="176dc-141">NOTES</span></span>

## <span data-ttu-id="176dc-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="176dc-142">RELATED LINKS</span></span>
