---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 13d8be80411e39124ab29d9a31e44edd0ebd95e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479009"
---
# <span data-ttu-id="06296-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="06296-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="06296-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06296-102">SYNOPSIS</span></span>
<span data-ttu-id="06296-103">Aktualisiert eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="06296-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06296-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06296-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06296-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06296-105">DESCRIPTION</span></span>
<span data-ttu-id="06296-106">Das Cmdlet " **Satz-AzureRmOperationalInsightsDataSource** " aktualisiert eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="06296-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="06296-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06296-107">EXAMPLES</span></span>

## <span data-ttu-id="06296-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="06296-108">PARAMETERS</span></span>

### <span data-ttu-id="06296-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="06296-109">-DataSource</span></span>
<span data-ttu-id="06296-110">Gibt die Datenquelle an, die von diesem Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="06296-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="06296-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06296-111">-DefaultProfile</span></span>
<span data-ttu-id="06296-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06296-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06296-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06296-113">CommonParameters</span></span>
<span data-ttu-id="06296-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06296-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06296-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06296-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06296-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06296-116">INPUTS</span></span>

### <span data-ttu-id="06296-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="06296-117">PSDataSource</span></span>
<span data-ttu-id="06296-118">Der Parameter "DataSource" akzeptiert den Wert vom Typ "PSDataSource" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="06296-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="06296-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06296-119">OUTPUTS</span></span>

### <span data-ttu-id="06296-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="06296-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="06296-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="06296-121">NOTES</span></span>
* <span data-ttu-id="06296-122">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="06296-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="06296-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06296-123">RELATED LINKS</span></span>

[<span data-ttu-id="06296-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="06296-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="06296-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="06296-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


