---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: 942bd2635c79a925779239e9746cef53195b202e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944561"
---
# <span data-ttu-id="db6e9-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="db6e9-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="db6e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="db6e9-103">Erstellt ein Blobabfragekonfigurationsobjekt, das in Get-AzStorageBlobQueryResult verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="db6e9-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="db6e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db6e9-104">SYNTAX</span></span>

### <span data-ttu-id="db6e9-105">Csv (Standard)</span><span class="sxs-lookup"><span data-stu-id="db6e9-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="db6e9-106">Json</span><span class="sxs-lookup"><span data-stu-id="db6e9-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="db6e9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db6e9-107">DESCRIPTION</span></span>
<span data-ttu-id="db6e9-108">Das **Cmdlet New-AzStorageBlobQueryConfig** erstellt ein Blobabfragekonfigurationsobjekt, das in Get-AzStorageBlobQueryResult verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="db6e9-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="db6e9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db6e9-109">EXAMPLES</span></span>

### <span data-ttu-id="db6e9-110">Beispiel 1: Erstellen von Blobabfragen konfiguriert , und Abfragen eines Blobs</span><span class="sxs-lookup"><span data-stu-id="db6e9-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="db6e9-111">Dieser Befehl erstellt zuerst das Eingabekonfigurationsobjekt als CSV und das Ausgabekonfigurationsobjekt als json, und verwenden Sie dann die 2 Konfigurationen zum Abfragen des Blobs.</span><span class="sxs-lookup"><span data-stu-id="db6e9-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="db6e9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="db6e9-112">PARAMETERS</span></span>

### <span data-ttu-id="db6e9-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="db6e9-113">-AsCsv</span></span>
<span data-ttu-id="db6e9-114">Geben Sie an, dass eine Blob Query-Konfiguration für CSV erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db6e9-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="db6e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db6e9-115">-AsJob</span></span>
<span data-ttu-id="db6e9-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="db6e9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db6e9-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="db6e9-117">-AsJson</span></span>
<span data-ttu-id="db6e9-118">Geben Sie an, dass eine Blob Query-Konfiguration für Json erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db6e9-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="db6e9-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="db6e9-119">-ColumnSeparator</span></span>
<span data-ttu-id="db6e9-120">Optional.</span><span class="sxs-lookup"><span data-stu-id="db6e9-120">Optional.</span></span>
<span data-ttu-id="db6e9-121">Die Zeichenfolge, die zum Trennen von Spalten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db6e9-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="db6e9-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="db6e9-122">-EscapeCharacter</span></span>
<span data-ttu-id="db6e9-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="db6e9-123">Optional.</span></span>
<span data-ttu-id="db6e9-124">Das Zeichen, das als Escapezeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db6e9-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="db6e9-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="db6e9-125">-HasHeader</span></span>
<span data-ttu-id="db6e9-126">Optional.</span><span class="sxs-lookup"><span data-stu-id="db6e9-126">Optional.</span></span>
<span data-ttu-id="db6e9-127">Geben Sie an, dass die Daten Überschriften enthalten.</span><span class="sxs-lookup"><span data-stu-id="db6e9-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="db6e9-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="db6e9-128">-QuotationCharacter</span></span>
<span data-ttu-id="db6e9-129">Optional.</span><span class="sxs-lookup"><span data-stu-id="db6e9-129">Optional.</span></span>
<span data-ttu-id="db6e9-130">Das Zeichen, das zum Zitieren eines bestimmten Felds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db6e9-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="db6e9-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="db6e9-131">-RecordSeparator</span></span>
<span data-ttu-id="db6e9-132">Optional.</span><span class="sxs-lookup"><span data-stu-id="db6e9-132">Optional.</span></span>
<span data-ttu-id="db6e9-133">Die Zeichenfolge, die zum Trennen von Datensätzen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db6e9-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="db6e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6e9-134">CommonParameters</span></span>
<span data-ttu-id="db6e9-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6e9-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6e9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6e9-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db6e9-137">INPUTS</span></span>

### <span data-ttu-id="db6e9-138">Keine</span><span class="sxs-lookup"><span data-stu-id="db6e9-138">None</span></span>

## <span data-ttu-id="db6e9-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db6e9-139">OUTPUTS</span></span>

### <span data-ttu-id="db6e9-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="db6e9-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="db6e9-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="db6e9-141">NOTES</span></span>

## <span data-ttu-id="db6e9-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="db6e9-142">RELATED LINKS</span></span>
