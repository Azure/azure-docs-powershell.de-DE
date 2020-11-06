---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8aae62ccbf79f2b3c59f6009aa5233daf00853fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499601"
---
# <span data-ttu-id="afea0-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="afea0-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="afea0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afea0-102">SYNOPSIS</span></span>
<span data-ttu-id="afea0-103">Ändert die Details einer Datenquelle eines Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="afea0-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afea0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afea0-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afea0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afea0-105">DESCRIPTION</span></span>
<span data-ttu-id="afea0-106">Das Cmdlet " **Satz-AzureRmDataLakeAnalyticsDataSource** " ändert die Details einer Datenquelle eines Azure Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="afea0-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="afea0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afea0-107">EXAMPLES</span></span>

### <span data-ttu-id="afea0-108">Beispiel 1: Ändern der Zugriffstaste für eine Datenquelle</span><span class="sxs-lookup"><span data-stu-id="afea0-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="afea0-109">Mit diesem Befehl wird die für eine Azure BLOB Storage-Datenquelle gespeicherte Zugriffstaste geändert.</span><span class="sxs-lookup"><span data-stu-id="afea0-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="afea0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="afea0-110">PARAMETERS</span></span>

### <span data-ttu-id="afea0-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="afea0-111">-AccessKey</span></span>
<span data-ttu-id="afea0-112">Gibt die neue Zugriffstaste der Azure BLOB Storage-Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="afea0-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afea0-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="afea0-113">-Account</span></span>
<span data-ttu-id="afea0-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="afea0-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="afea0-115">-BLOB</span><span class="sxs-lookup"><span data-stu-id="afea0-115">-Blob</span></span>
<span data-ttu-id="afea0-116">Gibt den Namen der Azure BLOB-Speicherdaten Quelle an.</span><span class="sxs-lookup"><span data-stu-id="afea0-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afea0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afea0-117">-DefaultProfile</span></span>
<span data-ttu-id="afea0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="afea0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afea0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afea0-119">-ResourceGroupName</span></span>
<span data-ttu-id="afea0-120">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="afea0-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="afea0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afea0-121">CommonParameters</span></span>
<span data-ttu-id="afea0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afea0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afea0-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afea0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afea0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afea0-124">INPUTS</span></span>

### <span data-ttu-id="afea0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="afea0-125">System.String</span></span>

## <span data-ttu-id="afea0-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afea0-126">OUTPUTS</span></span>

### <span data-ttu-id="afea0-127">System. void</span><span class="sxs-lookup"><span data-stu-id="afea0-127">System.Void</span></span>

## <span data-ttu-id="afea0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="afea0-128">NOTES</span></span>

## <span data-ttu-id="afea0-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afea0-129">RELATED LINKS</span></span>

[<span data-ttu-id="afea0-130">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="afea0-130">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="afea0-131">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="afea0-131">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


