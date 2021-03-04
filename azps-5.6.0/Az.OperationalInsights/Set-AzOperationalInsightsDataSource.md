---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4156bc414105d6d104e8315d83f92f0fb6e19ab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937872"
---
# <span data-ttu-id="9dd73-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9dd73-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="9dd73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd73-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd73-103">Aktualisiert eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="9dd73-103">Updates a data source.</span></span>

## <span data-ttu-id="9dd73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dd73-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9dd73-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dd73-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd73-106">Das **Cmdlet Set-AzOperationalInsightsDataSource aktualisiert** eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="9dd73-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="9dd73-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9dd73-107">EXAMPLES</span></span>

## <span data-ttu-id="9dd73-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9dd73-108">PARAMETERS</span></span>

### <span data-ttu-id="9dd73-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="9dd73-109">-DataSource</span></span>
<span data-ttu-id="9dd73-110">Gibt die Datenquelle an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9dd73-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd73-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd73-111">-DefaultProfile</span></span>
<span data-ttu-id="9dd73-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9dd73-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dd73-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd73-113">CommonParameters</span></span>
<span data-ttu-id="9dd73-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd73-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd73-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd73-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd73-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9dd73-116">INPUTS</span></span>

### <span data-ttu-id="9dd73-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9dd73-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9dd73-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9dd73-118">OUTPUTS</span></span>

### <span data-ttu-id="9dd73-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9dd73-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9dd73-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9dd73-120">NOTES</span></span>
* <span data-ttu-id="9dd73-121">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="9dd73-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9dd73-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9dd73-122">RELATED LINKS</span></span>

[<span data-ttu-id="9dd73-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9dd73-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="9dd73-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9dd73-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


