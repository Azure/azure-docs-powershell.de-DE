---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296548"
---
# <span data-ttu-id="0f1dc-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="0f1dc-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="0f1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1dc-103">Entfernt eine gespeicherte Suche aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="0f1dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f1dc-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f1dc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="0f1dc-106">Das **Cmdlet "Remove-AzOperationalInsightsSavedSearch"** entfernt eine gespeicherte Suche aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="0f1dc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f1dc-107">EXAMPLES</span></span>

### <span data-ttu-id="0f1dc-108">Beispiel 1: Entfernen einer gespeicherten Suche</span><span class="sxs-lookup"><span data-stu-id="0f1dc-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="0f1dc-109">Mit diesem Befehl wird eine gespeicherte Suche aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="0f1dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f1dc-110">PARAMETERS</span></span>

### <span data-ttu-id="0f1dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f1dc-111">-DefaultProfile</span></span>
<span data-ttu-id="0f1dc-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0f1dc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f1dc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f1dc-113">-ResourceGroupName</span></span>
<span data-ttu-id="0f1dc-114">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0f1dc-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="0f1dc-115">-SavedSearchId</span></span>
<span data-ttu-id="0f1dc-116">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="0f1dc-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f1dc-117">-WorkspaceName</span></span>
<span data-ttu-id="0f1dc-118">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0f1dc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f1dc-119">-Confirm</span></span>
<span data-ttu-id="0f1dc-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f1dc-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0f1dc-121">-WhatIf</span></span>
<span data-ttu-id="0f1dc-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f1dc-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f1dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1dc-124">CommonParameters</span></span>
<span data-ttu-id="0f1dc-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f1dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1dc-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f1dc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1dc-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f1dc-127">INPUTS</span></span>

### <span data-ttu-id="0f1dc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0f1dc-128">System.String</span></span>

## <span data-ttu-id="0f1dc-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f1dc-129">OUTPUTS</span></span>

### <span data-ttu-id="0f1dc-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="0f1dc-130">System.Void</span></span>

## <span data-ttu-id="0f1dc-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f1dc-131">NOTES</span></span>

## <span data-ttu-id="0f1dc-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f1dc-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f1dc-133">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0f1dc-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


