---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009622"
---
# <span data-ttu-id="d672e-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="d672e-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="d672e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d672e-102">SYNOPSIS</span></span>
<span data-ttu-id="d672e-103">Erstellt eine neue gespeicherte Suche mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="d672e-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="d672e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d672e-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d672e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d672e-105">DESCRIPTION</span></span>
<span data-ttu-id="d672e-106">Das Cmdlet **New-AzOperationalInsightsSavedSearch** erstellt eine neue gespeicherte Suche mit den angegebenen Parametern für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="d672e-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="d672e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d672e-107">EXAMPLES</span></span>

### <span data-ttu-id="d672e-108">Beispiel 1: Erstellen einer neuen gespeicherten Suche</span><span class="sxs-lookup"><span data-stu-id="d672e-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="d672e-109">Dieser Befehl erstellt eine neue gespeicherte Suche.</span><span class="sxs-lookup"><span data-stu-id="d672e-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="d672e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d672e-110">PARAMETERS</span></span>

### <span data-ttu-id="d672e-111">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="d672e-111">-Category</span></span>
<span data-ttu-id="d672e-112">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="d672e-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="d672e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d672e-113">-DefaultProfile</span></span>
<span data-ttu-id="d672e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d672e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d672e-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d672e-115">-DisplayName</span></span>
<span data-ttu-id="d672e-116">Gibt den Namen der gespeicherten Suchanzeige an.</span><span class="sxs-lookup"><span data-stu-id="d672e-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="d672e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d672e-117">-Force</span></span>
<span data-ttu-id="d672e-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d672e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d672e-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="d672e-119">-FunctionAlias</span></span>
<span data-ttu-id="d672e-120">Der Funktions-Alias, wenn Query als Funktion fungiert.</span><span class="sxs-lookup"><span data-stu-id="d672e-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="d672e-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="d672e-121">-FunctionParameter</span></span>
<span data-ttu-id="d672e-122">Die optionalen Funktionsparameter, wenn Query als Funktion fungiert.</span><span class="sxs-lookup"><span data-stu-id="d672e-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="d672e-123">Der Wert sollte das folgende Format aufweisen: ' param-Name1: default_value1, param-Name2: Typ2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="d672e-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="d672e-124">Weitere Beispiele und die richtige Syntax finden Sie unter https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="d672e-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="d672e-125">-Query</span><span class="sxs-lookup"><span data-stu-id="d672e-125">-Query</span></span>
<span data-ttu-id="d672e-126">Gibt den Abfrageausdruck für die gespeicherte Suche an.</span><span class="sxs-lookup"><span data-stu-id="d672e-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="d672e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d672e-127">-ResourceGroupName</span></span>
<span data-ttu-id="d672e-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d672e-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="d672e-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d672e-129">-SavedSearchId</span></span>
<span data-ttu-id="d672e-130">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="d672e-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="d672e-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d672e-131">-Tag</span></span>
<span data-ttu-id="d672e-132">Die gespeicherten Suchkategorien.</span><span class="sxs-lookup"><span data-stu-id="d672e-132">The saved search tags.</span></span>

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

### <span data-ttu-id="d672e-133">-Version</span><span class="sxs-lookup"><span data-stu-id="d672e-133">-Version</span></span>
<span data-ttu-id="d672e-134">Gibt die Version an.</span><span class="sxs-lookup"><span data-stu-id="d672e-134">Specifies the version.</span></span>

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

### <span data-ttu-id="d672e-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d672e-135">-WorkspaceName</span></span>
<span data-ttu-id="d672e-136">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="d672e-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="d672e-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d672e-137">-Confirm</span></span>
<span data-ttu-id="d672e-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d672e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d672e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d672e-139">-WhatIf</span></span>
<span data-ttu-id="d672e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d672e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d672e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d672e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d672e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d672e-142">CommonParameters</span></span>
<span data-ttu-id="d672e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d672e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d672e-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d672e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d672e-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d672e-145">INPUTS</span></span>

### <span data-ttu-id="d672e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d672e-146">System.String</span></span>

### <span data-ttu-id="d672e-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d672e-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d672e-148">System. Int64</span><span class="sxs-lookup"><span data-stu-id="d672e-148">System.Int64</span></span>

## <span data-ttu-id="d672e-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d672e-149">OUTPUTS</span></span>

### <span data-ttu-id="d672e-150">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="d672e-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="d672e-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="d672e-151">NOTES</span></span>

## <span data-ttu-id="d672e-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d672e-152">RELATED LINKS</span></span>

[<span data-ttu-id="d672e-153">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="d672e-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


