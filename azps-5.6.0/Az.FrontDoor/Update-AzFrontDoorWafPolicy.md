---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: bc4aa72d202938b5727245386f3485fbc43a6ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927171"
---
# <span data-ttu-id="043d0-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="043d0-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="043d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="043d0-102">SYNOPSIS</span></span>
<span data-ttu-id="043d0-103">Aktualisieren der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="043d0-103">Update WAF policy</span></span>

## <span data-ttu-id="043d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="043d0-104">SYNTAX</span></span>

### <span data-ttu-id="043d0-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="043d0-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043d0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="043d0-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043d0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="043d0-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="043d0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="043d0-108">DESCRIPTION</span></span>
<span data-ttu-id="043d0-109">Das **Cmdlet Update-AzFrontDoorWafPolicy** aktualisiert eine vorhandene WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="043d0-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="043d0-110">Wenn keine Eingabeparameter angegeben werden, werden alte Parameter aus der vorhandenen WAF-Richtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="043d0-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="043d0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="043d0-111">EXAMPLES</span></span>

### <span data-ttu-id="043d0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="043d0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="043d0-113">Aktualisieren Sie einen vorhandenen benutzerdefinierten Statuscode einer WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="043d0-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="043d0-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="043d0-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="043d0-115">Aktualisieren sie einen vorhandenen WAF-Richtlinienmodus.</span><span class="sxs-lookup"><span data-stu-id="043d0-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="043d0-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="043d0-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="043d0-117">Aktualisieren sie einen vorhandenen Zustand und Modus für eine aktivierte WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="043d0-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="043d0-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="043d0-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="043d0-119">Aktualisieren aller WAF-Richtlinien in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="043d0-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="043d0-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="043d0-120">PARAMETERS</span></span>

### <span data-ttu-id="043d0-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="043d0-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="043d0-122">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="043d0-122">Custom Response Body</span></span>

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

### <span data-ttu-id="043d0-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="043d0-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="043d0-124">Benutzerdefinierter Antwortstatuscode</span><span class="sxs-lookup"><span data-stu-id="043d0-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043d0-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="043d0-125">-Customrule</span></span>
<span data-ttu-id="043d0-126">Benutzerdefinierte Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="043d0-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="043d0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043d0-127">-DefaultProfile</span></span>
<span data-ttu-id="043d0-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="043d0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="043d0-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="043d0-129">-EnabledState</span></span>
<span data-ttu-id="043d0-130">Gibt an, ob sich die Richtlinie im aktivierten oder deaktivierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="043d0-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="043d0-131">Mögliche Werte sind: "Deaktiviert", "Aktiviert"</span><span class="sxs-lookup"><span data-stu-id="043d0-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="043d0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="043d0-132">-InputObject</span></span>
<span data-ttu-id="043d0-133">Das zu aktualisierende FireWallPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="043d0-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="043d0-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="043d0-134">-ManagedRule</span></span>
<span data-ttu-id="043d0-135">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="043d0-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="043d0-136">-Modus</span><span class="sxs-lookup"><span data-stu-id="043d0-136">-Mode</span></span>
<span data-ttu-id="043d0-137">Beschreibt, ob es sich auf Richtlinienebene im Erkennungs- oder Präventionsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="043d0-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="043d0-138">Mögliche Werte sind:'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="043d0-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="043d0-139">-Name</span><span class="sxs-lookup"><span data-stu-id="043d0-139">-Name</span></span>
<span data-ttu-id="043d0-140">Der Name der zu aktualisierende FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="043d0-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043d0-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="043d0-141">-RedirectUrl</span></span>
<span data-ttu-id="043d0-142">URL umleiten</span><span class="sxs-lookup"><span data-stu-id="043d0-142">Redirect URL</span></span>

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

### <span data-ttu-id="043d0-143">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="043d0-143">-RequestBodyCheck</span></span>
<span data-ttu-id="043d0-144">Definiert, ob der Textkörper von verwalteten Regeln überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="043d0-144">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="043d0-145">Mögliche Werte sind: "Aktiviert", "Deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="043d0-145">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="043d0-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="043d0-146">-ResourceGroupName</span></span>
<span data-ttu-id="043d0-147">Die Ressourcengruppe, zu der die FireWallPolicy gehört.</span><span class="sxs-lookup"><span data-stu-id="043d0-147">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043d0-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="043d0-148">-ResourceId</span></span>
<span data-ttu-id="043d0-149">Ressourcen-ID der zu aktualisierende FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="043d0-149">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043d0-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="043d0-150">-Confirm</span></span>
<span data-ttu-id="043d0-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="043d0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043d0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043d0-152">-WhatIf</span></span>
<span data-ttu-id="043d0-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="043d0-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="043d0-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="043d0-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043d0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043d0-155">CommonParameters</span></span>
<span data-ttu-id="043d0-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043d0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043d0-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="043d0-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043d0-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="043d0-158">INPUTS</span></span>

### <span data-ttu-id="043d0-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="043d0-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="043d0-160">System.String</span><span class="sxs-lookup"><span data-stu-id="043d0-160">System.String</span></span>

## <span data-ttu-id="043d0-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="043d0-161">OUTPUTS</span></span>

### <span data-ttu-id="043d0-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="043d0-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="043d0-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="043d0-163">NOTES</span></span>

## <span data-ttu-id="043d0-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="043d0-164">RELATED LINKS</span></span>

<span data-ttu-id="043d0-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="043d0-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
