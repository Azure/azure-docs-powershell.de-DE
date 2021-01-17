---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458603"
---
# <span data-ttu-id="0bd09-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="0bd09-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="0bd09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd09-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd09-103">Aktualisieren der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="0bd09-103">Update WAF policy</span></span>

## <span data-ttu-id="0bd09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bd09-104">SYNTAX</span></span>

### <span data-ttu-id="0bd09-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0bd09-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bd09-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd09-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bd09-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bd09-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bd09-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bd09-108">DESCRIPTION</span></span>
<span data-ttu-id="0bd09-109">Das **Cmdlet "Update-AzFrontDlicWafPolicy"** aktualisiert eine vorhandene WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0bd09-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="0bd09-110">Wenn keine Eingabeparameter bereitgestellt werden, werden alte Parameter aus der vorhandenen WAF-Richtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="0bd09-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="0bd09-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bd09-111">EXAMPLES</span></span>

### <span data-ttu-id="0bd09-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bd09-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="0bd09-113">Aktualisieren sie einen vorhandenen benutzerdefinierten Statuscode der WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0bd09-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="0bd09-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0bd09-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="0bd09-115">Aktualisieren sie einen vorhandenen WAF-Richtlinienmodus.</span><span class="sxs-lookup"><span data-stu-id="0bd09-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="0bd09-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0bd09-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="0bd09-117">Aktualisieren eines vorhandenen Zustands und Modus mit aktivierter WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0bd09-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="0bd09-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="0bd09-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="0bd09-119">Aktualisieren aller RICHTLINIEN in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd09-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="0bd09-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bd09-120">PARAMETERS</span></span>

### <span data-ttu-id="0bd09-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="0bd09-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="0bd09-122">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="0bd09-122">Custom Response Body</span></span>

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

### <span data-ttu-id="0bd09-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="0bd09-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="0bd09-124">Benutzerdefinierter Antwortstatuscode</span><span class="sxs-lookup"><span data-stu-id="0bd09-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="0bd09-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="0bd09-125">-Customrule</span></span>
<span data-ttu-id="0bd09-126">Benutzerdefinierte Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="0bd09-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="0bd09-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd09-127">-DefaultProfile</span></span>
<span data-ttu-id="0bd09-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bd09-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bd09-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0bd09-129">-EnabledState</span></span>
<span data-ttu-id="0bd09-130">Gibt an, ob sich die Richtlinie im Status "Aktiviert" oder "Deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="0bd09-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="0bd09-131">Mögliche Werte sind: "Disabled", "Enabled".</span><span class="sxs-lookup"><span data-stu-id="0bd09-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="0bd09-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bd09-132">-InputObject</span></span>
<span data-ttu-id="0bd09-133">Das zu aktualisierende FireWallPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0bd09-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="0bd09-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0bd09-134">-ManagedRule</span></span>
<span data-ttu-id="0bd09-135">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="0bd09-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="0bd09-136">-Mode</span><span class="sxs-lookup"><span data-stu-id="0bd09-136">-Mode</span></span>
<span data-ttu-id="0bd09-137">Beschreibt, ob er sich auf Richtlinienebene im Erkennungs- oder Verhinderungsmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="0bd09-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="0bd09-138">Mögliche Werte sind: "Verhinderung", "Erkennung".</span><span class="sxs-lookup"><span data-stu-id="0bd09-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="0bd09-139">-Name</span><span class="sxs-lookup"><span data-stu-id="0bd09-139">-Name</span></span>
<span data-ttu-id="0bd09-140">Der Name der zu aktualisierende FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="0bd09-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="0bd09-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="0bd09-141">-RedirectUrl</span></span>
<span data-ttu-id="0bd09-142">Umleitungs-URL</span><span class="sxs-lookup"><span data-stu-id="0bd09-142">Redirect URL</span></span>

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

### <span data-ttu-id="0bd09-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd09-143">-ResourceGroupName</span></span>
<span data-ttu-id="0bd09-144">Die Ressourcengruppe, zu der die FireWallPolicy gehört.</span><span class="sxs-lookup"><span data-stu-id="0bd09-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="0bd09-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bd09-145">-ResourceId</span></span>
<span data-ttu-id="0bd09-146">Ressourcen-ID der zu aktualisierende FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="0bd09-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="0bd09-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bd09-147">-Confirm</span></span>
<span data-ttu-id="0bd09-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bd09-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bd09-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0bd09-149">-WhatIf</span></span>
<span data-ttu-id="0bd09-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bd09-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bd09-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bd09-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bd09-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd09-152">CommonParameters</span></span>
<span data-ttu-id="0bd09-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd09-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd09-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bd09-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd09-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bd09-155">INPUTS</span></span>

### <span data-ttu-id="0bd09-156">Microsoft.Azure.Commands.FrontDando.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0bd09-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="0bd09-157">System.String</span><span class="sxs-lookup"><span data-stu-id="0bd09-157">System.String</span></span>

## <span data-ttu-id="0bd09-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bd09-158">OUTPUTS</span></span>

### <span data-ttu-id="0bd09-159">Microsoft.Azure.Commands.FrontDando.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0bd09-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="0bd09-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0bd09-160">NOTES</span></span>

## <span data-ttu-id="0bd09-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0bd09-161">RELATED LINKS</span></span>

<span data-ttu-id="0bd09-162">[New-AzFrontDlicWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDlicWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDullWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDneuWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="0bd09-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
