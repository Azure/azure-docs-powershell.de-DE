---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: af63ecd604f6ea7e475fcc8034a4e4b6d532069e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924440"
---
# <span data-ttu-id="06bbf-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="06bbf-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="06bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="06bbf-103">Löschen sie eine Analyse.</span><span class="sxs-lookup"><span data-stu-id="06bbf-103">Delete an Analytic.</span></span>

## <span data-ttu-id="06bbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06bbf-104">SYNTAX</span></span>

### <span data-ttu-id="06bbf-105">AlertRuleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="06bbf-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06bbf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="06bbf-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06bbf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06bbf-107">DESCRIPTION</span></span>
<span data-ttu-id="06bbf-108">Das **Cmdlet Remove-AzSentinelAlertRule** löscht eine Warnungsregel endgültig aus einem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="06bbf-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="06bbf-109">Sie können ein **AlertRule-Objekt** mithilfe des Pipelineoperators übergeben oder die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="06bbf-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="06bbf-110">Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="06bbf-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="06bbf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06bbf-111">EXAMPLES</span></span>

### <span data-ttu-id="06bbf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06bbf-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="06bbf-113">Mit diesem Befehl wird die Warnungsregel aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="06bbf-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="06bbf-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="06bbf-114">PARAMETERS</span></span>

### <span data-ttu-id="06bbf-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="06bbf-115">-AlertRuleId</span></span>
<span data-ttu-id="06bbf-116">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="06bbf-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bbf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06bbf-117">-DefaultProfile</span></span>
<span data-ttu-id="06bbf-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06bbf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06bbf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06bbf-119">-InputObject</span></span>
<span data-ttu-id="06bbf-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="06bbf-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06bbf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06bbf-121">-PassThru</span></span>
<span data-ttu-id="06bbf-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="06bbf-122">PassThru</span></span>

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

### <span data-ttu-id="06bbf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06bbf-123">-ResourceGroupName</span></span>
<span data-ttu-id="06bbf-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="06bbf-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bbf-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06bbf-125">-WorkspaceName</span></span>
<span data-ttu-id="06bbf-126">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="06bbf-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06bbf-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06bbf-127">-Confirm</span></span>
<span data-ttu-id="06bbf-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06bbf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06bbf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06bbf-129">-WhatIf</span></span>
<span data-ttu-id="06bbf-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06bbf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06bbf-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06bbf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06bbf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06bbf-132">CommonParameters</span></span>
<span data-ttu-id="06bbf-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06bbf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06bbf-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06bbf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06bbf-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06bbf-135">INPUTS</span></span>

### <span data-ttu-id="06bbf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="06bbf-136">System.String</span></span>
### <span data-ttu-id="06bbf-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="06bbf-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="06bbf-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06bbf-138">OUTPUTS</span></span>

### <span data-ttu-id="06bbf-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="06bbf-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="06bbf-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="06bbf-140">NOTES</span></span>

## <span data-ttu-id="06bbf-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="06bbf-141">RELATED LINKS</span></span>
