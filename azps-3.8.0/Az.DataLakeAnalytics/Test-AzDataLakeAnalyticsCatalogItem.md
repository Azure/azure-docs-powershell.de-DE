---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995233"
---
# <span data-ttu-id="22271-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="22271-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="22271-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22271-102">SYNOPSIS</span></span>
<span data-ttu-id="22271-103">Überprüft, ob ein Katalogelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="22271-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="22271-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22271-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22271-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22271-105">DESCRIPTION</span></span>
<span data-ttu-id="22271-106">Das Cmdlet **Test-AzDataLakeAnalyticsCatalogItem** überprüft, ob ein Azure Data Lake Analytics-Katalogelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="22271-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="22271-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22271-107">EXAMPLES</span></span>

### <span data-ttu-id="22271-108">Beispiel 1: testen, ob ein Katalogelement vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="22271-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="22271-109">Dieser Befehl testet, ob ein angegebenes Schema Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="22271-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="22271-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22271-110">PARAMETERS</span></span>

### <span data-ttu-id="22271-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="22271-111">-Account</span></span>
<span data-ttu-id="22271-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="22271-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="22271-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22271-113">-DefaultProfile</span></span>
<span data-ttu-id="22271-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="22271-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22271-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="22271-115">-ItemType</span></span>
<span data-ttu-id="22271-116">Gibt den Katalog Elementtyp des zu überprüfenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="22271-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="22271-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22271-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22271-118">Datenbank</span><span class="sxs-lookup"><span data-stu-id="22271-118">Database</span></span>
- <span data-ttu-id="22271-119">Schema</span><span class="sxs-lookup"><span data-stu-id="22271-119">Schema</span></span>
- <span data-ttu-id="22271-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="22271-120">Assembly</span></span>
- <span data-ttu-id="22271-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="22271-121">Table</span></span>
- <span data-ttu-id="22271-122">Partitions</span><span class="sxs-lookup"><span data-stu-id="22271-122">TablePartition</span></span>
- <span data-ttu-id="22271-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="22271-123">TableValuedFunction</span></span>
- <span data-ttu-id="22271-124">Statistiken</span><span class="sxs-lookup"><span data-stu-id="22271-124">TableStatistics</span></span>
- <span data-ttu-id="22271-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="22271-125">ExternalDataSource</span></span>
- <span data-ttu-id="22271-126">Ansicht</span><span class="sxs-lookup"><span data-stu-id="22271-126">View</span></span>
- <span data-ttu-id="22271-127">Verfahren</span><span class="sxs-lookup"><span data-stu-id="22271-127">Procedure</span></span>
- <span data-ttu-id="22271-128">Geheimnis</span><span class="sxs-lookup"><span data-stu-id="22271-128">Secret</span></span>
- <span data-ttu-id="22271-129">Credential</span><span class="sxs-lookup"><span data-stu-id="22271-129">Credential</span></span>
- <span data-ttu-id="22271-130">Typen</span><span class="sxs-lookup"><span data-stu-id="22271-130">Types</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22271-131">-Path</span><span class="sxs-lookup"><span data-stu-id="22271-131">-Path</span></span>
<span data-ttu-id="22271-132">Gibt den Pfad des abzurufenden Elements oder den Pfad zum übergeordneten Element der Liste der Elemente an.</span><span class="sxs-lookup"><span data-stu-id="22271-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22271-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22271-133">CommonParameters</span></span>
<span data-ttu-id="22271-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22271-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22271-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22271-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22271-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22271-136">INPUTS</span></span>

### <span data-ttu-id="22271-137">System. String</span><span class="sxs-lookup"><span data-stu-id="22271-137">System.String</span></span>

### <span data-ttu-id="22271-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="22271-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="22271-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="22271-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="22271-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22271-140">OUTPUTS</span></span>

### <span data-ttu-id="22271-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22271-141">System.Boolean</span></span>

## <span data-ttu-id="22271-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="22271-142">NOTES</span></span>

## <span data-ttu-id="22271-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22271-143">RELATED LINKS</span></span>

[<span data-ttu-id="22271-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="22271-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


