---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151289"
---
# <span data-ttu-id="a68e0-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a68e0-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="a68e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a68e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a68e0-103">Aktualisiert eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="a68e0-103">Updates a data source.</span></span>

## <span data-ttu-id="a68e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a68e0-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a68e0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a68e0-105">DESCRIPTION</span></span>
<span data-ttu-id="a68e0-106">Das **Cmdlet "Set-AzOperationalInsightsDataSource"** aktualisiert eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="a68e0-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="a68e0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a68e0-107">EXAMPLES</span></span>

## <span data-ttu-id="a68e0-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a68e0-108">PARAMETERS</span></span>

### <span data-ttu-id="a68e0-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="a68e0-109">-DataSource</span></span>
<span data-ttu-id="a68e0-110">Gibt die Datenquelle an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a68e0-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a68e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68e0-111">-DefaultProfile</span></span>
<span data-ttu-id="a68e0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a68e0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a68e0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68e0-113">CommonParameters</span></span>
<span data-ttu-id="a68e0-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a68e0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68e0-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68e0-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68e0-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a68e0-116">INPUTS</span></span>

### <span data-ttu-id="a68e0-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a68e0-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a68e0-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a68e0-118">OUTPUTS</span></span>

### <span data-ttu-id="a68e0-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a68e0-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a68e0-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a68e0-120">NOTES</span></span>
* <span data-ttu-id="a68e0-121">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="a68e0-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a68e0-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a68e0-122">RELATED LINKS</span></span>

[<span data-ttu-id="a68e0-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a68e0-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="a68e0-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a68e0-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


