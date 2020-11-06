---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a233e41ed91a40e8fb16ccda7ed640f8ad5239ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481741"
---
# <span data-ttu-id="89c47-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="89c47-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="89c47-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89c47-102">SYNOPSIS</span></span>
<span data-ttu-id="89c47-103">Erstellt eine neue gespeicherte Suche mit den angegebenen Parametern.</span><span class="sxs-lookup"><span data-stu-id="89c47-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89c47-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89c47-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89c47-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89c47-105">DESCRIPTION</span></span>
<span data-ttu-id="89c47-106">Das Cmdlet **New-AzureRmOperationalInsightsSavedSearch** erstellt eine neue gespeicherte Suche mit den angegebenen Parametern für den Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="89c47-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="89c47-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89c47-107">EXAMPLES</span></span>

### <span data-ttu-id="89c47-108">Beispiel 1: Erstellen einer neuen gespeicherten Suche</span><span class="sxs-lookup"><span data-stu-id="89c47-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="89c47-109">Dieser Befehl erstellt eine neue gespeicherte Suche.</span><span class="sxs-lookup"><span data-stu-id="89c47-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="89c47-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="89c47-110">PARAMETERS</span></span>

### <span data-ttu-id="89c47-111">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="89c47-111">-Category</span></span>
<span data-ttu-id="89c47-112">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="89c47-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="89c47-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="89c47-113">-DisplayName</span></span>
<span data-ttu-id="89c47-114">Gibt den Namen der gespeicherten Suchanzeige an.</span><span class="sxs-lookup"><span data-stu-id="89c47-114">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="89c47-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89c47-115">-Force</span></span>
<span data-ttu-id="89c47-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="89c47-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89c47-117">-Query</span><span class="sxs-lookup"><span data-stu-id="89c47-117">-Query</span></span>
<span data-ttu-id="89c47-118">Gibt den Abfragenamen an.</span><span class="sxs-lookup"><span data-stu-id="89c47-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="89c47-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c47-119">-ResourceGroupName</span></span>
<span data-ttu-id="89c47-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="89c47-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="89c47-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="89c47-121">-SavedSearchId</span></span>
<span data-ttu-id="89c47-122">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="89c47-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="89c47-123">-Tags</span><span class="sxs-lookup"><span data-stu-id="89c47-123">-Tags</span></span>
<span data-ttu-id="89c47-124">Gibt die Ressourcenkategorien für die gespeicherte Suche an.</span><span class="sxs-lookup"><span data-stu-id="89c47-124">Specifies the resource tags for the saved search.</span></span>

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

### <span data-ttu-id="89c47-125">-Version</span><span class="sxs-lookup"><span data-stu-id="89c47-125">-Version</span></span>
<span data-ttu-id="89c47-126">Gibt die Version an.</span><span class="sxs-lookup"><span data-stu-id="89c47-126">Specifies the version.</span></span>

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

### <span data-ttu-id="89c47-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89c47-127">-WorkspaceName</span></span>
<span data-ttu-id="89c47-128">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="89c47-128">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="89c47-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89c47-129">-Confirm</span></span>
<span data-ttu-id="89c47-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89c47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89c47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89c47-131">-WhatIf</span></span>
<span data-ttu-id="89c47-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89c47-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89c47-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89c47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89c47-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c47-134">-DefaultProfile</span></span>
<span data-ttu-id="89c47-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89c47-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89c47-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c47-136">CommonParameters</span></span>
<span data-ttu-id="89c47-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c47-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c47-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c47-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c47-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89c47-139">INPUTS</span></span>

## <span data-ttu-id="89c47-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89c47-140">OUTPUTS</span></span>

## <span data-ttu-id="89c47-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="89c47-141">NOTES</span></span>

## <span data-ttu-id="89c47-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89c47-142">RELATED LINKS</span></span>

[<span data-ttu-id="89c47-143">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="89c47-143">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


