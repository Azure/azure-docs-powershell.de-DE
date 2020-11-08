---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995863"
---
# <span data-ttu-id="c94b7-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="c94b7-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="c94b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c94b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c94b7-103">Aktualisieren der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c94b7-103">Update WAF policy</span></span>

## <span data-ttu-id="c94b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c94b7-104">SYNTAX</span></span>

### <span data-ttu-id="c94b7-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c94b7-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c94b7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c94b7-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c94b7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c94b7-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c94b7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c94b7-108">DESCRIPTION</span></span>
<span data-ttu-id="c94b7-109">Das Cmdlet **Update-AzFrontDoorWafPolicy** aktualisiert eine vorhandene WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="c94b7-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="c94b7-110">Wenn keine Eingabeparameter bereitgestellt werden, werden alte Parameter aus der vorhandenen WAF-Richtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="c94b7-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="c94b7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c94b7-111">EXAMPLES</span></span>

### <span data-ttu-id="c94b7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c94b7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="c94b7-113">Aktualisieren eines vorhandenen benutzerdefinierten WAF-Richtlinien Codes</span><span class="sxs-lookup"><span data-stu-id="c94b7-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="c94b7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c94b7-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="c94b7-115">Aktualisieren eines vorhandenen WAF-Richtlinienmodus</span><span class="sxs-lookup"><span data-stu-id="c94b7-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="c94b7-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c94b7-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="c94b7-117">Aktualisieren einer vorhandenen WAF-Richtlinie mit aktiviertem Status und Modus.</span><span class="sxs-lookup"><span data-stu-id="c94b7-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="c94b7-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="c94b7-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="c94b7-119">Aktualisieren aller WAF-Richtlinien in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c94b7-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="c94b7-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c94b7-120">PARAMETERS</span></span>

### <span data-ttu-id="c94b7-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="c94b7-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="c94b7-122">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="c94b7-122">Custom Response Body</span></span>

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

### <span data-ttu-id="c94b7-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="c94b7-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="c94b7-124">Benutzerdefinierter Antwort Status Code</span><span class="sxs-lookup"><span data-stu-id="c94b7-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="c94b7-125">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="c94b7-125">-Customrule</span></span>
<span data-ttu-id="c94b7-126">Benutzerdefinierte Regeln in der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c94b7-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="c94b7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c94b7-127">-DefaultProfile</span></span>
<span data-ttu-id="c94b7-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c94b7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c94b7-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c94b7-129">-EnabledState</span></span>
<span data-ttu-id="c94b7-130">Gibt an, ob sich die Richtlinie im Status "aktiviert" oder "deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="c94b7-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="c94b7-131">Mögliche Werte sind: "deaktiviert", "aktiviert"</span><span class="sxs-lookup"><span data-stu-id="c94b7-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="c94b7-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c94b7-132">-InputObject</span></span>
<span data-ttu-id="c94b7-133">Das zu Aktualisier FireWallPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c94b7-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="c94b7-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="c94b7-134">-ManagedRule</span></span>
<span data-ttu-id="c94b7-135">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c94b7-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="c94b7-136">-Modus</span><span class="sxs-lookup"><span data-stu-id="c94b7-136">-Mode</span></span>
<span data-ttu-id="c94b7-137">Beschreibt, ob sich der Erkennungsmodus oder der verhindermodus auf Richtlinienebene befindet.</span><span class="sxs-lookup"><span data-stu-id="c94b7-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="c94b7-138">Mögliche Werte sind: "Vorbeugung", "Erkennung"</span><span class="sxs-lookup"><span data-stu-id="c94b7-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="c94b7-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c94b7-139">-Name</span></span>
<span data-ttu-id="c94b7-140">Der Name des zu Aktualisier FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="c94b7-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="c94b7-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="c94b7-141">-RedirectUrl</span></span>
<span data-ttu-id="c94b7-142">URL umleiten</span><span class="sxs-lookup"><span data-stu-id="c94b7-142">Redirect URL</span></span>

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

### <span data-ttu-id="c94b7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c94b7-143">-ResourceGroupName</span></span>
<span data-ttu-id="c94b7-144">Die Ressourcengruppe, zu der die FireWallPolicy gehört.</span><span class="sxs-lookup"><span data-stu-id="c94b7-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="c94b7-145">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c94b7-145">-ResourceId</span></span>
<span data-ttu-id="c94b7-146">Ressourcen-ID des zu Aktualisier FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="c94b7-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="c94b7-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c94b7-147">-Confirm</span></span>
<span data-ttu-id="c94b7-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c94b7-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c94b7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c94b7-149">-WhatIf</span></span>
<span data-ttu-id="c94b7-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c94b7-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c94b7-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c94b7-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c94b7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c94b7-152">CommonParameters</span></span>
<span data-ttu-id="c94b7-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c94b7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c94b7-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c94b7-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c94b7-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c94b7-155">INPUTS</span></span>

### <span data-ttu-id="c94b7-156">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c94b7-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="c94b7-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c94b7-157">System.String</span></span>

## <span data-ttu-id="c94b7-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c94b7-158">OUTPUTS</span></span>

### <span data-ttu-id="c94b7-159">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c94b7-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="c94b7-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="c94b7-160">NOTES</span></span>

## <span data-ttu-id="c94b7-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c94b7-161">RELATED LINKS</span></span>

<span data-ttu-id="c94b7-162">[Neu – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Neu – AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [Neu – AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="c94b7-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
