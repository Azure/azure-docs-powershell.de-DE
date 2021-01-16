---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296050"
---
# <span data-ttu-id="de163-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="de163-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="de163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de163-102">SYNOPSIS</span></span>
<span data-ttu-id="de163-103">Sucht nach dem Vorhandensein eines Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="de163-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="de163-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de163-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de163-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de163-105">DESCRIPTION</span></span>
<span data-ttu-id="de163-106">Das **Cmdlet "Test-AzDataLakeAnalyticsCatalogItem"** sucht nach dem Vorhandensein eines Azure Data Lake Analytics-Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="de163-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="de163-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="de163-107">EXAMPLES</span></span>

### <span data-ttu-id="de163-108">Beispiel 1: Testen, ob ein Katalogelement vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="de163-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="de163-109">Mit diesem Befehl wird überprüft, ob ein angegebenes Schemaelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="de163-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="de163-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de163-110">PARAMETERS</span></span>

### <span data-ttu-id="de163-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="de163-111">-Account</span></span>
<span data-ttu-id="de163-112">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="de163-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="de163-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de163-113">-DefaultProfile</span></span>
<span data-ttu-id="de163-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="de163-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de163-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="de163-115">-ItemType</span></span>
<span data-ttu-id="de163-116">Gibt den Katalogelementtyp des zu überprüfenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="de163-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="de163-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="de163-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="de163-118">Datenbank</span><span class="sxs-lookup"><span data-stu-id="de163-118">Database</span></span>
- <span data-ttu-id="de163-119">Schema</span><span class="sxs-lookup"><span data-stu-id="de163-119">Schema</span></span>
- <span data-ttu-id="de163-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="de163-120">Assembly</span></span>
- <span data-ttu-id="de163-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="de163-121">Table</span></span>
- <span data-ttu-id="de163-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="de163-122">TablePartition</span></span>
- <span data-ttu-id="de163-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="de163-123">TableValuedFunction</span></span>
- <span data-ttu-id="de163-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="de163-124">TableStatistics</span></span>
- <span data-ttu-id="de163-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="de163-125">ExternalDataSource</span></span>
- <span data-ttu-id="de163-126">Ansicht</span><span class="sxs-lookup"><span data-stu-id="de163-126">View</span></span>
- <span data-ttu-id="de163-127">Vorgehensweise</span><span class="sxs-lookup"><span data-stu-id="de163-127">Procedure</span></span>
- <span data-ttu-id="de163-128">Geheim</span><span class="sxs-lookup"><span data-stu-id="de163-128">Secret</span></span>
- <span data-ttu-id="de163-129">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="de163-129">Credential</span></span>
- <span data-ttu-id="de163-130">Typen</span><span class="sxs-lookup"><span data-stu-id="de163-130">Types</span></span>

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

### <span data-ttu-id="de163-131">-Path</span><span class="sxs-lookup"><span data-stu-id="de163-131">-Path</span></span>
<span data-ttu-id="de163-132">Gibt den Pfad zum abrufenden Element oder den Pfad zum übergeordneten Element der zu listenden Elemente an.</span><span class="sxs-lookup"><span data-stu-id="de163-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="de163-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de163-133">CommonParameters</span></span>
<span data-ttu-id="de163-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de163-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de163-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de163-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de163-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="de163-136">INPUTS</span></span>

### <span data-ttu-id="de163-137">System.String</span><span class="sxs-lookup"><span data-stu-id="de163-137">System.String</span></span>

### <span data-ttu-id="de163-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="de163-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="de163-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="de163-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="de163-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="de163-140">OUTPUTS</span></span>

### <span data-ttu-id="de163-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de163-141">System.Boolean</span></span>

## <span data-ttu-id="de163-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="de163-142">NOTES</span></span>

## <span data-ttu-id="de163-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="de163-143">RELATED LINKS</span></span>

[<span data-ttu-id="de163-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="de163-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


