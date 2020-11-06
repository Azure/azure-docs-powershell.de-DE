---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504189"
---
# <span data-ttu-id="f5273-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="f5273-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="f5273-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5273-102">SYNOPSIS</span></span>
<span data-ttu-id="f5273-103">Ruft ein Data Lake Analytics-Katalogelement oder eine Art von Elementen ab.</span><span class="sxs-lookup"><span data-stu-id="f5273-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5273-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5273-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5273-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5273-105">DESCRIPTION</span></span>
<span data-ttu-id="f5273-106">Der **Get-AzureRmDataLakeAnalyticsCatalogItem** Ruft ein angegebenes Azure Data Lake Analytics-Katalogelement ab oder ruft Katalogelemente eines angegebenen Typs ab.</span><span class="sxs-lookup"><span data-stu-id="f5273-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="f5273-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5273-107">EXAMPLES</span></span>

### <span data-ttu-id="f5273-108">Beispiel 1: Abrufen einer angegebenen Datenbank</span><span class="sxs-lookup"><span data-stu-id="f5273-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="f5273-109">Dieser Befehl ruft die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="f5273-109">This command gets the specified database.</span></span>

### <span data-ttu-id="f5273-110">Beispiel 2: Abrufen von Tabellen in einer bestimmten Datenbank und einem angegebenen Schema</span><span class="sxs-lookup"><span data-stu-id="f5273-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="f5273-111">Mit diesem Befehl wird eine Liste der Tabellen in der angegebenen Datenbank abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f5273-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="f5273-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5273-112">PARAMETERS</span></span>

### <span data-ttu-id="f5273-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="f5273-113">-Account</span></span>
<span data-ttu-id="f5273-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f5273-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f5273-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="f5273-115">-ItemType</span></span>
<span data-ttu-id="f5273-116">Gibt den Katalog Elementtyp für die Elemente an, die abgerufen oder aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="f5273-116">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="f5273-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f5273-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5273-118">Datenbank</span><span class="sxs-lookup"><span data-stu-id="f5273-118">Database</span></span>
- <span data-ttu-id="f5273-119">Schema</span><span class="sxs-lookup"><span data-stu-id="f5273-119">Schema</span></span>
- <span data-ttu-id="f5273-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="f5273-120">Assembly</span></span>
- <span data-ttu-id="f5273-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="f5273-121">Table</span></span>
- <span data-ttu-id="f5273-122">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="f5273-122">TableValuedFunction</span></span>
- <span data-ttu-id="f5273-123">Statistiken</span><span class="sxs-lookup"><span data-stu-id="f5273-123">TableStatistics</span></span>
- <span data-ttu-id="f5273-124">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="f5273-124">ExternalDataSource</span></span>
- <span data-ttu-id="f5273-125">Ansicht</span><span class="sxs-lookup"><span data-stu-id="f5273-125">View</span></span>
- <span data-ttu-id="f5273-126">Verfahren</span><span class="sxs-lookup"><span data-stu-id="f5273-126">Procedure</span></span>
- <span data-ttu-id="f5273-127">Geheimnis</span><span class="sxs-lookup"><span data-stu-id="f5273-127">Secret</span></span>
- <span data-ttu-id="f5273-128">Credential</span><span class="sxs-lookup"><span data-stu-id="f5273-128">Credential</span></span>
- <span data-ttu-id="f5273-129">Typen</span><span class="sxs-lookup"><span data-stu-id="f5273-129">Types</span></span>
- <span data-ttu-id="f5273-130">Partitions</span><span class="sxs-lookup"><span data-stu-id="f5273-130">TablePartition</span></span>

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

### <span data-ttu-id="f5273-131">-Path</span><span class="sxs-lookup"><span data-stu-id="f5273-131">-Path</span></span>
<span data-ttu-id="f5273-132">Gibt den mehrteiligen Pfad zum abzurufenden Element oder das übergeordnete Element der Liste der Elemente an.</span><span class="sxs-lookup"><span data-stu-id="f5273-132">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="f5273-133">Die Teile des Pfads sollten durch einen Punkt (.) getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="f5273-133">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5273-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5273-134">-DefaultProfile</span></span>
<span data-ttu-id="f5273-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5273-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5273-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5273-136">CommonParameters</span></span>
<span data-ttu-id="f5273-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5273-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5273-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5273-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5273-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5273-139">INPUTS</span></span>

## <span data-ttu-id="f5273-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5273-140">OUTPUTS</span></span>

### <span data-ttu-id="f5273-141">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="f5273-141">CatalogItem</span></span>
<span data-ttu-id="f5273-142">Das angegebene Katalogelement</span><span class="sxs-lookup"><span data-stu-id="f5273-142">The specified catalog item.</span></span>

### <span data-ttu-id="f5273-143">Liste<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="f5273-143">List<CatalogItem></span></span>
<span data-ttu-id="f5273-144">Die Liste der angegebenen Katalogelemente unterhalb des zugehörigen Containers.</span><span class="sxs-lookup"><span data-stu-id="f5273-144">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="f5273-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5273-145">NOTES</span></span>

## <span data-ttu-id="f5273-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5273-146">RELATED LINKS</span></span>

[<span data-ttu-id="f5273-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="f5273-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


