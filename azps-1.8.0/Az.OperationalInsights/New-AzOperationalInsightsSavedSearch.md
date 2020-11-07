---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 5853447dfc91511782e99ebafae644e14b6649b3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662128"
---
# <span data-ttu-id="dd8ed-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="dd8ed-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="dd8ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8ed-103">Erstellt eine neue gespeicherte Suche mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="dd8ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd8ed-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd8ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8ed-106">Das Cmdlet **New-AzOperationalInsightsSavedSearch** erstellt eine neue gespeicherte Suche mit den angegebenen Parametern für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="dd8ed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd8ed-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8ed-108">Beispiel 1: Erstellen einer neuen gespeicherten Suche</span><span class="sxs-lookup"><span data-stu-id="dd8ed-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="dd8ed-109">Dieser Befehl erstellt eine neue gespeicherte Suche.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="dd8ed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd8ed-110">PARAMETERS</span></span>

### <span data-ttu-id="dd8ed-111">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="dd8ed-111">-Category</span></span>
<span data-ttu-id="dd8ed-112">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="dd8ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8ed-113">-DefaultProfile</span></span>
<span data-ttu-id="dd8ed-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dd8ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd8ed-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd8ed-115">-DisplayName</span></span>
<span data-ttu-id="dd8ed-116">Gibt den Namen der gespeicherten Suchanzeige an.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="dd8ed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dd8ed-117">-Force</span></span>
<span data-ttu-id="dd8ed-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd8ed-119">-Query</span><span class="sxs-lookup"><span data-stu-id="dd8ed-119">-Query</span></span>
<span data-ttu-id="dd8ed-120">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="dd8ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd8ed-122">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="dd8ed-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="dd8ed-123">-SavedSearchId</span></span>
<span data-ttu-id="dd8ed-124">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="dd8ed-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd8ed-125">-Tag</span></span>
<span data-ttu-id="dd8ed-126">Die gespeicherten Suchkategorien.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-126">The saved search tags.</span></span>

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

### <span data-ttu-id="dd8ed-127">-Version</span><span class="sxs-lookup"><span data-stu-id="dd8ed-127">-Version</span></span>
<span data-ttu-id="dd8ed-128">Gibt die Version an.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8ed-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dd8ed-129">-WorkspaceName</span></span>
<span data-ttu-id="dd8ed-130">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="dd8ed-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd8ed-131">-Confirm</span></span>
<span data-ttu-id="dd8ed-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8ed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8ed-133">-WhatIf</span></span>
<span data-ttu-id="dd8ed-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8ed-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8ed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8ed-136">CommonParameters</span></span>
<span data-ttu-id="dd8ed-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8ed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8ed-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8ed-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8ed-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd8ed-139">INPUTS</span></span>

### <span data-ttu-id="dd8ed-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8ed-140">System.String</span></span>

### <span data-ttu-id="dd8ed-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dd8ed-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dd8ed-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="dd8ed-142">System.Int64</span></span>

## <span data-ttu-id="dd8ed-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd8ed-143">OUTPUTS</span></span>

### <span data-ttu-id="dd8ed-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="dd8ed-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="dd8ed-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd8ed-145">NOTES</span></span>

## <span data-ttu-id="dd8ed-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd8ed-146">RELATED LINKS</span></span>

[<span data-ttu-id="dd8ed-147">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="dd8ed-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


