---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660044"
---
# <span data-ttu-id="d4982-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d4982-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="d4982-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4982-102">SYNOPSIS</span></span>
<span data-ttu-id="d4982-103">Aktualisiert eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="d4982-103">Updates a data source.</span></span>

## <span data-ttu-id="d4982-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4982-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4982-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4982-105">DESCRIPTION</span></span>
<span data-ttu-id="d4982-106">Das Cmdlet " **Satz-AzOperationalInsightsDataSource** " aktualisiert eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="d4982-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="d4982-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4982-107">EXAMPLES</span></span>

## <span data-ttu-id="d4982-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4982-108">PARAMETERS</span></span>

### <span data-ttu-id="d4982-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="d4982-109">-DataSource</span></span>
<span data-ttu-id="d4982-110">Gibt die Datenquelle an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d4982-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="d4982-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4982-111">-DefaultProfile</span></span>
<span data-ttu-id="d4982-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d4982-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4982-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4982-113">CommonParameters</span></span>
<span data-ttu-id="d4982-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4982-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4982-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4982-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4982-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4982-116">INPUTS</span></span>

### <span data-ttu-id="d4982-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d4982-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d4982-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4982-118">OUTPUTS</span></span>

### <span data-ttu-id="d4982-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d4982-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d4982-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4982-120">NOTES</span></span>
* <span data-ttu-id="d4982-121">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="d4982-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d4982-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4982-122">RELATED LINKS</span></span>

[<span data-ttu-id="d4982-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d4982-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="d4982-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d4982-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


