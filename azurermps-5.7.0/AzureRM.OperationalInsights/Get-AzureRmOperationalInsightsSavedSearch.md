---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481069"
---
# <span data-ttu-id="a5a87-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a5a87-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="a5a87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5a87-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a87-103">Gibt alle gespeicherten Suchvorgänge für einen angegebenen Arbeitsbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="a5a87-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5a87-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a87-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5a87-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a87-106">Das Cmdlet " **Get-AzureRmOperationalInsightsSavedSearch** " gibt alle gespeicherten Suchen nach einem angegebenen Arbeitsbereich innerhalb der angegebenen Ressourcengruppe zurück, wenn Sie keine gespeicherte Such-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="a5a87-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="a5a87-107">Wenn Sie eine gespeicherte Such-ID angeben, wird die gespeicherte Suche, die dieser ID entspricht, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5a87-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="a5a87-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5a87-108">EXAMPLES</span></span>

### <span data-ttu-id="a5a87-109">Beispiel 1: Abrufen aller gespeicherten Suchvorgänge für einen Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a5a87-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="a5a87-110">Dieser Befehl ruft alle gespeicherten Ressourcen ab, die einem Arbeitsbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a5a87-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="a5a87-111">Beispiel 2: Abrufen einer bestimmten gespeicherten Suche nach ID</span><span class="sxs-lookup"><span data-stu-id="a5a87-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="a5a87-112">Mit diesem Befehl wird eine bestimmte gespeicherte Suche anhand der ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5a87-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="a5a87-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5a87-113">PARAMETERS</span></span>

### <span data-ttu-id="a5a87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a87-114">-DefaultProfile</span></span>
<span data-ttu-id="a5a87-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a5a87-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a87-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a87-116">-ResourceGroupName</span></span>
<span data-ttu-id="a5a87-117">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="a5a87-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a87-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="a5a87-118">-SavedSearchId</span></span>
<span data-ttu-id="a5a87-119">Gibt eine gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="a5a87-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a87-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5a87-120">-WorkspaceName</span></span>
<span data-ttu-id="a5a87-121">Gibt einen Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="a5a87-121">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a87-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a87-122">CommonParameters</span></span>
<span data-ttu-id="a5a87-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a87-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a87-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a87-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a87-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5a87-125">INPUTS</span></span>

### <span data-ttu-id="a5a87-126">Keine</span><span class="sxs-lookup"><span data-stu-id="a5a87-126">None</span></span>
<span data-ttu-id="a5a87-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a5a87-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5a87-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5a87-128">OUTPUTS</span></span>

### <span data-ttu-id="a5a87-129">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="a5a87-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="a5a87-130">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="a5a87-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="a5a87-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5a87-131">NOTES</span></span>

## <span data-ttu-id="a5a87-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5a87-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5a87-133">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="a5a87-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


