---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 202fafead72ec57f3f03460093791943d36a2ba3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475997"
---
# <span data-ttu-id="3b710-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="3b710-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="3b710-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b710-102">SYNOPSIS</span></span>
<span data-ttu-id="3b710-103">Gibt die Ergebnisse einer Abfrage zurück.</span><span class="sxs-lookup"><span data-stu-id="3b710-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b710-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b710-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b710-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b710-105">DESCRIPTION</span></span>
<span data-ttu-id="3b710-106">Das Cmdlet " **Get-AzureRmOperationalInsightsSavedSearchResults** " gibt die Ergebnisse aus der Abfrage zurück, die durch die Such-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b710-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="3b710-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b710-107">EXAMPLES</span></span>

### <span data-ttu-id="3b710-108">Beispiel 1: Abrufen aller Suchergebnisse für eine gespeicherte Suche</span><span class="sxs-lookup"><span data-stu-id="3b710-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="3b710-109">Dieser Befehl ruft alle Suchergebnisse für eine gespeicherte Suche ab.</span><span class="sxs-lookup"><span data-stu-id="3b710-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="3b710-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b710-110">PARAMETERS</span></span>

### <span data-ttu-id="3b710-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b710-111">-DefaultProfile</span></span>
<span data-ttu-id="3b710-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3b710-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b710-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b710-113">-ResourceGroupName</span></span>
<span data-ttu-id="3b710-114">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="3b710-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b710-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3b710-115">-SavedSearchId</span></span>
<span data-ttu-id="3b710-116">Gibt eine gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="3b710-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="3b710-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3b710-117">-WorkspaceName</span></span>
<span data-ttu-id="3b710-118">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="3b710-118">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b710-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b710-119">CommonParameters</span></span>
<span data-ttu-id="3b710-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b710-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b710-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b710-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b710-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b710-122">INPUTS</span></span>

### <span data-ttu-id="3b710-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3b710-123">System.String</span></span>

## <span data-ttu-id="3b710-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b710-124">OUTPUTS</span></span>

### <span data-ttu-id="3b710-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="3b710-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="3b710-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b710-126">NOTES</span></span>

## <span data-ttu-id="3b710-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b710-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b710-128">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="3b710-128">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


