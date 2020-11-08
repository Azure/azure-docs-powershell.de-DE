---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178281"
---
# <span data-ttu-id="a14c0-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="a14c0-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="a14c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a14c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a14c0-103">Aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a14c0-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="a14c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a14c0-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a14c0-105">DESCRIPTION</span></span>
<span data-ttu-id="a14c0-106">Das Cmdlet " **Satz-AzOperationalInsightsSavedSearch** " aktualisiert eine gespeicherte Suche, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a14c0-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="a14c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a14c0-107">EXAMPLES</span></span>

### <span data-ttu-id="a14c0-108">Beispiel 1: legt eine gespeicherte Suche mit aktualisierten Eigenschaften fest</span><span class="sxs-lookup"><span data-stu-id="a14c0-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="a14c0-109">Mit diesem Befehl wird eine gespeicherte Suche mit aktualisierten Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a14c0-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="a14c0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a14c0-110">PARAMETERS</span></span>

### <span data-ttu-id="a14c0-111">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="a14c0-111">-Category</span></span>
<span data-ttu-id="a14c0-112">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="a14c0-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="a14c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14c0-113">-DefaultProfile</span></span>
<span data-ttu-id="a14c0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a14c0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a14c0-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a14c0-115">-DisplayName</span></span>
<span data-ttu-id="a14c0-116">Gibt den Anzeigenamen an.</span><span class="sxs-lookup"><span data-stu-id="a14c0-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="a14c0-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="a14c0-117">-ETag</span></span>
<span data-ttu-id="a14c0-118">Gibt den ETag-Namen an.</span><span class="sxs-lookup"><span data-stu-id="a14c0-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="a14c0-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="a14c0-119">-FunctionAlias</span></span>
<span data-ttu-id="a14c0-120">Der Funktions-Alias, wenn Query als Funktion fungiert.</span><span class="sxs-lookup"><span data-stu-id="a14c0-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="a14c0-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="a14c0-121">-FunctionParameter</span></span>
<span data-ttu-id="a14c0-122">Die optionalen Funktionsparameter, wenn Query als Funktion fungiert.</span><span class="sxs-lookup"><span data-stu-id="a14c0-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="a14c0-123">Der Wert sollte das folgende Format aufweisen: ' param-Name1: default_value1, param-Name2: Typ2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="a14c0-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="a14c0-124">Weitere Beispiele und die richtige Syntax finden Sie unter https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="a14c0-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="a14c0-125">-Query</span><span class="sxs-lookup"><span data-stu-id="a14c0-125">-Query</span></span>
<span data-ttu-id="a14c0-126">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="a14c0-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="a14c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="a14c0-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a14c0-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="a14c0-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="a14c0-129">-SavedSearchId</span></span>
<span data-ttu-id="a14c0-130">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="a14c0-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="a14c0-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="a14c0-131">-Tag</span></span>
<span data-ttu-id="a14c0-132">Die gespeicherten Suchkategorien.</span><span class="sxs-lookup"><span data-stu-id="a14c0-132">The saved search tags.</span></span>

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

### <span data-ttu-id="a14c0-133">-Version</span><span class="sxs-lookup"><span data-stu-id="a14c0-133">-Version</span></span>
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

### <span data-ttu-id="a14c0-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a14c0-134">-WorkspaceName</span></span>
<span data-ttu-id="a14c0-135">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="a14c0-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="a14c0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14c0-136">CommonParameters</span></span>
<span data-ttu-id="a14c0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14c0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14c0-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a14c0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14c0-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a14c0-139">INPUTS</span></span>

### <span data-ttu-id="a14c0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a14c0-140">System.String</span></span>

### <span data-ttu-id="a14c0-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a14c0-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a14c0-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="a14c0-142">System.Int64</span></span>

## <span data-ttu-id="a14c0-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a14c0-143">OUTPUTS</span></span>

### <span data-ttu-id="a14c0-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="a14c0-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="a14c0-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a14c0-145">NOTES</span></span>

## <span data-ttu-id="a14c0-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a14c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="a14c0-147">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="a14c0-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


