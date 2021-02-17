---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156353"
---
# <span data-ttu-id="ed96a-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="ed96a-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="ed96a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed96a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed96a-103">Aktualisieren einer automatisierten Antwort (Warnungsregelaktion)</span><span class="sxs-lookup"><span data-stu-id="ed96a-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="ed96a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed96a-104">SYNTAX</span></span>

### <span data-ttu-id="ed96a-105">ActionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed96a-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed96a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed96a-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed96a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed96a-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed96a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed96a-108">DESCRIPTION</span></span>
<span data-ttu-id="ed96a-109">Das **Cmdlet "Update-AzSentinelAlertRuleAction"** aktualisiert die Textmarke im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="ed96a-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="ed96a-110">Sie können ein **AlertRuleAction-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können die *Parameter "AlertRuleId"* und *"ActionId"* angeben.</span><span class="sxs-lookup"><span data-stu-id="ed96a-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="ed96a-111">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="ed96a-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ed96a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed96a-112">EXAMPLES</span></span>

### <span data-ttu-id="ed96a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed96a-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="ed96a-114">In diesem Beispiel wird **ein AlertRuleAction-Konto** aktualisiert, das eine vorhandene *Aktion durch* neue Eigenschaften ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ed96a-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="ed96a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ed96a-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="ed96a-116">In diesem Beispiel wird **alertRuleAction** mit einem InputObject aktualisiert, das eine vorhandene *Aktion* durch neue Eigenschaften ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ed96a-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="ed96a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed96a-117">PARAMETERS</span></span>

### <span data-ttu-id="ed96a-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="ed96a-118">-ActionId</span></span>
<span data-ttu-id="ed96a-119">Aktions-ID.</span><span class="sxs-lookup"><span data-stu-id="ed96a-119">Action Id.</span></span>

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

### <span data-ttu-id="ed96a-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="ed96a-120">-AlertRuleId</span></span>
<span data-ttu-id="ed96a-121">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="ed96a-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="ed96a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed96a-122">-DefaultProfile</span></span>
<span data-ttu-id="ed96a-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed96a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed96a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed96a-124">-InputObject</span></span>
<span data-ttu-id="ed96a-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="ed96a-125">InputObject.</span></span>

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

### <span data-ttu-id="ed96a-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="ed96a-126">-LogicAppResourceId</span></span>
<span data-ttu-id="ed96a-127">Ressourcen-ID der Action Logic-App.</span><span class="sxs-lookup"><span data-stu-id="ed96a-127">Action Logic App Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed96a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed96a-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed96a-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ed96a-129">Resource group name.</span></span>

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

### <span data-ttu-id="ed96a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed96a-130">-ResourceId</span></span>
<span data-ttu-id="ed96a-131">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ed96a-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed96a-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="ed96a-132">-TriggerUri</span></span>
<span data-ttu-id="ed96a-133">Trigger-URI der Aktionslogik-App.</span><span class="sxs-lookup"><span data-stu-id="ed96a-133">Action Logic App Trigger Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed96a-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed96a-134">-WorkspaceName</span></span>
<span data-ttu-id="ed96a-135">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="ed96a-135">Workspace Name.</span></span>

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

### <span data-ttu-id="ed96a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed96a-136">-Confirm</span></span>
<span data-ttu-id="ed96a-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed96a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed96a-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed96a-138">-WhatIf</span></span>
<span data-ttu-id="ed96a-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed96a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed96a-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed96a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed96a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed96a-141">CommonParameters</span></span>
<span data-ttu-id="ed96a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed96a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed96a-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed96a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed96a-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed96a-144">INPUTS</span></span>

### <span data-ttu-id="ed96a-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed96a-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="ed96a-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ed96a-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="ed96a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ed96a-147">System.String</span></span>

## <span data-ttu-id="ed96a-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed96a-148">OUTPUTS</span></span>

### <span data-ttu-id="ed96a-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ed96a-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="ed96a-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed96a-150">NOTES</span></span>

## <span data-ttu-id="ed96a-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed96a-151">RELATED LINKS</span></span>
