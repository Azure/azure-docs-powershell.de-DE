---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 25d973d6a568695fbca7371b229cf9bb18fcd5cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937856"
---
# <span data-ttu-id="67951-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="67951-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="67951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67951-102">SYNOPSIS</span></span>
<span data-ttu-id="67951-103">Aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="67951-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="67951-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67951-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67951-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67951-105">DESCRIPTION</span></span>
<span data-ttu-id="67951-106">Das **Cmdlet Set-AzOperationalInsightsSavedSearch** aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="67951-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="67951-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67951-107">EXAMPLES</span></span>

### <span data-ttu-id="67951-108">Beispiel 1: Festlegen einer gespeicherten Suche mit aktualisierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="67951-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="67951-109">Mit diesem Befehl wird eine gespeicherte Suche mit aktualisierten Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="67951-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="67951-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="67951-110">PARAMETERS</span></span>

### <span data-ttu-id="67951-111">-Category</span><span class="sxs-lookup"><span data-stu-id="67951-111">-Category</span></span>
<span data-ttu-id="67951-112">Gibt den Kategorienamen an.</span><span class="sxs-lookup"><span data-stu-id="67951-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="67951-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67951-113">-DefaultProfile</span></span>
<span data-ttu-id="67951-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="67951-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67951-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="67951-115">-DisplayName</span></span>
<span data-ttu-id="67951-116">Gibt den Anzeigenamen an.</span><span class="sxs-lookup"><span data-stu-id="67951-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="67951-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="67951-117">-ETag</span></span>
<span data-ttu-id="67951-118">Gibt den Namen des ETags an.</span><span class="sxs-lookup"><span data-stu-id="67951-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="67951-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="67951-119">-FunctionAlias</span></span>
<span data-ttu-id="67951-120">Der Funktionsalias, wenn abfrage als Funktion dient.</span><span class="sxs-lookup"><span data-stu-id="67951-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="67951-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="67951-121">-FunctionParameter</span></span>
<span data-ttu-id="67951-122">Die optionalen Funktionsparameter, wenn Abfrage als Funktion dient.</span><span class="sxs-lookup"><span data-stu-id="67951-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="67951-123">Der Wert sollte das folgende Format haben: "param-name1:type1 = default_value1, param-name2:type2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="67951-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="67951-124">Weitere Beispiele und die richtige Syntax finden Sie unter https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="67951-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="67951-125">-Query</span><span class="sxs-lookup"><span data-stu-id="67951-125">-Query</span></span>
<span data-ttu-id="67951-126">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="67951-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="67951-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67951-127">-ResourceGroupName</span></span>
<span data-ttu-id="67951-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="67951-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="67951-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="67951-129">-SavedSearchId</span></span>
<span data-ttu-id="67951-130">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="67951-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="67951-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="67951-131">-Tag</span></span>
<span data-ttu-id="67951-132">Die gespeicherten Suchtags.</span><span class="sxs-lookup"><span data-stu-id="67951-132">The saved search tags.</span></span>

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

### <span data-ttu-id="67951-133">-Version</span><span class="sxs-lookup"><span data-stu-id="67951-133">-Version</span></span>
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

### <span data-ttu-id="67951-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67951-134">-WorkspaceName</span></span>
<span data-ttu-id="67951-135">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="67951-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="67951-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67951-136">CommonParameters</span></span>
<span data-ttu-id="67951-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67951-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67951-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67951-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67951-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67951-139">INPUTS</span></span>

### <span data-ttu-id="67951-140">System.String</span><span class="sxs-lookup"><span data-stu-id="67951-140">System.String</span></span>

### <span data-ttu-id="67951-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="67951-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="67951-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="67951-142">System.Int64</span></span>

## <span data-ttu-id="67951-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67951-143">OUTPUTS</span></span>

### <span data-ttu-id="67951-144">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="67951-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="67951-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="67951-145">NOTES</span></span>

## <span data-ttu-id="67951-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="67951-146">RELATED LINKS</span></span>

[<span data-ttu-id="67951-147">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="67951-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


