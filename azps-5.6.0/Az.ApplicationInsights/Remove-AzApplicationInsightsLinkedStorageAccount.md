---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 377a2b967058de9c0cdae1d4c07ceffc73b1bfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944296"
---
# <span data-ttu-id="5d08c-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d08c-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5d08c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d08c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d08c-103">Löschen eines verknüpften Speicherkontos für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="5d08c-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="5d08c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d08c-104">SYNTAX</span></span>

### <span data-ttu-id="5d08c-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d08c-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d08c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d08c-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d08c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d08c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d08c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d08c-108">DESCRIPTION</span></span>
<span data-ttu-id="5d08c-109">Löschen eines verknüpften Speicherkontos für Anwendungseinblicke</span><span class="sxs-lookup"><span data-stu-id="5d08c-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="5d08c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d08c-110">EXAMPLES</span></span>

### <span data-ttu-id="5d08c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d08c-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="5d08c-112">Löschen des verknüpften Speicherkontos, das der Komponente "componentName" für Anwendungseinblicke zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="5d08c-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="5d08c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5d08c-113">PARAMETERS</span></span>

### <span data-ttu-id="5d08c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="5d08c-114">-ComponentName</span></span>
<span data-ttu-id="5d08c-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="5d08c-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d08c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d08c-116">-DefaultProfile</span></span>
<span data-ttu-id="5d08c-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d08c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d08c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d08c-118">-InputObject</span></span>
<span data-ttu-id="5d08c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5d08c-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d08c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d08c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d08c-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5d08c-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d08c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d08c-122">-ResourceId</span></span>
<span data-ttu-id="5d08c-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d08c-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d08c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d08c-124">-Confirm</span></span>
<span data-ttu-id="5d08c-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d08c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d08c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d08c-126">-WhatIf</span></span>
<span data-ttu-id="5d08c-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d08c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d08c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d08c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d08c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d08c-129">CommonParameters</span></span>
<span data-ttu-id="5d08c-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d08c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d08c-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d08c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d08c-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d08c-132">INPUTS</span></span>

### <span data-ttu-id="5d08c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5d08c-133">System.String</span></span>

### <span data-ttu-id="5d08c-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5d08c-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5d08c-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d08c-135">OUTPUTS</span></span>

### <span data-ttu-id="5d08c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d08c-136">System.Boolean</span></span>

## <span data-ttu-id="5d08c-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5d08c-137">NOTES</span></span>

## <span data-ttu-id="5d08c-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5d08c-138">RELATED LINKS</span></span>
