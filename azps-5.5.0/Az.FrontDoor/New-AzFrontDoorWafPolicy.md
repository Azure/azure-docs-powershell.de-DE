---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 7e382683398ae0fcb0da239240e967b2001c565d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175428"
---
# <span data-ttu-id="aab8c-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="aab8c-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="aab8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab8c-102">SYNOPSIS</span></span>
<span data-ttu-id="aab8c-103">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aab8c-103">Create WAF policy</span></span>

## <span data-ttu-id="aab8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aab8c-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab8c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aab8c-105">DESCRIPTION</span></span>
<span data-ttu-id="aab8c-106">Das **Cmdlet "New-AzFrontDlicWafPolicy"** erstellt eine neue Azure -WAF-Richtlinie in der angegebenen Ressourcengruppe unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aab8c-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="aab8c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aab8c-107">EXAMPLES</span></span>

### <span data-ttu-id="aab8c-108">Beispiel 1: Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aab8c-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="aab8c-109">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aab8c-109">Create WAF policy</span></span>

## <span data-ttu-id="aab8c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aab8c-110">PARAMETERS</span></span>

### <span data-ttu-id="aab8c-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="aab8c-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="aab8c-112">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="aab8c-112">Custom Response Body</span></span>

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

### <span data-ttu-id="aab8c-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="aab8c-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="aab8c-114">Benutzerdefinierter Antwortstatuscode</span><span class="sxs-lookup"><span data-stu-id="aab8c-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="aab8c-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="aab8c-115">-Customrule</span></span>
<span data-ttu-id="aab8c-116">Benutzerdefinierte Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aab8c-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="aab8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab8c-117">-DefaultProfile</span></span>
<span data-ttu-id="aab8c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aab8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab8c-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="aab8c-119">-EnabledState</span></span>
<span data-ttu-id="aab8c-120">Gibt an, ob sich die Richtlinie im Status "Aktiviert" oder "Deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="aab8c-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="aab8c-121">Mögliche Werte sind: "Disabled", "Enabled".</span><span class="sxs-lookup"><span data-stu-id="aab8c-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="aab8c-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="aab8c-122">-ManagedRule</span></span>
<span data-ttu-id="aab8c-123">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aab8c-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="aab8c-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="aab8c-124">-Mode</span></span>
<span data-ttu-id="aab8c-125">Beschreibt, ob er sich auf Richtlinienebene im Erkennungs- oder Verhinderungsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="aab8c-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="aab8c-126">Mögliche Werte sind: "Verhinderung", "Erkennung".</span><span class="sxs-lookup"><span data-stu-id="aab8c-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="aab8c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="aab8c-127">-Name</span></span>
<span data-ttu-id="aab8c-128">Name von WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="aab8c-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="aab8c-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="aab8c-129">-RedirectUrl</span></span>
<span data-ttu-id="aab8c-130">Umleitungs-URL</span><span class="sxs-lookup"><span data-stu-id="aab8c-130">Redirect URL</span></span>

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

### <span data-ttu-id="aab8c-131">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="aab8c-131">-RequestBodyCheck</span></span>
<span data-ttu-id="aab8c-132">Definiert, ob der Textkörper von verwalteten Regeln überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="aab8c-132">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="aab8c-133">Mögliche Werte sind: "Enabled", "Disabled".</span><span class="sxs-lookup"><span data-stu-id="aab8c-133">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="aab8c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab8c-134">-ResourceGroupName</span></span>
<span data-ttu-id="aab8c-135">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aab8c-135">The resource group name</span></span>

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

### <span data-ttu-id="aab8c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aab8c-136">-Confirm</span></span>
<span data-ttu-id="aab8c-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aab8c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab8c-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aab8c-138">-WhatIf</span></span>
<span data-ttu-id="aab8c-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aab8c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aab8c-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aab8c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab8c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab8c-141">CommonParameters</span></span>
<span data-ttu-id="aab8c-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab8c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab8c-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aab8c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab8c-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aab8c-144">INPUTS</span></span>

### <span data-ttu-id="aab8c-145">Keine</span><span class="sxs-lookup"><span data-stu-id="aab8c-145">None</span></span>

## <span data-ttu-id="aab8c-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aab8c-146">OUTPUTS</span></span>

### <span data-ttu-id="aab8c-147">Microsoft.Azure.Commands.FrontDando.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="aab8c-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="aab8c-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aab8c-148">NOTES</span></span>

## <span data-ttu-id="aab8c-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aab8c-149">RELATED LINKS</span></span>

<span data-ttu-id="aab8c-150">[Update-AzFrontDlicWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDlicWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDlicWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDullWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDneuWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="aab8c-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
