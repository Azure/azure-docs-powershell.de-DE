---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370024"
---
# <span data-ttu-id="4dfa9-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="4dfa9-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="4dfa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfa9-103">Ruft ein Data Lake Analytics-Katalogelement oder Elementtypen ab.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="4dfa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dfa9-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dfa9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dfa9-105">DESCRIPTION</span></span>
<span data-ttu-id="4dfa9-106">Die **Get-AzDataLakeAnalyticsCatalogItem** ruft ein angegebenes Azure Data Lake Analytics-Katalogelement oder Katalogelemente eines angegebenen Typs ab.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="4dfa9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4dfa9-107">EXAMPLES</span></span>

### <span data-ttu-id="4dfa9-108">Beispiel 1: Erhalten einer angegebenen Datenbank</span><span class="sxs-lookup"><span data-stu-id="4dfa9-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="4dfa9-109">Dieser Befehl ruft die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-109">This command gets the specified database.</span></span>

### <span data-ttu-id="4dfa9-110">Beispiel 2: Tabellen in einer angegebenen Datenbank und einem angegebenen Schema erhalten</span><span class="sxs-lookup"><span data-stu-id="4dfa9-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="4dfa9-111">Dieser Befehl ruft eine Liste der Tabellen in der angegebenen Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="4dfa9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dfa9-112">PARAMETERS</span></span>

### <span data-ttu-id="4dfa9-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="4dfa9-113">-Account</span></span>
<span data-ttu-id="4dfa9-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4dfa9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfa9-115">-DefaultProfile</span></span>
<span data-ttu-id="4dfa9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4dfa9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dfa9-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="4dfa9-117">-ItemType</span></span>
<span data-ttu-id="4dfa9-118">Gibt den Katalogelementtyp des Elements an, das abgerufen oder aufgelistet wird.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="4dfa9-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4dfa9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dfa9-120">Datenbank</span><span class="sxs-lookup"><span data-stu-id="4dfa9-120">Database</span></span>
- <span data-ttu-id="4dfa9-121">Schema</span><span class="sxs-lookup"><span data-stu-id="4dfa9-121">Schema</span></span>
- <span data-ttu-id="4dfa9-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="4dfa9-122">Assembly</span></span>
- <span data-ttu-id="4dfa9-123">Tabelle</span><span class="sxs-lookup"><span data-stu-id="4dfa9-123">Table</span></span>
- <span data-ttu-id="4dfa9-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="4dfa9-124">TableValuedFunction</span></span>
- <span data-ttu-id="4dfa9-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="4dfa9-125">TableStatistics</span></span>
- <span data-ttu-id="4dfa9-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="4dfa9-126">ExternalDataSource</span></span>
- <span data-ttu-id="4dfa9-127">Ansicht</span><span class="sxs-lookup"><span data-stu-id="4dfa9-127">View</span></span>
- <span data-ttu-id="4dfa9-128">Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="4dfa9-128">Procedure</span></span>
- <span data-ttu-id="4dfa9-129">Geheim</span><span class="sxs-lookup"><span data-stu-id="4dfa9-129">Secret</span></span>
- <span data-ttu-id="4dfa9-130">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4dfa9-130">Credential</span></span>
- <span data-ttu-id="4dfa9-131">Typen</span><span class="sxs-lookup"><span data-stu-id="4dfa9-131">Types</span></span>
- <span data-ttu-id="4dfa9-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="4dfa9-132">TablePartition</span></span>

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

### <span data-ttu-id="4dfa9-133">-Path</span><span class="sxs-lookup"><span data-stu-id="4dfa9-133">-Path</span></span>
<span data-ttu-id="4dfa9-134">Gibt den mehrteiligen Pfad zum abzurufenden Element oder zum übergeordneten Element der zu listenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="4dfa9-135">Die Teile des Pfads sollten durch einen Bestimmten (.) getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="4dfa9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfa9-136">CommonParameters</span></span>
<span data-ttu-id="4dfa9-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfa9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfa9-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dfa9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfa9-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4dfa9-139">INPUTS</span></span>

### <span data-ttu-id="4dfa9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4dfa9-140">System.String</span></span>

### <span data-ttu-id="4dfa9-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="4dfa9-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="4dfa9-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="4dfa9-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="4dfa9-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4dfa9-143">OUTPUTS</span></span>

### <span data-ttu-id="4dfa9-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="4dfa9-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="4dfa9-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4dfa9-145">NOTES</span></span>

## <span data-ttu-id="4dfa9-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4dfa9-146">RELATED LINKS</span></span>

[<span data-ttu-id="4dfa9-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="4dfa9-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


