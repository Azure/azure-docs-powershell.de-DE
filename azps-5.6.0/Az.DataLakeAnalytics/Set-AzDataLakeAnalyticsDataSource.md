---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: cb51b1c703d527a2888bd0e80d8cc7a50d044e36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923800"
---
# <span data-ttu-id="69519-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="69519-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="69519-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69519-102">SYNOPSIS</span></span>
<span data-ttu-id="69519-103">Ändert die Details einer Datenquelle eines Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="69519-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="69519-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69519-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69519-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69519-105">DESCRIPTION</span></span>
<span data-ttu-id="69519-106">Das **Cmdlet Set-AzDataLakeAnalyticsDataSource** ändert die Details einer Datenquelle eines Azure Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="69519-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="69519-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69519-107">EXAMPLES</span></span>

### <span data-ttu-id="69519-108">Beispiel 1: Ändern des Zugriffsschlüssels für eine Datenquelle</span><span class="sxs-lookup"><span data-stu-id="69519-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="69519-109">Mit diesem Befehl wird der Zugriffsschlüssel geändert, der für eine Azure Blob Storage-Datenquelle gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="69519-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="69519-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="69519-110">PARAMETERS</span></span>

### <span data-ttu-id="69519-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="69519-111">-AccessKey</span></span>
<span data-ttu-id="69519-112">Gibt den neuen Zugriffsschlüssel der Azure Blob Storage-Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="69519-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="69519-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="69519-113">-Account</span></span>
<span data-ttu-id="69519-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="69519-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="69519-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="69519-115">-Blob</span></span>
<span data-ttu-id="69519-116">Gibt den Namen der Azure Blob Storage-Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="69519-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="69519-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69519-117">-DefaultProfile</span></span>
<span data-ttu-id="69519-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="69519-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69519-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69519-119">-ResourceGroupName</span></span>
<span data-ttu-id="69519-120">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="69519-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="69519-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69519-121">CommonParameters</span></span>
<span data-ttu-id="69519-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69519-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69519-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69519-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69519-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69519-124">INPUTS</span></span>

### <span data-ttu-id="69519-125">System.String</span><span class="sxs-lookup"><span data-stu-id="69519-125">System.String</span></span>

## <span data-ttu-id="69519-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69519-126">OUTPUTS</span></span>

### <span data-ttu-id="69519-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="69519-127">System.Void</span></span>

## <span data-ttu-id="69519-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="69519-128">NOTES</span></span>

## <span data-ttu-id="69519-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="69519-129">RELATED LINKS</span></span>

[<span data-ttu-id="69519-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="69519-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="69519-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="69519-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


