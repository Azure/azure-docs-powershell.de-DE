---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665072"
---
# <span data-ttu-id="97ae2-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="97ae2-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="97ae2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="97ae2-103">Ruft eine Data Lake Analytics-Datenquelle ab.</span><span class="sxs-lookup"><span data-stu-id="97ae2-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97ae2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97ae2-104">SYNTAX</span></span>

### <span data-ttu-id="97ae2-105">Auflisten aller Datenquellen (Standard)</span><span class="sxs-lookup"><span data-stu-id="97ae2-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ae2-106">Abrufen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="97ae2-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ae2-107">Abrufen eines BLOB-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="97ae2-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97ae2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97ae2-108">DESCRIPTION</span></span>
<span data-ttu-id="97ae2-109">Das Cmdlet " **Get-AzureRmDataLakeAnalyticsDataSource** " Ruft eine Azure Data Lake Analytics-Datenquelle ab.</span><span class="sxs-lookup"><span data-stu-id="97ae2-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="97ae2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97ae2-110">EXAMPLES</span></span>

### <span data-ttu-id="97ae2-111">Beispiel 1: Abrufen einer Datenquelle von einem Konto</span><span class="sxs-lookup"><span data-stu-id="97ae2-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="97ae2-112">Dieser Befehl ruft eine Data Lake Store-Datenquelle mit dem Namen ContosoAdls aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="97ae2-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="97ae2-113">Beispiel 2: Abrufen der Liste der Data Lake Store-Konten in einem Data Lake Analytics-Konto</span><span class="sxs-lookup"><span data-stu-id="97ae2-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="97ae2-114">Dieser Befehl ruft alle Daten Lake Store-Konten aus einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="97ae2-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="97ae2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="97ae2-115">PARAMETERS</span></span>

### <span data-ttu-id="97ae2-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="97ae2-116">-Account</span></span>
<span data-ttu-id="97ae2-117">Gibt das Data Lake Analytics-Konto an, mit dem dieses Cmdlet Datenquellen erhält.</span><span class="sxs-lookup"><span data-stu-id="97ae2-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="97ae2-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="97ae2-118">-Blob</span></span>
<span data-ttu-id="97ae2-119">Gibt den Namen der Azure BLOB-Speicherdaten Quelle an.</span><span class="sxs-lookup"><span data-stu-id="97ae2-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ae2-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="97ae2-120">-DataLakeStore</span></span>
<span data-ttu-id="97ae2-121">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="97ae2-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ae2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ae2-122">-ResourceGroupName</span></span>
<span data-ttu-id="97ae2-123">Gibt den Namen der Ressourcengruppe an, die die Datenquelle enthält.</span><span class="sxs-lookup"><span data-stu-id="97ae2-123">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="97ae2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ae2-124">-DefaultProfile</span></span>
<span data-ttu-id="97ae2-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97ae2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97ae2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ae2-126">CommonParameters</span></span>
<span data-ttu-id="97ae2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ae2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ae2-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ae2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ae2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97ae2-129">INPUTS</span></span>

## <span data-ttu-id="97ae2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97ae2-130">OUTPUTS</span></span>

### <span data-ttu-id="97ae2-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="97ae2-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="97ae2-132">Die angegebenen Azure Storage-Kontodetails.</span><span class="sxs-lookup"><span data-stu-id="97ae2-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="97ae2-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="97ae2-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="97ae2-134">Die Details des angegebenen Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="97ae2-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="97ae2-135">Liste<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="97ae2-135">List<AdlDataSource></span></span>
<span data-ttu-id="97ae2-136">Die Liste der Azure-Speicherkonten und der Data Lake-Speicherkonten im angegebenen Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="97ae2-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="97ae2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="97ae2-137">NOTES</span></span>

## <span data-ttu-id="97ae2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97ae2-138">RELATED LINKS</span></span>

[<span data-ttu-id="97ae2-139">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="97ae2-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="97ae2-140">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="97ae2-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="97ae2-141">Satz-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="97ae2-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


