---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 247589f50028fb8d4cebf78f0ad45bb2124e43cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482173"
---
# <span data-ttu-id="612f4-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="612f4-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="612f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="612f4-102">SYNOPSIS</span></span>
<span data-ttu-id="612f4-103">Erstellt eine neue gespeicherte Suche mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="612f4-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="612f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="612f4-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="612f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="612f4-105">DESCRIPTION</span></span>
<span data-ttu-id="612f4-106">Das Cmdlet **New-AzureRmOperationalInsightsSavedSearch** erstellt eine neue gespeicherte Suche mit den angegebenen Parametern für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="612f4-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="612f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="612f4-107">EXAMPLES</span></span>

### <span data-ttu-id="612f4-108">Beispiel 1: Erstellen einer neuen gespeicherten Suche</span><span class="sxs-lookup"><span data-stu-id="612f4-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="612f4-109">Dieser Befehl erstellt eine neue gespeicherte Suche.</span><span class="sxs-lookup"><span data-stu-id="612f4-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="612f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="612f4-110">PARAMETERS</span></span>

### <span data-ttu-id="612f4-111">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="612f4-111">-Category</span></span>
<span data-ttu-id="612f4-112">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="612f4-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="612f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612f4-113">-DefaultProfile</span></span>
<span data-ttu-id="612f4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="612f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="612f4-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="612f4-115">-DisplayName</span></span>
<span data-ttu-id="612f4-116">Gibt den Namen der gespeicherten Suchanzeige an.</span><span class="sxs-lookup"><span data-stu-id="612f4-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="612f4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="612f4-117">-Force</span></span>
<span data-ttu-id="612f4-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="612f4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="612f4-119">-Query</span><span class="sxs-lookup"><span data-stu-id="612f4-119">-Query</span></span>
<span data-ttu-id="612f4-120">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="612f4-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="612f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="612f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="612f4-122">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="612f4-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="612f4-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="612f4-123">-SavedSearchId</span></span>
<span data-ttu-id="612f4-124">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="612f4-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="612f4-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="612f4-125">-Tag</span></span>
<span data-ttu-id="612f4-126">Die gespeicherten Suchkategorien.</span><span class="sxs-lookup"><span data-stu-id="612f4-126">The saved search tags.</span></span>

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

### <span data-ttu-id="612f4-127">-Version</span><span class="sxs-lookup"><span data-stu-id="612f4-127">-Version</span></span>
<span data-ttu-id="612f4-128">Gibt die Version an.</span><span class="sxs-lookup"><span data-stu-id="612f4-128">Specifies the version.</span></span>

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

### <span data-ttu-id="612f4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="612f4-129">-WorkspaceName</span></span>
<span data-ttu-id="612f4-130">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="612f4-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="612f4-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="612f4-131">-Confirm</span></span>
<span data-ttu-id="612f4-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="612f4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="612f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="612f4-133">-WhatIf</span></span>
<span data-ttu-id="612f4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="612f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="612f4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="612f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="612f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612f4-136">CommonParameters</span></span>
<span data-ttu-id="612f4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="612f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612f4-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="612f4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612f4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="612f4-139">INPUTS</span></span>

### <span data-ttu-id="612f4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="612f4-140">System.String</span></span>

### <span data-ttu-id="612f4-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="612f4-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="612f4-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="612f4-142">System.Int64</span></span>

## <span data-ttu-id="612f4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="612f4-143">OUTPUTS</span></span>

### <span data-ttu-id="612f4-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="612f4-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="612f4-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="612f4-145">NOTES</span></span>

## <span data-ttu-id="612f4-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="612f4-146">RELATED LINKS</span></span>

[<span data-ttu-id="612f4-147">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="612f4-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


