---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 9b1339d138087207b84a7f515c66bd9964420dcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401486"
---
# <span data-ttu-id="91995-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="91995-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="91995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91995-102">SYNOPSIS</span></span>
<span data-ttu-id="91995-103">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="91995-103">Create WAF policy</span></span>

## <span data-ttu-id="91995-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91995-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91995-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91995-105">DESCRIPTION</span></span>
<span data-ttu-id="91995-106">Das **Cmdlet "New-AzFrontD selbstFireWallPolicy"** erstellt eine neue Azure -WAF-Richtlinie in der angegebenen Ressourcengruppe unter dem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="91995-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="91995-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91995-107">EXAMPLES</span></span>

### <span data-ttu-id="91995-108">Beispiel 1: Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="91995-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="91995-109">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="91995-109">Create WAF policy</span></span>

## <span data-ttu-id="91995-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91995-110">PARAMETERS</span></span>

### <span data-ttu-id="91995-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="91995-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="91995-112">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="91995-112">Custom Response Body</span></span>

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

### <span data-ttu-id="91995-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="91995-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="91995-114">Benutzerdefinierter Antwortstatuscode</span><span class="sxs-lookup"><span data-stu-id="91995-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91995-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="91995-115">-Customrule</span></span>
<span data-ttu-id="91995-116">Benutzerdefinierte Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="91995-116">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91995-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91995-117">-DefaultProfile</span></span>
<span data-ttu-id="91995-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91995-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91995-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="91995-119">-EnabledState</span></span>
<span data-ttu-id="91995-120">Gibt an, ob sich die Richtlinie im Status "Aktiviert" oder "Deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="91995-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="91995-121">Mögliche Werte sind: "Disabled", "Enabled".</span><span class="sxs-lookup"><span data-stu-id="91995-121">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91995-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="91995-122">-ManagedRule</span></span>
<span data-ttu-id="91995-123">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="91995-123">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91995-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="91995-124">-Mode</span></span>
<span data-ttu-id="91995-125">Beschreibt, ob er sich auf Richtlinienebene im Erkennungs- oder Verhinderungsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="91995-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="91995-126">Mögliche Werte sind:'Vermeidung', 'Erkennung'</span><span class="sxs-lookup"><span data-stu-id="91995-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91995-127">-Name</span><span class="sxs-lookup"><span data-stu-id="91995-127">-Name</span></span>
<span data-ttu-id="91995-128">Name von WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="91995-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="91995-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="91995-129">-RedirectUrl</span></span>
<span data-ttu-id="91995-130">Umleitungs-URL</span><span class="sxs-lookup"><span data-stu-id="91995-130">Redirect URL</span></span>

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

### <span data-ttu-id="91995-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91995-131">-ResourceGroupName</span></span>
<span data-ttu-id="91995-132">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="91995-132">The resource group name</span></span>

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

### <span data-ttu-id="91995-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91995-133">-Confirm</span></span>
<span data-ttu-id="91995-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91995-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91995-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="91995-135">-WhatIf</span></span>
<span data-ttu-id="91995-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91995-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91995-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91995-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91995-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91995-138">CommonParameters</span></span>
<span data-ttu-id="91995-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91995-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91995-140">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91995-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91995-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91995-141">INPUTS</span></span>

### <span data-ttu-id="91995-142">Keine</span><span class="sxs-lookup"><span data-stu-id="91995-142">None</span></span>

## <span data-ttu-id="91995-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91995-143">OUTPUTS</span></span>

### <span data-ttu-id="91995-144">Microsoft.Azure.Commands.FrontD selbst.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="91995-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="91995-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91995-145">NOTES</span></span>

## <span data-ttu-id="91995-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91995-146">RELATED LINKS</span></span>

<span data-ttu-id="91995-147">[Get-AzFrontD firewallWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontD firewallWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Update-AzFrontD firewallWallPolicy](./Update-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontD dannManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDcustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="91995-147">[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[Update-AzFrontDoorFireWallPolicy](./Update-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
