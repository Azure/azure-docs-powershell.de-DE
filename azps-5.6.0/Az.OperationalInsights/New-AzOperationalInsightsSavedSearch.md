---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: cba56fd21263d4accba296cd7aab181f18b09200
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937963"
---
# <span data-ttu-id="36c33-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="36c33-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="36c33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36c33-102">SYNOPSIS</span></span>
<span data-ttu-id="36c33-103">Erstellt eine neue gespeicherte Suche mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="36c33-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="36c33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36c33-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36c33-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36c33-105">DESCRIPTION</span></span>
<span data-ttu-id="36c33-106">Das **Cmdlet New-AzOperationalInsightsSavedSearch** erstellt eine neue gespeicherte Suche mit den angegebenen Parametern für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="36c33-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="36c33-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36c33-107">EXAMPLES</span></span>

### <span data-ttu-id="36c33-108">Beispiel 1: Erstellen einer neuen gespeicherten Suche</span><span class="sxs-lookup"><span data-stu-id="36c33-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="36c33-109">Mit diesem Befehl wird eine neue gespeicherte Suche erstellt.</span><span class="sxs-lookup"><span data-stu-id="36c33-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="36c33-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="36c33-110">PARAMETERS</span></span>

### <span data-ttu-id="36c33-111">-Category</span><span class="sxs-lookup"><span data-stu-id="36c33-111">-Category</span></span>
<span data-ttu-id="36c33-112">Gibt den Kategorienamen an.</span><span class="sxs-lookup"><span data-stu-id="36c33-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="36c33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c33-113">-DefaultProfile</span></span>
<span data-ttu-id="36c33-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="36c33-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36c33-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="36c33-115">-DisplayName</span></span>
<span data-ttu-id="36c33-116">Gibt den namen der gespeicherten Suchanzeige an.</span><span class="sxs-lookup"><span data-stu-id="36c33-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="36c33-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="36c33-117">-Force</span></span>
<span data-ttu-id="36c33-118">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="36c33-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c33-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="36c33-119">-FunctionAlias</span></span>
<span data-ttu-id="36c33-120">Der Funktionsalias, wenn abfrage als Funktion dient.</span><span class="sxs-lookup"><span data-stu-id="36c33-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c33-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="36c33-121">-FunctionParameter</span></span>
<span data-ttu-id="36c33-122">Die optionalen Funktionsparameter, wenn Abfrage als Funktion dient.</span><span class="sxs-lookup"><span data-stu-id="36c33-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="36c33-123">Der Wert sollte das folgende Format haben: "param-name1:type1 = default_value1, param-name2:type2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="36c33-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="36c33-124">Weitere Beispiele und die richtige Syntax finden Sie unter https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="36c33-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c33-125">-Query</span><span class="sxs-lookup"><span data-stu-id="36c33-125">-Query</span></span>
<span data-ttu-id="36c33-126">Gibt den Abfrageausdruck für die gespeicherte Suche an.</span><span class="sxs-lookup"><span data-stu-id="36c33-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="36c33-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c33-127">-ResourceGroupName</span></span>
<span data-ttu-id="36c33-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="36c33-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="36c33-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="36c33-129">-SavedSearchId</span></span>
<span data-ttu-id="36c33-130">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="36c33-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="36c33-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="36c33-131">-Tag</span></span>
<span data-ttu-id="36c33-132">Die gespeicherten Suchtags.</span><span class="sxs-lookup"><span data-stu-id="36c33-132">The saved search tags.</span></span>

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

### <span data-ttu-id="36c33-133">-Version</span><span class="sxs-lookup"><span data-stu-id="36c33-133">-Version</span></span>
<span data-ttu-id="36c33-134">Gibt die Version an.</span><span class="sxs-lookup"><span data-stu-id="36c33-134">Specifies the version.</span></span>

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

### <span data-ttu-id="36c33-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="36c33-135">-WorkspaceName</span></span>
<span data-ttu-id="36c33-136">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="36c33-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="36c33-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36c33-137">-Confirm</span></span>
<span data-ttu-id="36c33-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36c33-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c33-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c33-139">-WhatIf</span></span>
<span data-ttu-id="36c33-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36c33-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36c33-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36c33-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c33-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c33-142">CommonParameters</span></span>
<span data-ttu-id="36c33-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c33-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c33-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36c33-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c33-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36c33-145">INPUTS</span></span>

### <span data-ttu-id="36c33-146">System.String</span><span class="sxs-lookup"><span data-stu-id="36c33-146">System.String</span></span>

### <span data-ttu-id="36c33-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="36c33-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="36c33-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="36c33-148">System.Int64</span></span>

## <span data-ttu-id="36c33-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36c33-149">OUTPUTS</span></span>

### <span data-ttu-id="36c33-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="36c33-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="36c33-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="36c33-151">NOTES</span></span>

## <span data-ttu-id="36c33-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="36c33-152">RELATED LINKS</span></span>

[<span data-ttu-id="36c33-153">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="36c33-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


