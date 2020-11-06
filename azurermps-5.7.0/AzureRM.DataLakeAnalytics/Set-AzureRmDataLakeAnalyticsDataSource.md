---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e873a7f4a825ed84172d098dfa0f8cb631cc3f7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482997"
---
# <span data-ttu-id="2b5cc-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2b5cc-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="2b5cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5cc-103">Ändert die Details einer Datenquelle eines Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b5cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b5cc-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b5cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b5cc-105">DESCRIPTION</span></span>
<span data-ttu-id="2b5cc-106">Das Cmdlet " **Satz-AzureRmDataLakeAnalyticsDataSource** " ändert die Details einer Datenquelle eines Azure Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2b5cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b5cc-107">EXAMPLES</span></span>

### <span data-ttu-id="2b5cc-108">Beispiel 1: Ändern der Zugriffstaste für eine Datenquelle</span><span class="sxs-lookup"><span data-stu-id="2b5cc-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="2b5cc-109">Mit diesem Befehl wird die für eine Azure BLOB Storage-Datenquelle gespeicherte Zugriffstaste geändert.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="2b5cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b5cc-110">PARAMETERS</span></span>

### <span data-ttu-id="2b5cc-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="2b5cc-111">-AccessKey</span></span>
<span data-ttu-id="2b5cc-112">Gibt die neue Zugriffstaste der Azure BLOB Storage-Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b5cc-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="2b5cc-113">-Account</span></span>
<span data-ttu-id="2b5cc-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b5cc-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2b5cc-115">-Blob</span></span>
<span data-ttu-id="2b5cc-116">Gibt den Namen der Azure BLOB-Speicherdaten Quelle an.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b5cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5cc-117">-DefaultProfile</span></span>
<span data-ttu-id="2b5cc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2b5cc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b5cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b5cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b5cc-120">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b5cc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5cc-121">CommonParameters</span></span>
<span data-ttu-id="2b5cc-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5cc-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b5cc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5cc-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b5cc-124">INPUTS</span></span>

### <span data-ttu-id="2b5cc-125">Keine</span><span class="sxs-lookup"><span data-stu-id="2b5cc-125">None</span></span>
<span data-ttu-id="2b5cc-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2b5cc-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b5cc-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b5cc-127">OUTPUTS</span></span>

### <span data-ttu-id="2b5cc-128">Keine</span><span class="sxs-lookup"><span data-stu-id="2b5cc-128">None</span></span>

## <span data-ttu-id="2b5cc-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b5cc-129">NOTES</span></span>

## <span data-ttu-id="2b5cc-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b5cc-130">RELATED LINKS</span></span>

[<span data-ttu-id="2b5cc-131">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2b5cc-131">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="2b5cc-132">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="2b5cc-132">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


