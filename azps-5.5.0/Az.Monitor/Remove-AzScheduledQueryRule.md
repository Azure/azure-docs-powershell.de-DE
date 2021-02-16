---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170189"
---
# <span data-ttu-id="85ac7-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="85ac7-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="85ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="85ac7-103">Entfernt eine Protokollwarnungsregel</span><span class="sxs-lookup"><span data-stu-id="85ac7-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="85ac7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85ac7-104">SYNTAX</span></span>

### <span data-ttu-id="85ac7-105">ByRuleName (Standard)</span><span class="sxs-lookup"><span data-stu-id="85ac7-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85ac7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="85ac7-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85ac7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="85ac7-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85ac7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85ac7-108">DESCRIPTION</span></span>
<span data-ttu-id="85ac7-109">Entfernt eine Protokollwarnungsregel</span><span class="sxs-lookup"><span data-stu-id="85ac7-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="85ac7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85ac7-110">EXAMPLES</span></span>

### <span data-ttu-id="85ac7-111">Beispiel 1: Entfernen nach Regelname</span><span class="sxs-lookup"><span data-stu-id="85ac7-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="85ac7-112">Beispiel 2: Entfernen durch Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="85ac7-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="85ac7-113">Beispiel 3: Entfernen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="85ac7-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="85ac7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85ac7-114">PARAMETERS</span></span>

### <span data-ttu-id="85ac7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ac7-115">-DefaultProfile</span></span>
<span data-ttu-id="85ac7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85ac7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85ac7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85ac7-117">-InputObject</span></span>
<span data-ttu-id="85ac7-118">Ressource "Geplante Abfrageregel"</span><span class="sxs-lookup"><span data-stu-id="85ac7-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85ac7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="85ac7-119">-Name</span></span>
<span data-ttu-id="85ac7-120">Der Benachrichtigungsname</span><span class="sxs-lookup"><span data-stu-id="85ac7-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ac7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85ac7-121">-PassThru</span></span>
<span data-ttu-id="85ac7-122">Gibt einen Wert zurück, der Erfolg oder Misserfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="85ac7-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="85ac7-123">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="85ac7-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85ac7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ac7-124">-ResourceGroupName</span></span>
<span data-ttu-id="85ac7-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="85ac7-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ac7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85ac7-126">-ResourceId</span></span>
<span data-ttu-id="85ac7-127">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="85ac7-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85ac7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85ac7-128">-Confirm</span></span>
<span data-ttu-id="85ac7-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85ac7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85ac7-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="85ac7-130">-WhatIf</span></span>
<span data-ttu-id="85ac7-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85ac7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85ac7-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85ac7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85ac7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ac7-133">CommonParameters</span></span>
<span data-ttu-id="85ac7-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85ac7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ac7-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85ac7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ac7-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85ac7-136">INPUTS</span></span>

### <span data-ttu-id="85ac7-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="85ac7-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="85ac7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="85ac7-138">System.String</span></span>

## <span data-ttu-id="85ac7-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85ac7-139">OUTPUTS</span></span>

### <span data-ttu-id="85ac7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85ac7-140">System.Boolean</span></span>

## <span data-ttu-id="85ac7-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85ac7-141">NOTES</span></span>

## <span data-ttu-id="85ac7-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85ac7-142">RELATED LINKS</span></span>
