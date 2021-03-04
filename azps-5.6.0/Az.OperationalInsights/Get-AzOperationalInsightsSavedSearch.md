---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921664"
---
# <span data-ttu-id="47222-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="47222-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="47222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47222-102">SYNOPSIS</span></span>
<span data-ttu-id="47222-103">Gibt alle gespeicherten Suchbegriffe für einen angegebenen Arbeitsbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="47222-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="47222-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47222-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47222-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47222-105">DESCRIPTION</span></span>
<span data-ttu-id="47222-106">Das **Get-AzOperationalInsightsSavedSearch-Cmdlet** gibt alle gespeicherten Suchvorgänge für einen angegebenen Arbeitsbereich innerhalb der Ressourcengruppe zurück, die angegeben sind, wenn Sie keine gespeicherte Such-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="47222-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="47222-107">Wenn Sie eine gespeicherte Such-ID angeben, wird die gespeicherte Suche zurückgegeben, die dieser ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="47222-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="47222-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47222-108">EXAMPLES</span></span>

### <span data-ttu-id="47222-109">Beispiel 1: Alle gespeicherten Suchbegriffe für einen Arbeitsbereich erhalten</span><span class="sxs-lookup"><span data-stu-id="47222-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="47222-110">Dieser Befehl ruft alle gespeicherten Ressourcen ab, die einem Arbeitsbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="47222-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="47222-111">Beispiel 2: Erhalten einer bestimmten gespeicherten Suche nach ID</span><span class="sxs-lookup"><span data-stu-id="47222-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="47222-112">Dieser Befehl ruft eine bestimmte gespeicherte Suche nach seiner ID ab.</span><span class="sxs-lookup"><span data-stu-id="47222-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="47222-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="47222-113">PARAMETERS</span></span>

### <span data-ttu-id="47222-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47222-114">-DefaultProfile</span></span>
<span data-ttu-id="47222-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="47222-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47222-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47222-116">-ResourceGroupName</span></span>
<span data-ttu-id="47222-117">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="47222-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="47222-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="47222-118">-SavedSearchId</span></span>
<span data-ttu-id="47222-119">Gibt eine gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="47222-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="47222-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47222-120">-WorkspaceName</span></span>
<span data-ttu-id="47222-121">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="47222-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="47222-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47222-122">CommonParameters</span></span>
<span data-ttu-id="47222-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47222-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47222-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47222-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47222-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47222-125">INPUTS</span></span>

### <span data-ttu-id="47222-126">System.String</span><span class="sxs-lookup"><span data-stu-id="47222-126">System.String</span></span>

## <span data-ttu-id="47222-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47222-127">OUTPUTS</span></span>

### <span data-ttu-id="47222-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="47222-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="47222-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="47222-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="47222-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="47222-130">NOTES</span></span>

## <span data-ttu-id="47222-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="47222-131">RELATED LINKS</span></span>

[<span data-ttu-id="47222-132">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="47222-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


