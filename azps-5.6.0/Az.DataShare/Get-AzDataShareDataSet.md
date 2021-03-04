---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: d0bf60bbfd13474270391afd6f01bc9ec8130b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938811"
---
# <span data-ttu-id="acd2c-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="acd2c-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="acd2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="acd2c-103">Ruft Informationen zu Datensätzen in azureer Datenfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="acd2c-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="acd2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acd2c-104">SYNTAX</span></span>

### <span data-ttu-id="acd2c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="acd2c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acd2c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd2c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd2c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acd2c-107">DESCRIPTION</span></span>
<span data-ttu-id="acd2c-108">Das **Get-AzDataShareDataSet-Cmdlet** ruft Informationen zu Datensätzen ab, die in einer Freigabe in einem Azure-Datenfreigabekonto hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="acd2c-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="acd2c-109">Wenn Sie den Namen des Datensets angeben, ruft dieses Cmdlet Informationen zum Datenset ab.</span><span class="sxs-lookup"><span data-stu-id="acd2c-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="acd2c-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datensätzen in einer Freigabe ab. I</span><span class="sxs-lookup"><span data-stu-id="acd2c-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="acd2c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="acd2c-111">EXAMPLES</span></span>

### <span data-ttu-id="acd2c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="acd2c-112">Example 1</span></span>
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

<span data-ttu-id="acd2c-113">Mit diesem Befehl werden Informationen zum Datenset AdsDataSet in Share AdsShare im Azure-Datenfreigabekonto WikiAdsAccount und der Ressourcengruppe ADS angezeigt.</span><span class="sxs-lookup"><span data-stu-id="acd2c-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="acd2c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="acd2c-114">PARAMETERS</span></span>

### <span data-ttu-id="acd2c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="acd2c-115">-AccountName</span></span>
<span data-ttu-id="acd2c-116">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="acd2c-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="acd2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd2c-117">-DefaultProfile</span></span>
<span data-ttu-id="acd2c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="acd2c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd2c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="acd2c-119">-Name</span></span>
<span data-ttu-id="acd2c-120">Name des Azure-Datenspeichers.</span><span class="sxs-lookup"><span data-stu-id="acd2c-120">Azure data set name.</span></span>

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

### <span data-ttu-id="acd2c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd2c-121">-ResourceGroupName</span></span>
<span data-ttu-id="acd2c-122">Der Ressourcengruppenname des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="acd2c-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="acd2c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acd2c-123">-ResourceId</span></span>
<span data-ttu-id="acd2c-124">Die Ressourcen-ID des Azure-Datensets.</span><span class="sxs-lookup"><span data-stu-id="acd2c-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="acd2c-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="acd2c-125">-ShareName</span></span>
<span data-ttu-id="acd2c-126">Azure-Datenfreigabename.</span><span class="sxs-lookup"><span data-stu-id="acd2c-126">Azure data share name.</span></span>

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

### <span data-ttu-id="acd2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd2c-127">CommonParameters</span></span>
<span data-ttu-id="acd2c-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd2c-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acd2c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd2c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="acd2c-130">INPUTS</span></span>

### <span data-ttu-id="acd2c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="acd2c-131">System.String</span></span>

## <span data-ttu-id="acd2c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="acd2c-132">OUTPUTS</span></span>

### <span data-ttu-id="acd2c-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="acd2c-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="acd2c-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="acd2c-134">NOTES</span></span>

## <span data-ttu-id="acd2c-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="acd2c-135">RELATED LINKS</span></span>
