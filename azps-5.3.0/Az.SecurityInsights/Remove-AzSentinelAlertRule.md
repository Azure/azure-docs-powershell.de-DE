---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471955"
---
# <span data-ttu-id="89619-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="89619-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="89619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89619-102">SYNOPSIS</span></span>
<span data-ttu-id="89619-103">Löschen sie eine Analyse.</span><span class="sxs-lookup"><span data-stu-id="89619-103">Delete an Analytic.</span></span>

## <span data-ttu-id="89619-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89619-104">SYNTAX</span></span>

### <span data-ttu-id="89619-105">AlertRuleId (Standard)</span><span class="sxs-lookup"><span data-stu-id="89619-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89619-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="89619-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89619-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89619-107">DESCRIPTION</span></span>
<span data-ttu-id="89619-108">Das **Cmdlet "Remove-AzSentinelAlertRule"** löscht eine Warnungsregel endgültig aus einem angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="89619-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="89619-109">Sie können ein **"AlertRule"-Objekt** mithilfe des Pipelineoperators übergeben, oder Sie können die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="89619-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="89619-110">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="89619-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="89619-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89619-111">EXAMPLES</span></span>

### <span data-ttu-id="89619-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89619-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="89619-113">Mit diesem Befehl wird die Warnungsregel aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="89619-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="89619-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89619-114">PARAMETERS</span></span>

### <span data-ttu-id="89619-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="89619-115">-AlertRuleId</span></span>
<span data-ttu-id="89619-116">Benachrichtigungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="89619-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="89619-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89619-117">-DefaultProfile</span></span>
<span data-ttu-id="89619-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89619-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89619-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89619-119">-InputObject</span></span>
<span data-ttu-id="89619-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="89619-120">InputObject.</span></span>

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

### <span data-ttu-id="89619-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89619-121">-PassThru</span></span>
<span data-ttu-id="89619-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="89619-122">PassThru</span></span>

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

### <span data-ttu-id="89619-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89619-123">-ResourceGroupName</span></span>
<span data-ttu-id="89619-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="89619-124">Resource group name.</span></span>

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

### <span data-ttu-id="89619-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89619-125">-WorkspaceName</span></span>
<span data-ttu-id="89619-126">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="89619-126">Workspace Name.</span></span>

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

### <span data-ttu-id="89619-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89619-127">-Confirm</span></span>
<span data-ttu-id="89619-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89619-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89619-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="89619-129">-WhatIf</span></span>
<span data-ttu-id="89619-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89619-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89619-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89619-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89619-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89619-132">CommonParameters</span></span>
<span data-ttu-id="89619-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89619-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89619-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89619-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89619-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89619-135">INPUTS</span></span>

### <span data-ttu-id="89619-136">System.String</span><span class="sxs-lookup"><span data-stu-id="89619-136">System.String</span></span>
### <span data-ttu-id="89619-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="89619-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="89619-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89619-138">OUTPUTS</span></span>

### <span data-ttu-id="89619-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="89619-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="89619-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89619-140">NOTES</span></span>

## <span data-ttu-id="89619-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89619-141">RELATED LINKS</span></span>
