---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 0828961a534a6f98d52cdf8c4e2a134cc2975df4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924432"
---
# <span data-ttu-id="6f1e5-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="6f1e5-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="6f1e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1e5-103">Entfernen einer automatisierten Antwort aus einer Analyse.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="6f1e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f1e5-104">SYNTAX</span></span>

### <span data-ttu-id="6f1e5-105">ActionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f1e5-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f1e5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6f1e5-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f1e5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f1e5-107">DESCRIPTION</span></span>
<span data-ttu-id="6f1e5-108">Das **Cmdlet Remove-AzSentinelAlertRuleAction** löscht eine automatisierte Antwort aus der Warnungsregel in einem angegebenen Arbeitsbereich endgültig.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="6f1e5-109">Sie können ein **AlertRuleAction-Objekt** mithilfe des Pipelineoperators übergeben oder die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="6f1e5-110">Sie können den Parameter Bestätigen und die $ConfirmPreference Windows PowerShell verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6f1e5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f1e5-111">EXAMPLES</span></span>

### <span data-ttu-id="6f1e5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f1e5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="6f1e5-113">Mit diesem Befehl wird die Warnungsregel aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="6f1e5-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6f1e5-114">PARAMETERS</span></span>

### <span data-ttu-id="6f1e5-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="6f1e5-115">-ActionId</span></span>
<span data-ttu-id="6f1e5-116">Aktions-ID.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-116">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1e5-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="6f1e5-117">-AlertRuleId</span></span>
<span data-ttu-id="6f1e5-118">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1e5-119">-DefaultProfile</span></span>
<span data-ttu-id="6f1e5-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f1e5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f1e5-121">-InputObject</span></span>
<span data-ttu-id="6f1e5-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-122">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1e5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f1e5-123">-PassThru</span></span>
<span data-ttu-id="6f1e5-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="6f1e5-124">PassThru</span></span>

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

### <span data-ttu-id="6f1e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f1e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f1e5-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1e5-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f1e5-127">-WorkspaceName</span></span>
<span data-ttu-id="6f1e5-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1e5-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f1e5-129">-Confirm</span></span>
<span data-ttu-id="6f1e5-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f1e5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f1e5-131">-WhatIf</span></span>
<span data-ttu-id="6f1e5-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f1e5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f1e5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1e5-134">CommonParameters</span></span>
<span data-ttu-id="6f1e5-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f1e5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1e5-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f1e5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1e5-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f1e5-137">INPUTS</span></span>

### <span data-ttu-id="6f1e5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6f1e5-138">System.String</span></span>
### <span data-ttu-id="6f1e5-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="6f1e5-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="6f1e5-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f1e5-140">OUTPUTS</span></span>

### <span data-ttu-id="6f1e5-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="6f1e5-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="6f1e5-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6f1e5-142">NOTES</span></span>

## <span data-ttu-id="6f1e5-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6f1e5-143">RELATED LINKS</span></span>
