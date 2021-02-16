---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153417"
---
# <span data-ttu-id="dd347-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="dd347-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="dd347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd347-102">SYNOPSIS</span></span>
<span data-ttu-id="dd347-103">Ruft eine Data Lake Analytics-Datenquelle ab.</span><span class="sxs-lookup"><span data-stu-id="dd347-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="dd347-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd347-104">SYNTAX</span></span>

### <span data-ttu-id="dd347-105">GetAllDataSources (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd347-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd347-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dd347-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd347-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd347-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd347-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd347-108">DESCRIPTION</span></span>
<span data-ttu-id="dd347-109">Das **Cmdlet "Get-AzDataLakeAnalyticsDataSource"** ruft eine Azure Data Lake Analytics-Datenquelle ab.</span><span class="sxs-lookup"><span data-stu-id="dd347-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="dd347-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd347-110">EXAMPLES</span></span>

### <span data-ttu-id="dd347-111">Beispiel 1: Erhalten einer Datenquelle aus einem Konto</span><span class="sxs-lookup"><span data-stu-id="dd347-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="dd347-112">Dieser Befehl ruft eine Data Lake Store-Datenquelle namens "ContosoAdls" aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="dd347-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="dd347-113">Beispiel 2: Erhalten der Liste der Data Lake Store-Konten in einem Data Lake Analytics-Konto</span><span class="sxs-lookup"><span data-stu-id="dd347-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="dd347-114">Dieser Befehl ruft alle Data Lake Store-Konten aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="dd347-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="dd347-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd347-115">PARAMETERS</span></span>

### <span data-ttu-id="dd347-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="dd347-116">-Account</span></span>
<span data-ttu-id="dd347-117">Gibt das Data Lake Analytics-Konto an, das dieses Cmdlet Datenquellen erhält.</span><span class="sxs-lookup"><span data-stu-id="dd347-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="dd347-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="dd347-118">-Blob</span></span>
<span data-ttu-id="dd347-119">Gibt den Namen der Azure Blob Storage-Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="dd347-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd347-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dd347-120">-DataLakeStore</span></span>
<span data-ttu-id="dd347-121">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="dd347-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd347-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd347-122">-DefaultProfile</span></span>
<span data-ttu-id="dd347-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dd347-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd347-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd347-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd347-125">Gibt den Namen der Ressourcengruppe an, der die Datenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="dd347-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd347-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd347-126">CommonParameters</span></span>
<span data-ttu-id="dd347-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd347-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd347-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd347-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd347-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd347-129">INPUTS</span></span>

### <span data-ttu-id="dd347-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dd347-130">System.String</span></span>

## <span data-ttu-id="dd347-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd347-131">OUTPUTS</span></span>

### <span data-ttu-id="dd347-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="dd347-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="dd347-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="dd347-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="dd347-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="dd347-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="dd347-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dd347-135">NOTES</span></span>

## <span data-ttu-id="dd347-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dd347-136">RELATED LINKS</span></span>

[<span data-ttu-id="dd347-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="dd347-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="dd347-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="dd347-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="dd347-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="dd347-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


