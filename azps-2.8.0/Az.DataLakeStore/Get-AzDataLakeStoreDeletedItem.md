---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 750203e954ef96619e32b63ffd6eae333bb852f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651557"
---
# <span data-ttu-id="3ce09-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="3ce09-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="3ce09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ce09-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce09-103">Sucht nach gelöschten Einträgen im Papierkorb, die dem Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3ce09-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="3ce09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ce09-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ce09-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce09-106">Das Cmdlet " **Get-AzDataLakeStoreDeletedItem** " durchsucht die gelöschten Dateien oder Ordner im Data Lake Store, die dem angegebenen Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3ce09-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="3ce09-107">Es werden die folgenden Attribute der gelöschten Elemente angezeigt: OriginalPath, TrashDirPath, Typ, Erstellungsdatum.</span><span class="sxs-lookup"><span data-stu-id="3ce09-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="3ce09-108">Dies kann ein langwieriger Vorgang sein, da er möglicherweise Millionen von Dateien im Papierkorb durchsuchen und als Job ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="3ce09-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>

## <span data-ttu-id="3ce09-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ce09-109">EXAMPLES</span></span>

### <span data-ttu-id="3ce09-110">Beispiel: Abrufen von Details zu einer Datei aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3ce09-110">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="3ce09-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ce09-111">PARAMETERS</span></span>

### <span data-ttu-id="3ce09-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="3ce09-112">-Account</span></span>
<span data-ttu-id="3ce09-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3ce09-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3ce09-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ce09-114">-AsJob</span></span>
<span data-ttu-id="3ce09-115">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="3ce09-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3ce09-116">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="3ce09-116">-Count</span></span>
<span data-ttu-id="3ce09-117">Gibt die Anzahl der Ergebnisse an, die der Benutzer ermitteln möchte.</span><span class="sxs-lookup"><span data-stu-id="3ce09-117">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="3ce09-118">Die Abfrage wird ausgeführt, bis Sie die Anzahl der Ergebnisse findet, oder Sie durchsucht den gesamten Papierkorb, je nachdem, was zuerst geschieht.</span><span class="sxs-lookup"><span data-stu-id="3ce09-118">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="3ce09-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce09-119">-DefaultProfile</span></span>
<span data-ttu-id="3ce09-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ce09-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce09-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="3ce09-121">-Filter</span></span>
<span data-ttu-id="3ce09-122">Gibt die Suchabfrage an.</span><span class="sxs-lookup"><span data-stu-id="3ce09-122">Specifies the search query.</span></span> <span data-ttu-id="3ce09-123">Ein spezifischer Wert gibt relevantere Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="3ce09-123">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="3ce09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce09-124">CommonParameters</span></span>
<span data-ttu-id="3ce09-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ce09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce09-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce09-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce09-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ce09-127">INPUTS</span></span>

### <span data-ttu-id="3ce09-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3ce09-128">System.String</span></span>

## <span data-ttu-id="3ce09-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ce09-129">OUTPUTS</span></span>

### <span data-ttu-id="3ce09-130">System. Collections. Generic. List<Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="3ce09-130">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="3ce09-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ce09-131">NOTES</span></span>

## <span data-ttu-id="3ce09-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ce09-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ce09-133">Wiederherstellen – AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="3ce09-133">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)