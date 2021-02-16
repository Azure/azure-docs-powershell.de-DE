---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 2d3811b5605b6f4923abd58c64d8d870ede8d334
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403849"
---
# <span data-ttu-id="5f05e-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="5f05e-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="5f05e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f05e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f05e-103">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5f05e-103">Create WAF policy</span></span>

## <span data-ttu-id="5f05e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f05e-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f05e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f05e-105">DESCRIPTION</span></span>
<span data-ttu-id="5f05e-106">Das **Cmdlet "New-AzFrontDlicWafPolicy"** erstellt eine neue Azure -WAF-Richtlinie in der angegebenen Ressourcengruppe unter dem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="5f05e-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="5f05e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f05e-107">EXAMPLES</span></span>

### <span data-ttu-id="5f05e-108">Beispiel 1: Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5f05e-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="5f05e-109">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5f05e-109">Create WAF policy</span></span>

## <span data-ttu-id="5f05e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f05e-110">PARAMETERS</span></span>

### <span data-ttu-id="5f05e-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="5f05e-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="5f05e-112">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="5f05e-112">Custom Response Body</span></span>

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

### <span data-ttu-id="5f05e-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="5f05e-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="5f05e-114">Benutzerdefinierter Antwortstatuscode</span><span class="sxs-lookup"><span data-stu-id="5f05e-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="5f05e-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="5f05e-115">-Customrule</span></span>
<span data-ttu-id="5f05e-116">Benutzerdefinierte Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5f05e-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="5f05e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f05e-117">-DefaultProfile</span></span>
<span data-ttu-id="5f05e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f05e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f05e-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="5f05e-119">-EnabledState</span></span>
<span data-ttu-id="5f05e-120">Gibt an, ob sich die Richtlinie im Status "Aktiviert" oder "Deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="5f05e-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="5f05e-121">Mögliche Werte sind: "Disabled", "Enabled".</span><span class="sxs-lookup"><span data-stu-id="5f05e-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="5f05e-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="5f05e-122">-ManagedRule</span></span>
<span data-ttu-id="5f05e-123">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="5f05e-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="5f05e-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="5f05e-124">-Mode</span></span>
<span data-ttu-id="5f05e-125">Beschreibt, ob er sich auf Richtlinienebene im Erkennungs- oder Verhinderungsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="5f05e-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="5f05e-126">Mögliche Werte sind:'Vermeidung', 'Erkennung'</span><span class="sxs-lookup"><span data-stu-id="5f05e-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="5f05e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5f05e-127">-Name</span></span>
<span data-ttu-id="5f05e-128">Name von WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="5f05e-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="5f05e-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="5f05e-129">-RedirectUrl</span></span>
<span data-ttu-id="5f05e-130">Umleitungs-URL</span><span class="sxs-lookup"><span data-stu-id="5f05e-130">Redirect URL</span></span>

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

### <span data-ttu-id="5f05e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f05e-131">-ResourceGroupName</span></span>
<span data-ttu-id="5f05e-132">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5f05e-132">The resource group name</span></span>

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

### <span data-ttu-id="5f05e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f05e-133">-Confirm</span></span>
<span data-ttu-id="5f05e-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f05e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f05e-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5f05e-135">-WhatIf</span></span>
<span data-ttu-id="5f05e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f05e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f05e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f05e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f05e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f05e-138">CommonParameters</span></span>
<span data-ttu-id="5f05e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f05e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f05e-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f05e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f05e-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f05e-141">INPUTS</span></span>

### <span data-ttu-id="5f05e-142">Keine</span><span class="sxs-lookup"><span data-stu-id="5f05e-142">None</span></span>

## <span data-ttu-id="5f05e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f05e-143">OUTPUTS</span></span>

### <span data-ttu-id="5f05e-144">Microsoft.Azure.Commands.FrontDando.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5f05e-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="5f05e-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5f05e-145">NOTES</span></span>

## <span data-ttu-id="5f05e-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5f05e-146">RELATED LINKS</span></span>

<span data-ttu-id="5f05e-147">[Get-AzFrontDlicWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDlicWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDlicWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDullWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDneuWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="5f05e-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
