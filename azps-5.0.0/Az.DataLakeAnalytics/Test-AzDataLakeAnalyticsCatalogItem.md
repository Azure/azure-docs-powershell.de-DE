---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297975"
---
# <span data-ttu-id="19524-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="19524-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="19524-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19524-102">SYNOPSIS</span></span>
<span data-ttu-id="19524-103">Überprüft, ob ein Katalogelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="19524-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="19524-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19524-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19524-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19524-105">DESCRIPTION</span></span>
<span data-ttu-id="19524-106">Das Cmdlet **Test-AzDataLakeAnalyticsCatalogItem** überprüft, ob ein Azure Data Lake Analytics-Katalogelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="19524-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="19524-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19524-107">EXAMPLES</span></span>

### <span data-ttu-id="19524-108">Beispiel 1: testen, ob ein Katalogelement vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="19524-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="19524-109">Dieser Befehl testet, ob ein angegebenes Schema Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="19524-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="19524-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19524-110">PARAMETERS</span></span>

### <span data-ttu-id="19524-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="19524-111">-Account</span></span>
<span data-ttu-id="19524-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="19524-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="19524-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19524-113">-DefaultProfile</span></span>
<span data-ttu-id="19524-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="19524-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19524-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="19524-115">-ItemType</span></span>
<span data-ttu-id="19524-116">Gibt den Katalog Elementtyp des zu überprüfenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="19524-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="19524-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="19524-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19524-118">Datenbank</span><span class="sxs-lookup"><span data-stu-id="19524-118">Database</span></span>
- <span data-ttu-id="19524-119">Schema</span><span class="sxs-lookup"><span data-stu-id="19524-119">Schema</span></span>
- <span data-ttu-id="19524-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="19524-120">Assembly</span></span>
- <span data-ttu-id="19524-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="19524-121">Table</span></span>
- <span data-ttu-id="19524-122">Partitions</span><span class="sxs-lookup"><span data-stu-id="19524-122">TablePartition</span></span>
- <span data-ttu-id="19524-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="19524-123">TableValuedFunction</span></span>
- <span data-ttu-id="19524-124">Statistiken</span><span class="sxs-lookup"><span data-stu-id="19524-124">TableStatistics</span></span>
- <span data-ttu-id="19524-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="19524-125">ExternalDataSource</span></span>
- <span data-ttu-id="19524-126">Ansicht</span><span class="sxs-lookup"><span data-stu-id="19524-126">View</span></span>
- <span data-ttu-id="19524-127">Verfahren</span><span class="sxs-lookup"><span data-stu-id="19524-127">Procedure</span></span>
- <span data-ttu-id="19524-128">Geheimnis</span><span class="sxs-lookup"><span data-stu-id="19524-128">Secret</span></span>
- <span data-ttu-id="19524-129">Credential</span><span class="sxs-lookup"><span data-stu-id="19524-129">Credential</span></span>
- <span data-ttu-id="19524-130">Typen</span><span class="sxs-lookup"><span data-stu-id="19524-130">Types</span></span>

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

### <span data-ttu-id="19524-131">-Path</span><span class="sxs-lookup"><span data-stu-id="19524-131">-Path</span></span>
<span data-ttu-id="19524-132">Gibt den Pfad des abzurufenden Elements oder den Pfad zum übergeordneten Element der Liste der Elemente an.</span><span class="sxs-lookup"><span data-stu-id="19524-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="19524-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19524-133">CommonParameters</span></span>
<span data-ttu-id="19524-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19524-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19524-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19524-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19524-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19524-136">INPUTS</span></span>

### <span data-ttu-id="19524-137">System. String</span><span class="sxs-lookup"><span data-stu-id="19524-137">System.String</span></span>

### <span data-ttu-id="19524-138">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="19524-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="19524-139">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="19524-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="19524-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19524-140">OUTPUTS</span></span>

### <span data-ttu-id="19524-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19524-141">System.Boolean</span></span>

## <span data-ttu-id="19524-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="19524-142">NOTES</span></span>

## <span data-ttu-id="19524-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19524-143">RELATED LINKS</span></span>

[<span data-ttu-id="19524-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="19524-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


