---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 19b8b5a00e5bcb75b90a91097316dc065afa025b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661310"
---
# <span data-ttu-id="3563f-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3563f-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="3563f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3563f-102">SYNOPSIS</span></span>
<span data-ttu-id="3563f-103">Fügt eine Datenquelle zu einem Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="3563f-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="3563f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3563f-104">SYNTAX</span></span>

### <span data-ttu-id="3563f-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3563f-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3563f-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3563f-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3563f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3563f-107">DESCRIPTION</span></span>
<span data-ttu-id="3563f-108">Das Cmdlet **Add-AzDataLakeAnalyticsDataSource** fügt eine Datenquelle zu einem Azure Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="3563f-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3563f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3563f-109">EXAMPLES</span></span>

### <span data-ttu-id="3563f-110">Beispiel 1: Hinzufügen einer Datenquelle zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="3563f-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="3563f-111">Dieser Befehl fügt einem Data Lake Analytics-Konto eine Data Lake Store-Datenquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="3563f-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="3563f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3563f-112">PARAMETERS</span></span>

### <span data-ttu-id="3563f-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="3563f-113">-AccessKey</span></span>
<span data-ttu-id="3563f-114">Gibt die Zugriffstaste des Azure-BLOB-speicherkontos an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3563f-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3563f-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="3563f-115">-Account</span></span>
<span data-ttu-id="3563f-116">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3563f-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="3563f-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="3563f-117">-Blob</span></span>
<span data-ttu-id="3563f-118">Gibt den Namen des Azure-BLOB-speicherkontos an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3563f-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3563f-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3563f-119">-DataLakeStore</span></span>
<span data-ttu-id="3563f-120">Gibt den Namen des Azure Data Lake Store-Kontos an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3563f-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3563f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3563f-121">-DefaultProfile</span></span>
<span data-ttu-id="3563f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3563f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3563f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3563f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3563f-124">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3563f-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3563f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3563f-125">CommonParameters</span></span>
<span data-ttu-id="3563f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3563f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3563f-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3563f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3563f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3563f-128">INPUTS</span></span>

### <span data-ttu-id="3563f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3563f-129">System.String</span></span>

## <span data-ttu-id="3563f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3563f-130">OUTPUTS</span></span>

### <span data-ttu-id="3563f-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="3563f-131">System.Object</span></span>
## <span data-ttu-id="3563f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3563f-132">NOTES</span></span>

## <span data-ttu-id="3563f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3563f-133">RELATED LINKS</span></span>

[<span data-ttu-id="3563f-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3563f-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="3563f-135">Satz-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="3563f-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


