---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144289"
---
# <span data-ttu-id="ef171-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ef171-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="ef171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef171-102">SYNOPSIS</span></span>
<span data-ttu-id="ef171-103">Ruft Informationen zu Datensätzen in der Azure-Datenfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="ef171-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="ef171-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef171-104">SYNTAX</span></span>

### <span data-ttu-id="ef171-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef171-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef171-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef171-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef171-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef171-107">DESCRIPTION</span></span>
<span data-ttu-id="ef171-108">Das **Cmdlet "Get-AzDataShareDataSet"** ruft Informationen zu Datensätzen ab, die bei einer Freigabe in einem Azure-Datenfreigabekonto hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="ef171-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="ef171-109">Wenn Sie den Namen des Datensets angeben, ruft dieses Cmdlet Informationen über das Datenset ab.</span><span class="sxs-lookup"><span data-stu-id="ef171-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="ef171-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datensätzen in einer Freigabe ab. I</span><span class="sxs-lookup"><span data-stu-id="ef171-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="ef171-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef171-111">EXAMPLES</span></span>

### <span data-ttu-id="ef171-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef171-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="ef171-113">Dieser Befehl zeigt Informationen zum Dataset AdsDataSet in "AdsShare teilen" im WikiAdsAccount des Azure-Datenfreigabekontos und der Ressourcengruppe ADS an.</span><span class="sxs-lookup"><span data-stu-id="ef171-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="ef171-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef171-114">PARAMETERS</span></span>

### <span data-ttu-id="ef171-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef171-115">-AccountName</span></span>
<span data-ttu-id="ef171-116">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="ef171-116">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef171-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef171-117">-DefaultProfile</span></span>
<span data-ttu-id="ef171-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef171-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef171-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ef171-119">-Name</span></span>
<span data-ttu-id="ef171-120">Name des Azure-Datensets.</span><span class="sxs-lookup"><span data-stu-id="ef171-120">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef171-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef171-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef171-122">Der Ressourcengruppenname des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="ef171-122">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef171-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef171-123">-ResourceId</span></span>
<span data-ttu-id="ef171-124">Die Ressourcen-ID des Azure-Datensets.</span><span class="sxs-lookup"><span data-stu-id="ef171-124">The resource id of the azure data set.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef171-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ef171-125">-ShareName</span></span>
<span data-ttu-id="ef171-126">Name der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="ef171-126">Azure data share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef171-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef171-127">CommonParameters</span></span>
<span data-ttu-id="ef171-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef171-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef171-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef171-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef171-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef171-130">INPUTS</span></span>

### <span data-ttu-id="ef171-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ef171-131">System.String</span></span>

## <span data-ttu-id="ef171-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef171-132">OUTPUTS</span></span>

### <span data-ttu-id="ef171-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ef171-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="ef171-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef171-134">NOTES</span></span>

## <span data-ttu-id="ef171-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef171-135">RELATED LINKS</span></span>
