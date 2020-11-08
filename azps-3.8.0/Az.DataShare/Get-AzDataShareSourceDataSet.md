---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: cda879a29d207a3e71d903c02e20129267124414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995867"
---
# <span data-ttu-id="8461c-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="8461c-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="8461c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8461c-102">SYNOPSIS</span></span>
<span data-ttu-id="8461c-103">Ruft Informationen zu Quelldatensätzen im Share-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8461c-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="8461c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8461c-104">SYNTAX</span></span>

### <span data-ttu-id="8461c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8461c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8461c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8461c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8461c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8461c-107">DESCRIPTION</span></span>
<span data-ttu-id="8461c-108">Das Cmdlet " **Get-AzDataShareSourceDataSet** " enthält Informationen zu den Quelldatensätzen im Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8461c-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="8461c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8461c-109">EXAMPLES</span></span>

### <span data-ttu-id="8461c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8461c-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="8461c-111">Ruft die in der Quell Freigabe verfügbaren Datasets ab.</span><span class="sxs-lookup"><span data-stu-id="8461c-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="8461c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8461c-112">PARAMETERS</span></span>

### <span data-ttu-id="8461c-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="8461c-113">-AccountName</span></span>
<span data-ttu-id="8461c-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="8461c-114">Azure data share account name</span></span>

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

### <span data-ttu-id="8461c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8461c-115">-DefaultProfile</span></span>
<span data-ttu-id="8461c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8461c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8461c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8461c-117">-ResourceGroupName</span></span>
<span data-ttu-id="8461c-118">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="8461c-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8461c-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8461c-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="8461c-120">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="8461c-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8461c-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="8461c-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="8461c-122">Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="8461c-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="8461c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8461c-123">CommonParameters</span></span>
<span data-ttu-id="8461c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8461c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8461c-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8461c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8461c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8461c-126">INPUTS</span></span>

### <span data-ttu-id="8461c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8461c-127">System.String</span></span>

## <span data-ttu-id="8461c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8461c-128">OUTPUTS</span></span>

### <span data-ttu-id="8461c-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="8461c-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="8461c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="8461c-130">NOTES</span></span>

## <span data-ttu-id="8461c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8461c-131">RELATED LINKS</span></span>
