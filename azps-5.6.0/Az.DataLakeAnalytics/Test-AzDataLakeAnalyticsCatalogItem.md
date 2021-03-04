---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2642a310e2a318498b3d170b463ac7e366bf5818
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921283"
---
# <span data-ttu-id="551ca-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="551ca-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="551ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="551ca-102">SYNOPSIS</span></span>
<span data-ttu-id="551ca-103">Überprüft das Vorhandensein eines Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="551ca-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="551ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="551ca-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="551ca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="551ca-105">DESCRIPTION</span></span>
<span data-ttu-id="551ca-106">Das **Cmdlet Test-AzDataLakeAnalyticsCatalogItem** überprüft das Vorhandensein eines Azure Data Lake Analytics-Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="551ca-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="551ca-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="551ca-107">EXAMPLES</span></span>

### <span data-ttu-id="551ca-108">Beispiel 1: Testen, ob ein Katalogelement vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="551ca-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="551ca-109">Mit diesem Befehl wird überprüft, ob ein angegebenes Schemaelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="551ca-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="551ca-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="551ca-110">PARAMETERS</span></span>

### <span data-ttu-id="551ca-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="551ca-111">-Account</span></span>
<span data-ttu-id="551ca-112">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="551ca-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="551ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551ca-113">-DefaultProfile</span></span>
<span data-ttu-id="551ca-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="551ca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="551ca-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="551ca-115">-ItemType</span></span>
<span data-ttu-id="551ca-116">Gibt den Katalogelementtyp des zu überprüfenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="551ca-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="551ca-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="551ca-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="551ca-118">Datenbank</span><span class="sxs-lookup"><span data-stu-id="551ca-118">Database</span></span>
- <span data-ttu-id="551ca-119">Schema</span><span class="sxs-lookup"><span data-stu-id="551ca-119">Schema</span></span>
- <span data-ttu-id="551ca-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="551ca-120">Assembly</span></span>
- <span data-ttu-id="551ca-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="551ca-121">Table</span></span>
- <span data-ttu-id="551ca-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="551ca-122">TablePartition</span></span>
- <span data-ttu-id="551ca-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="551ca-123">TableValuedFunction</span></span>
- <span data-ttu-id="551ca-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="551ca-124">TableStatistics</span></span>
- <span data-ttu-id="551ca-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="551ca-125">ExternalDataSource</span></span>
- <span data-ttu-id="551ca-126">Ansicht</span><span class="sxs-lookup"><span data-stu-id="551ca-126">View</span></span>
- <span data-ttu-id="551ca-127">Verfahren</span><span class="sxs-lookup"><span data-stu-id="551ca-127">Procedure</span></span>
- <span data-ttu-id="551ca-128">Geheim</span><span class="sxs-lookup"><span data-stu-id="551ca-128">Secret</span></span>
- <span data-ttu-id="551ca-129">Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="551ca-129">Credential</span></span>
- <span data-ttu-id="551ca-130">Typen</span><span class="sxs-lookup"><span data-stu-id="551ca-130">Types</span></span>

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

### <span data-ttu-id="551ca-131">-Path</span><span class="sxs-lookup"><span data-stu-id="551ca-131">-Path</span></span>
<span data-ttu-id="551ca-132">Gibt den Pfad zum zu abrufenden Element oder den Pfad zum übergeordneten Element der elemente an, die sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="551ca-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="551ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551ca-133">CommonParameters</span></span>
<span data-ttu-id="551ca-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551ca-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="551ca-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551ca-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="551ca-136">INPUTS</span></span>

### <span data-ttu-id="551ca-137">System.String</span><span class="sxs-lookup"><span data-stu-id="551ca-137">System.String</span></span>

### <span data-ttu-id="551ca-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="551ca-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="551ca-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="551ca-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="551ca-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="551ca-140">OUTPUTS</span></span>

### <span data-ttu-id="551ca-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="551ca-141">System.Boolean</span></span>

## <span data-ttu-id="551ca-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="551ca-142">NOTES</span></span>

## <span data-ttu-id="551ca-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="551ca-143">RELATED LINKS</span></span>

[<span data-ttu-id="551ca-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="551ca-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


