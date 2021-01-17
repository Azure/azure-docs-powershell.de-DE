---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471969"
---
# <span data-ttu-id="f7393-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="f7393-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="f7393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7393-102">SYNOPSIS</span></span>
<span data-ttu-id="f7393-103">Fügen Sie einer Analyse eine automatisierte Antwort hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7393-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="f7393-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7393-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7393-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7393-105">DESCRIPTION</span></span>
<span data-ttu-id="f7393-106">Das **Cmdlet "New-AzSentinelAlertRuleAction"** erstellt eine automatisierte Antwort für eine Warnungsregel im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="f7393-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="f7393-107">Sie müssen die Resorce-ID der Logik-App und den Trigger-URI bereitstellen, die im Logik-App-Modul gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="f7393-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="f7393-108">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f7393-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f7393-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7393-109">EXAMPLES</span></span>

### <span data-ttu-id="f7393-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7393-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="f7393-111">In diesem Beispiel wird anhand der Eigenschaften der Logik-App ein **AlertRuleAction** für die angegebene Warnungsregel erstellt und dann in der $AlertRuleAction gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f7393-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="f7393-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7393-112">PARAMETERS</span></span>

### <span data-ttu-id="f7393-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="f7393-113">-ActionId</span></span>
<span data-ttu-id="f7393-114">Aktions-ID.</span><span class="sxs-lookup"><span data-stu-id="f7393-114">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7393-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="f7393-115">-AlertRuleId</span></span>
<span data-ttu-id="f7393-116">Warnungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="f7393-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="f7393-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7393-117">-DefaultProfile</span></span>
<span data-ttu-id="f7393-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7393-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7393-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="f7393-119">-LogicAppResourceId</span></span>
<span data-ttu-id="f7393-120">Ressourcen-ID der Action Logic-App.</span><span class="sxs-lookup"><span data-stu-id="f7393-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="f7393-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7393-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7393-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f7393-122">Resource group name.</span></span>

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

### <span data-ttu-id="f7393-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="f7393-123">-TriggerUri</span></span>
<span data-ttu-id="f7393-124">Trigger-URI der Aktionslogik-App.</span><span class="sxs-lookup"><span data-stu-id="f7393-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="f7393-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7393-125">-WorkspaceName</span></span>
<span data-ttu-id="f7393-126">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="f7393-126">Workspace Name.</span></span>

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

### <span data-ttu-id="f7393-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7393-127">-Confirm</span></span>
<span data-ttu-id="f7393-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7393-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7393-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f7393-129">-WhatIf</span></span>
<span data-ttu-id="f7393-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7393-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7393-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7393-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7393-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7393-132">CommonParameters</span></span>
<span data-ttu-id="f7393-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7393-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7393-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7393-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7393-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7393-135">INPUTS</span></span>

### <span data-ttu-id="f7393-136">Keine</span><span class="sxs-lookup"><span data-stu-id="f7393-136">None</span></span>
## <span data-ttu-id="f7393-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7393-137">OUTPUTS</span></span>

### <span data-ttu-id="f7393-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="f7393-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="f7393-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7393-139">NOTES</span></span>

## <span data-ttu-id="f7393-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7393-140">RELATED LINKS</span></span>
