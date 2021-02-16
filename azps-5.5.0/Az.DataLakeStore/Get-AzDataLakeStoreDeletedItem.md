---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170838"
---
# <span data-ttu-id="0b039-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="0b039-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="0b039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b039-102">SYNOPSIS</span></span>
<span data-ttu-id="0b039-103">Sucht nach gelöschten Einträgen im Papierkorb, die dem Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b039-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="0b039-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b039-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b039-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b039-105">DESCRIPTION</span></span>
<span data-ttu-id="0b039-106">Das **Cmdlet "Get-AzDataLakeStoreDeletedItem"** durchsucht die gelöschten Dateien oder Ordner im Data Lake Store, die dem angegebenen Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b039-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="0b039-107">Es zeigt die folgenden Attribute der gelöschten Elemente an– "OriginalPath", "TrashDirPath", "Type", "CreationTime".</span><span class="sxs-lookup"><span data-stu-id="0b039-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="0b039-108">Dies kann ein Vorgang mit langer Dauer sein, da er möglicherweise Millionen von Dateien im Papierkorb durchsuchen muss und als Auftrag ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b039-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="0b039-109">Vorsicht: Das Wiederherstellen von Dateien ist ein Vorgang nach bestem Aufwand.</span><span class="sxs-lookup"><span data-stu-id="0b039-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="0b039-110">Es gibt keine Garantie dafür, dass eine Datei nach dem Löschen wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b039-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="0b039-111">Die Verwendung dieser API wird über Whitelisting aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0b039-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="0b039-112">Wenn Ihr ADL-Konto nicht in der Whiteliste aufgeführt ist, wird mit dieser API die Ausnahme "Nicht implementiert" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="0b039-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="0b039-113">Für weitere Informationen und Unterstützung wenden Sie sich bitte an den Microsoft-Support.</span><span class="sxs-lookup"><span data-stu-id="0b039-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="0b039-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b039-114">EXAMPLES</span></span>

### <span data-ttu-id="0b039-115">Beispiel: Details zu einer Datei aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0b039-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="0b039-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b039-116">PARAMETERS</span></span>

### <span data-ttu-id="0b039-117">-Konto</span><span class="sxs-lookup"><span data-stu-id="0b039-117">-Account</span></span>
<span data-ttu-id="0b039-118">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0b039-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0b039-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b039-119">-AsJob</span></span>
<span data-ttu-id="0b039-120">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="0b039-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="0b039-121">-Count</span><span class="sxs-lookup"><span data-stu-id="0b039-121">-Count</span></span>
<span data-ttu-id="0b039-122">Gibt die Anzahl der Ergebnisse an, die der Benutzer suchen möchte.</span><span class="sxs-lookup"><span data-stu-id="0b039-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="0b039-123">Die Abfrage wird ausgeführt, bis sie die Ergebnisse für "Anzahl" findet, oder sie durchsucht den gesamten Papierkorb, ganz gleich, was zuerst geschieht.</span><span class="sxs-lookup"><span data-stu-id="0b039-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b039-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b039-124">-DefaultProfile</span></span>
<span data-ttu-id="0b039-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b039-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b039-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="0b039-126">-Filter</span></span>
<span data-ttu-id="0b039-127">Gibt die Suchabfrage an.</span><span class="sxs-lookup"><span data-stu-id="0b039-127">Specifies the search query.</span></span> <span data-ttu-id="0b039-128">Ein spezifischerer Wert führt zu relevanteren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="0b039-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="0b039-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b039-129">CommonParameters</span></span>
<span data-ttu-id="0b039-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b039-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b039-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b039-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b039-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b039-132">INPUTS</span></span>

### <span data-ttu-id="0b039-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0b039-133">System.String</span></span>

## <span data-ttu-id="0b039-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b039-134">OUTPUTS</span></span>

### <span data-ttu-id="0b039-135">System.Collections.generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="0b039-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="0b039-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0b039-136">NOTES</span></span>

## <span data-ttu-id="0b039-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0b039-137">RELATED LINKS</span></span>

[<span data-ttu-id="0b039-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="0b039-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)