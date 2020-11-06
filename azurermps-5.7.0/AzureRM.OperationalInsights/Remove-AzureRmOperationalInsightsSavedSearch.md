---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: e66ca332d2fd59faa64e4360d00af714cfa28475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476725"
---
# <span data-ttu-id="64983-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="64983-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="64983-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64983-102">SYNOPSIS</span></span>
<span data-ttu-id="64983-103">Entfernt eine gespeicherte Suche aus dem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="64983-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64983-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64983-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64983-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64983-105">DESCRIPTION</span></span>
<span data-ttu-id="64983-106">Mit dem Cmdlet **Remove-AzureRmOperationalInsightsSavedSearch** wird eine gespeicherte Suche aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="64983-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="64983-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64983-107">EXAMPLES</span></span>

### <span data-ttu-id="64983-108">Beispiel 1: Entfernen einer gespeicherten Suche</span><span class="sxs-lookup"><span data-stu-id="64983-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="64983-109">Mit diesem Befehl wird eine gespeicherte Suche aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="64983-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="64983-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64983-110">PARAMETERS</span></span>

### <span data-ttu-id="64983-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64983-111">-DefaultProfile</span></span>
<span data-ttu-id="64983-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="64983-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64983-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64983-113">-ResourceGroupName</span></span>
<span data-ttu-id="64983-114">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="64983-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="64983-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="64983-115">-SavedSearchId</span></span>
<span data-ttu-id="64983-116">Gibt die gespeicherte Such-ID an.</span><span class="sxs-lookup"><span data-stu-id="64983-116">Specifies the saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64983-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64983-117">-WorkspaceName</span></span>
<span data-ttu-id="64983-118">Gibt den Arbeitsbereichsnamen an.</span><span class="sxs-lookup"><span data-stu-id="64983-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="64983-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64983-119">-Confirm</span></span>
<span data-ttu-id="64983-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64983-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64983-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64983-121">-WhatIf</span></span>
<span data-ttu-id="64983-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64983-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64983-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64983-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64983-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64983-124">CommonParameters</span></span>
<span data-ttu-id="64983-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64983-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64983-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64983-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64983-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64983-127">INPUTS</span></span>

### <span data-ttu-id="64983-128">Keine</span><span class="sxs-lookup"><span data-stu-id="64983-128">None</span></span>
<span data-ttu-id="64983-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="64983-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64983-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64983-130">OUTPUTS</span></span>

## <span data-ttu-id="64983-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="64983-131">NOTES</span></span>

## <span data-ttu-id="64983-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64983-132">RELATED LINKS</span></span>

[<span data-ttu-id="64983-133">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="64983-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


