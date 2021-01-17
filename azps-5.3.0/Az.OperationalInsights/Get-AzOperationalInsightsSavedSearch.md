---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468819"
---
# <span data-ttu-id="26ecd-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="26ecd-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="26ecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="26ecd-103">Gibt alle gespeicherten Suchbegriffe für einen angegebenen Arbeitsbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="26ecd-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="26ecd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26ecd-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26ecd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26ecd-105">DESCRIPTION</span></span>
<span data-ttu-id="26ecd-106">Das **Cmdlet "Get-AzOperationalInsightsSavedSearch"** gibt alle gespeicherten Suchvorgänge für einen angegebenen Arbeitsbereich innerhalb der angegebenen Ressourcengruppe zurück, wenn Sie keine gespeicherte Such-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="26ecd-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="26ecd-107">Wenn Sie eine gespeicherte Such-ID angeben, wird die gespeicherte Suche zurückgegeben, die dieser ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="26ecd-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="26ecd-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26ecd-108">EXAMPLES</span></span>

### <span data-ttu-id="26ecd-109">Beispiel 1: Alle gespeicherten Suchbegriffe für einen Arbeitsbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="26ecd-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="26ecd-110">Dieser Befehl ruft alle gespeicherten Ressourcen ab, die einem Arbeitsbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26ecd-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="26ecd-111">Beispiel 2: Erhalten einer bestimmten gespeicherten Suche nach ID</span><span class="sxs-lookup"><span data-stu-id="26ecd-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="26ecd-112">Dieser Befehl ruft eine bestimmte gespeicherte Suche mit seiner ID ab.</span><span class="sxs-lookup"><span data-stu-id="26ecd-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="26ecd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26ecd-113">PARAMETERS</span></span>

### <span data-ttu-id="26ecd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ecd-114">-DefaultProfile</span></span>
<span data-ttu-id="26ecd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="26ecd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26ecd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26ecd-116">-ResourceGroupName</span></span>
<span data-ttu-id="26ecd-117">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="26ecd-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="26ecd-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="26ecd-118">-SavedSearchId</span></span>
<span data-ttu-id="26ecd-119">Gibt eine gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="26ecd-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26ecd-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26ecd-120">-WorkspaceName</span></span>
<span data-ttu-id="26ecd-121">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="26ecd-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="26ecd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ecd-122">CommonParameters</span></span>
<span data-ttu-id="26ecd-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26ecd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ecd-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ecd-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ecd-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26ecd-125">INPUTS</span></span>

### <span data-ttu-id="26ecd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="26ecd-126">System.String</span></span>

## <span data-ttu-id="26ecd-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26ecd-127">OUTPUTS</span></span>

### <span data-ttu-id="26ecd-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="26ecd-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="26ecd-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="26ecd-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="26ecd-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26ecd-130">NOTES</span></span>

## <span data-ttu-id="26ecd-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26ecd-131">RELATED LINKS</span></span>

[<span data-ttu-id="26ecd-132">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="26ecd-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


