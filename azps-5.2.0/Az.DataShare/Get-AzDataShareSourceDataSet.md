---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357635"
---
# <span data-ttu-id="d0bb6-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="d0bb6-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="d0bb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bb6-103">Ruft Informationen zu Quelldatensets im Freigabeabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="d0bb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0bb6-104">SYNTAX</span></span>

### <span data-ttu-id="d0bb6-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0bb6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0bb6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bb6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0bb6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0bb6-107">DESCRIPTION</span></span>
<span data-ttu-id="d0bb6-108">Das **Cmdlet "Get-AzDataShareSourceDataSet"** enthält Informationen zu den Quelldatensets im Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="d0bb6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0bb6-109">EXAMPLES</span></span>

### <span data-ttu-id="d0bb6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0bb6-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="d0bb6-111">Ruft Datasets ab, die in der Quellfreigabe verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="d0bb6-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="d0bb6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0bb6-112">PARAMETERS</span></span>

### <span data-ttu-id="d0bb6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0bb6-113">-AccountName</span></span>
<span data-ttu-id="d0bb6-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="d0bb6-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d0bb6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0bb6-115">-DefaultProfile</span></span>
<span data-ttu-id="d0bb6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0bb6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0bb6-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0bb6-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="d0bb6-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d0bb6-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d0bb6-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="d0bb6-120">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="d0bb6-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d0bb6-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="d0bb6-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="d0bb6-122">Ressourcen-ID des Azure-Datenfreigabeabonnements</span><span class="sxs-lookup"><span data-stu-id="d0bb6-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="d0bb6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bb6-123">CommonParameters</span></span>
<span data-ttu-id="d0bb6-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0bb6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bb6-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0bb6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bb6-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0bb6-126">INPUTS</span></span>

### <span data-ttu-id="d0bb6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d0bb6-127">System.String</span></span>

## <span data-ttu-id="d0bb6-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0bb6-128">OUTPUTS</span></span>

### <span data-ttu-id="d0bb6-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="d0bb6-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="d0bb6-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0bb6-130">NOTES</span></span>

## <span data-ttu-id="d0bb6-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0bb6-131">RELATED LINKS</span></span>
