---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: a3eff47b688f2f426c4f255d400ce1ef73c3c027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479298"
---
# <span data-ttu-id="5e478-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="5e478-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="5e478-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e478-102">SYNOPSIS</span></span>
<span data-ttu-id="5e478-103">Fügt eine Datenquelle zu einem Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e478-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e478-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e478-104">SYNTAX</span></span>

### <span data-ttu-id="5e478-105">Hinzufügen eines Data Lake-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5e478-105">Add a Data Lake storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e478-106">Hinzufügen eines BLOB-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5e478-106">Add a Blob storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e478-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e478-107">DESCRIPTION</span></span>
<span data-ttu-id="5e478-108">Das Cmdlet **Add-AzureRmDataLakeAnalyticsDataSource** fügt eine Datenquelle zu einem Azure Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e478-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5e478-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e478-109">EXAMPLES</span></span>

### <span data-ttu-id="5e478-110">Beispiel 1: Hinzufügen einer Datenquelle zu einem Konto</span><span class="sxs-lookup"><span data-stu-id="5e478-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="5e478-111">Dieser Befehl fügt einem Data Lake Analytics-Konto eine Data Lake Store-Datenquelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e478-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5e478-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e478-112">PARAMETERS</span></span>

### <span data-ttu-id="5e478-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="5e478-113">-AccessKey</span></span>
<span data-ttu-id="5e478-114">Gibt die Zugriffstaste des Azure-BLOB-speicherkontos an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e478-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e478-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="5e478-115">-Account</span></span>
<span data-ttu-id="5e478-116">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5e478-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5e478-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="5e478-117">-Blob</span></span>
<span data-ttu-id="5e478-118">Gibt den Namen des Azure-BLOB-speicherkontos an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e478-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e478-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5e478-119">-DataLakeStore</span></span>
<span data-ttu-id="5e478-120">Gibt den Namen des Azure Data Lake Store-Kontos an, das hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e478-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e478-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e478-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e478-122">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5e478-122">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="5e478-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e478-123">-DefaultProfile</span></span>
<span data-ttu-id="5e478-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e478-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e478-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e478-125">CommonParameters</span></span>
<span data-ttu-id="5e478-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e478-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e478-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e478-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e478-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e478-128">INPUTS</span></span>

## <span data-ttu-id="5e478-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e478-129">OUTPUTS</span></span>

### <span data-ttu-id="5e478-130">Keine</span><span class="sxs-lookup"><span data-stu-id="5e478-130">None</span></span>

## <span data-ttu-id="5e478-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e478-131">NOTES</span></span>

## <span data-ttu-id="5e478-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e478-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e478-133">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="5e478-133">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="5e478-134">Satz-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="5e478-134">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


