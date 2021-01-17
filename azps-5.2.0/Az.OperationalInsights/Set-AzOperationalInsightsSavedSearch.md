---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372069"
---
# <span data-ttu-id="508d7-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="508d7-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="508d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="508d7-102">SYNOPSIS</span></span>
<span data-ttu-id="508d7-103">Aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="508d7-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="508d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="508d7-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="508d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="508d7-105">DESCRIPTION</span></span>
<span data-ttu-id="508d7-106">Das **Cmdlet "Set-AzOperationalInsightsSavedSearch"** aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="508d7-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="508d7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="508d7-107">EXAMPLES</span></span>

### <span data-ttu-id="508d7-108">Beispiel 1: Festlegen einer gespeicherten Suche mit aktualisierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="508d7-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="508d7-109">Mit diesem Befehl wird eine gespeicherte Suche mit aktualisierten Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="508d7-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="508d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="508d7-110">PARAMETERS</span></span>

### <span data-ttu-id="508d7-111">-Category</span><span class="sxs-lookup"><span data-stu-id="508d7-111">-Category</span></span>
<span data-ttu-id="508d7-112">Gibt den Kategorienamen an.</span><span class="sxs-lookup"><span data-stu-id="508d7-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="508d7-113">-DefaultProfile</span></span>
<span data-ttu-id="508d7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="508d7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="508d7-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="508d7-115">-DisplayName</span></span>
<span data-ttu-id="508d7-116">Gibt den Anzeigenamen an.</span><span class="sxs-lookup"><span data-stu-id="508d7-116">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="508d7-117">-ETag</span></span>
<span data-ttu-id="508d7-118">Gibt den #A0 an.</span><span class="sxs-lookup"><span data-stu-id="508d7-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="508d7-119">-FunctionAlias</span></span>
<span data-ttu-id="508d7-120">Der Funktionsalias, wenn die Abfrage als Funktion dient.</span><span class="sxs-lookup"><span data-stu-id="508d7-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="508d7-121">-FunctionParameter</span></span>
<span data-ttu-id="508d7-122">Die optionalen Funktionsparameter, wenn die Abfrage als Funktion dient.</span><span class="sxs-lookup"><span data-stu-id="508d7-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="508d7-123">Der Wert sollte das folgende Format haben: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span><span class="sxs-lookup"><span data-stu-id="508d7-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="508d7-124">Weitere Beispiele und die richtige Syntax finden Sie unter https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="508d7-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-125">-Query</span><span class="sxs-lookup"><span data-stu-id="508d7-125">-Query</span></span>
<span data-ttu-id="508d7-126">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="508d7-126">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="508d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="508d7-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="508d7-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="508d7-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="508d7-129">-SavedSearchId</span></span>
<span data-ttu-id="508d7-130">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="508d7-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="508d7-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="508d7-131">-Tag</span></span>
<span data-ttu-id="508d7-132">Die gespeicherten Suchtags.</span><span class="sxs-lookup"><span data-stu-id="508d7-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-133">-Version</span><span class="sxs-lookup"><span data-stu-id="508d7-133">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="508d7-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="508d7-134">-WorkspaceName</span></span>
<span data-ttu-id="508d7-135">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="508d7-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="508d7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="508d7-136">CommonParameters</span></span>
<span data-ttu-id="508d7-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="508d7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="508d7-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="508d7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="508d7-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="508d7-139">INPUTS</span></span>

### <span data-ttu-id="508d7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="508d7-140">System.String</span></span>

### <span data-ttu-id="508d7-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="508d7-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="508d7-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="508d7-142">System.Int64</span></span>

## <span data-ttu-id="508d7-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="508d7-143">OUTPUTS</span></span>

### <span data-ttu-id="508d7-144">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="508d7-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="508d7-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="508d7-145">NOTES</span></span>

## <span data-ttu-id="508d7-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="508d7-146">RELATED LINKS</span></span>

[<span data-ttu-id="508d7-147">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="508d7-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


