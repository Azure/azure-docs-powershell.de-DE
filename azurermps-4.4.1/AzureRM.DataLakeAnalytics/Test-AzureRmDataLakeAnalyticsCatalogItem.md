---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 249ef7ae66436d4bf82b3b038aa8b1201f68110e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663329"
---
# <span data-ttu-id="6d860-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="6d860-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="6d860-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d860-102">SYNOPSIS</span></span>
<span data-ttu-id="6d860-103">Überprüft, ob ein Katalogelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d860-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d860-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d860-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d860-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d860-105">DESCRIPTION</span></span>
<span data-ttu-id="6d860-106">Das Cmdlet **Test-AzureRmDataLakeAnalyticsCatalogItem** überprüft, ob ein Azure Data Lake Analytics-Katalogelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d860-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="6d860-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d860-107">EXAMPLES</span></span>

### <span data-ttu-id="6d860-108">Beispiel 1: testen, ob ein Katalogelement vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="6d860-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="6d860-109">Dieser Befehl testet, ob ein angegebenes Schema Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d860-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="6d860-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d860-110">PARAMETERS</span></span>

### <span data-ttu-id="6d860-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="6d860-111">-Account</span></span>
<span data-ttu-id="6d860-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6d860-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6d860-113">-ItemType</span><span class="sxs-lookup"><span data-stu-id="6d860-113">-ItemType</span></span>
<span data-ttu-id="6d860-114">Gibt den Katalog Elementtyp des zu überprüfenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="6d860-114">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="6d860-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6d860-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6d860-116">Datenbank</span><span class="sxs-lookup"><span data-stu-id="6d860-116">Database</span></span>
- <span data-ttu-id="6d860-117">Schema</span><span class="sxs-lookup"><span data-stu-id="6d860-117">Schema</span></span>
- <span data-ttu-id="6d860-118">Assembly</span><span class="sxs-lookup"><span data-stu-id="6d860-118">Assembly</span></span>
- <span data-ttu-id="6d860-119">Tabelle</span><span class="sxs-lookup"><span data-stu-id="6d860-119">Table</span></span>
- <span data-ttu-id="6d860-120">Partitions</span><span class="sxs-lookup"><span data-stu-id="6d860-120">TablePartition</span></span>
- <span data-ttu-id="6d860-121">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="6d860-121">TableValuedFunction</span></span>
- <span data-ttu-id="6d860-122">Statistiken</span><span class="sxs-lookup"><span data-stu-id="6d860-122">TableStatistics</span></span>
- <span data-ttu-id="6d860-123">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="6d860-123">ExternalDataSource</span></span>
- <span data-ttu-id="6d860-124">Ansicht</span><span class="sxs-lookup"><span data-stu-id="6d860-124">View</span></span>
- <span data-ttu-id="6d860-125">Verfahren</span><span class="sxs-lookup"><span data-stu-id="6d860-125">Procedure</span></span>
- <span data-ttu-id="6d860-126">Geheimnis</span><span class="sxs-lookup"><span data-stu-id="6d860-126">Secret</span></span>
- <span data-ttu-id="6d860-127">Credential</span><span class="sxs-lookup"><span data-stu-id="6d860-127">Credential</span></span>
- <span data-ttu-id="6d860-128">Typen</span><span class="sxs-lookup"><span data-stu-id="6d860-128">Types</span></span>

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

### <span data-ttu-id="6d860-129">-Path</span><span class="sxs-lookup"><span data-stu-id="6d860-129">-Path</span></span>
<span data-ttu-id="6d860-130">Gibt den Pfad des abzurufenden Elements oder den Pfad zum übergeordneten Element der Liste der Elemente an.</span><span class="sxs-lookup"><span data-stu-id="6d860-130">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="6d860-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d860-131">-DefaultProfile</span></span>
<span data-ttu-id="6d860-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d860-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d860-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d860-133">CommonParameters</span></span>
<span data-ttu-id="6d860-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d860-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d860-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d860-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d860-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d860-136">INPUTS</span></span>

## <span data-ttu-id="6d860-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d860-137">OUTPUTS</span></span>

### <span data-ttu-id="6d860-138">bool</span><span class="sxs-lookup"><span data-stu-id="6d860-138">bool</span></span>
<span data-ttu-id="6d860-139">"Wahr" oder "falsch" gibt an, ob das angegebene Katalogelement vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d860-139">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="6d860-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d860-140">NOTES</span></span>

## <span data-ttu-id="6d860-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d860-141">RELATED LINKS</span></span>

[<span data-ttu-id="6d860-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="6d860-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


