---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471953"
---
# <span data-ttu-id="19380-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="19380-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="19380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19380-102">SYNOPSIS</span></span>
<span data-ttu-id="19380-103">Entfernen einer automatisierten Antwort aus einer Analyse</span><span class="sxs-lookup"><span data-stu-id="19380-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="19380-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19380-104">SYNTAX</span></span>

### <span data-ttu-id="19380-105">ActionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="19380-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19380-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="19380-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19380-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19380-107">DESCRIPTION</span></span>
<span data-ttu-id="19380-108">Das **Cmdlet "Remove-AzSentinelAlertRuleAction"** löscht eine automatisierte Antwort aus der Warnungsregel in einem angegebenen Arbeitsbereich endgültig.</span><span class="sxs-lookup"><span data-stu-id="19380-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="19380-109">Sie können ein **AlertRuleAction-Objekt** mit dem Pipelineoperator übergeben, oder Sie können die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="19380-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="19380-110">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="19380-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="19380-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19380-111">EXAMPLES</span></span>

### <span data-ttu-id="19380-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19380-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="19380-113">Mit diesem Befehl wird die Warnungsregel aus dem Arbeitsbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="19380-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="19380-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19380-114">PARAMETERS</span></span>

### <span data-ttu-id="19380-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="19380-115">-ActionId</span></span>
<span data-ttu-id="19380-116">Aktions-ID.</span><span class="sxs-lookup"><span data-stu-id="19380-116">Action Id.</span></span>

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

### <span data-ttu-id="19380-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="19380-117">-AlertRuleId</span></span>
<span data-ttu-id="19380-118">Benachrichtigungsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="19380-118">Alert Rule Id.</span></span>

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

### <span data-ttu-id="19380-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19380-119">-DefaultProfile</span></span>
<span data-ttu-id="19380-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19380-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19380-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19380-121">-InputObject</span></span>
<span data-ttu-id="19380-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="19380-122">InputObject.</span></span>

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

### <span data-ttu-id="19380-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19380-123">-PassThru</span></span>
<span data-ttu-id="19380-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="19380-124">PassThru</span></span>

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

### <span data-ttu-id="19380-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19380-125">-ResourceGroupName</span></span>
<span data-ttu-id="19380-126">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="19380-126">Resource group name.</span></span>

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

### <span data-ttu-id="19380-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19380-127">-WorkspaceName</span></span>
<span data-ttu-id="19380-128">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="19380-128">Workspace Name.</span></span>

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

### <span data-ttu-id="19380-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19380-129">-Confirm</span></span>
<span data-ttu-id="19380-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19380-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19380-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="19380-131">-WhatIf</span></span>
<span data-ttu-id="19380-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19380-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19380-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19380-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19380-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19380-134">CommonParameters</span></span>
<span data-ttu-id="19380-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19380-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19380-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19380-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19380-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19380-137">INPUTS</span></span>

### <span data-ttu-id="19380-138">System.String</span><span class="sxs-lookup"><span data-stu-id="19380-138">System.String</span></span>
### <span data-ttu-id="19380-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="19380-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="19380-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19380-140">OUTPUTS</span></span>

### <span data-ttu-id="19380-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="19380-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="19380-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="19380-142">NOTES</span></span>

## <span data-ttu-id="19380-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="19380-143">RELATED LINKS</span></span>
