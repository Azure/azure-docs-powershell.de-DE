---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306760"
---
# <span data-ttu-id="b4aab-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4aab-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="b4aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4aab-102">SYNOPSIS</span></span>
<span data-ttu-id="b4aab-103">Löschen eines verknüpften Speicherkontos mit Anwendungseinblicken</span><span class="sxs-lookup"><span data-stu-id="b4aab-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="b4aab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4aab-104">SYNTAX</span></span>

### <span data-ttu-id="b4aab-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4aab-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4aab-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4aab-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4aab-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4aab-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4aab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4aab-108">DESCRIPTION</span></span>
<span data-ttu-id="b4aab-109">Löschen eines verknüpften Speicherkontos mit Anwendungseinblicken</span><span class="sxs-lookup"><span data-stu-id="b4aab-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="b4aab-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4aab-110">EXAMPLES</span></span>

### <span data-ttu-id="b4aab-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4aab-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="b4aab-112">Löschen eines verknüpften Speicherkontos, das der Komponente "componentName" von Anwendungserkenntnissen zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="b4aab-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="b4aab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4aab-113">PARAMETERS</span></span>

### <span data-ttu-id="b4aab-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="b4aab-114">-ComponentName</span></span>
<span data-ttu-id="b4aab-115">Komponentenname</span><span class="sxs-lookup"><span data-stu-id="b4aab-115">Component Name</span></span>

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

### <span data-ttu-id="b4aab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4aab-116">-DefaultProfile</span></span>
<span data-ttu-id="b4aab-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4aab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4aab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4aab-118">-InputObject</span></span>
<span data-ttu-id="b4aab-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b4aab-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="b4aab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4aab-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4aab-121">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b4aab-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b4aab-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4aab-122">-ResourceId</span></span>
<span data-ttu-id="b4aab-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4aab-123">Component ResourceId</span></span>

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

### <span data-ttu-id="b4aab-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4aab-124">-Confirm</span></span>
<span data-ttu-id="b4aab-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4aab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4aab-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b4aab-126">-WhatIf</span></span>
<span data-ttu-id="b4aab-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4aab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4aab-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4aab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4aab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4aab-129">CommonParameters</span></span>
<span data-ttu-id="b4aab-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4aab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4aab-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4aab-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4aab-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4aab-132">INPUTS</span></span>

### <span data-ttu-id="b4aab-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b4aab-133">System.String</span></span>

### <span data-ttu-id="b4aab-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b4aab-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="b4aab-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4aab-135">OUTPUTS</span></span>

### <span data-ttu-id="b4aab-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4aab-136">System.Boolean</span></span>

## <span data-ttu-id="b4aab-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4aab-137">NOTES</span></span>

## <span data-ttu-id="b4aab-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4aab-138">RELATED LINKS</span></span>
