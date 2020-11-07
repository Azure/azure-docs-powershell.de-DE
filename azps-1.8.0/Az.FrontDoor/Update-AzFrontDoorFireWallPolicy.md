---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 3e0502d3503bdbf95fb81c779829b73e896b150f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819988"
---
# <span data-ttu-id="21064-101">Update-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="21064-101">Update-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="21064-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21064-102">SYNOPSIS</span></span>
<span data-ttu-id="21064-103">Aktualisieren der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="21064-103">Update WAF policy</span></span>

## <span data-ttu-id="21064-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21064-104">SYNTAX</span></span>

### <span data-ttu-id="21064-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21064-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21064-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21064-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21064-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21064-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21064-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21064-108">DESCRIPTION</span></span>
<span data-ttu-id="21064-109">Das Cmdlet **Update-AzFrontDoorFireWallPolicy** aktualisiert eine vorhandene WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="21064-109">The **Update-AzFrontDoorFireWallPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="21064-110">Wenn keine Eingabeparameter bereitgestellt werden, werden alte Parameter aus der vorhandenen WAF-Richtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="21064-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="21064-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21064-111">EXAMPLES</span></span>

### <span data-ttu-id="21064-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21064-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="21064-113">Aktualisieren eines vorhandenen benutzerdefinierten WAF-Richtlinien Codes</span><span class="sxs-lookup"><span data-stu-id="21064-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="21064-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="21064-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="21064-115">Aktualisieren eines vorhandenen WAF-Richtlinienmodus</span><span class="sxs-lookup"><span data-stu-id="21064-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="21064-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="21064-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="21064-117">Aktualisieren einer vorhandenen WAF-Richtlinie mit aktiviertem Status und Modus.</span><span class="sxs-lookup"><span data-stu-id="21064-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="21064-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="21064-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorFireWallPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="21064-119">Aktualisieren aller WAF-Richtlinien in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21064-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="21064-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="21064-120">PARAMETERS</span></span>

### <span data-ttu-id="21064-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="21064-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="21064-122">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="21064-122">Custom Response Body</span></span>

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

### <span data-ttu-id="21064-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="21064-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="21064-124">Benutzerdefinierter Antwort Status Code</span><span class="sxs-lookup"><span data-stu-id="21064-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="21064-125">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="21064-125">-Customrule</span></span>
<span data-ttu-id="21064-126">Benutzerdefinierte Regeln in der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="21064-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="21064-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21064-127">-DefaultProfile</span></span>
<span data-ttu-id="21064-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21064-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21064-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="21064-129">-EnabledState</span></span>
<span data-ttu-id="21064-130">Gibt an, ob sich die Richtlinie im Status "aktiviert" oder "deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="21064-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="21064-131">Mögliche Werte sind: "deaktiviert", "aktiviert"</span><span class="sxs-lookup"><span data-stu-id="21064-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="21064-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21064-132">-InputObject</span></span>
<span data-ttu-id="21064-133">Das zu Aktualisier FireWallPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="21064-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="21064-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="21064-134">-ManagedRule</span></span>
<span data-ttu-id="21064-135">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="21064-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="21064-136">-Modus</span><span class="sxs-lookup"><span data-stu-id="21064-136">-Mode</span></span>
<span data-ttu-id="21064-137">Beschreibt, ob sich der Erkennungsmodus oder der verhindermodus auf Richtlinienebene befindet.</span><span class="sxs-lookup"><span data-stu-id="21064-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="21064-138">Mögliche Werte sind: "Vorbeugung", "Erkennung"</span><span class="sxs-lookup"><span data-stu-id="21064-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="21064-139">-Name</span><span class="sxs-lookup"><span data-stu-id="21064-139">-Name</span></span>
<span data-ttu-id="21064-140">Der Name des zu Aktualisier FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="21064-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="21064-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="21064-141">-RedirectUrl</span></span>
<span data-ttu-id="21064-142">URL umleiten</span><span class="sxs-lookup"><span data-stu-id="21064-142">Redirect URL</span></span>

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

### <span data-ttu-id="21064-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21064-143">-ResourceGroupName</span></span>
<span data-ttu-id="21064-144">Die Ressourcengruppe, zu der die FireWallPolicy gehört.</span><span class="sxs-lookup"><span data-stu-id="21064-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="21064-145">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="21064-145">-ResourceId</span></span>
<span data-ttu-id="21064-146">Ressourcen-ID des zu Aktualisier FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="21064-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="21064-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21064-147">-Confirm</span></span>
<span data-ttu-id="21064-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21064-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21064-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21064-149">-WhatIf</span></span>
<span data-ttu-id="21064-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21064-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21064-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21064-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21064-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21064-152">CommonParameters</span></span>
<span data-ttu-id="21064-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21064-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21064-154">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21064-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21064-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21064-155">INPUTS</span></span>

### <span data-ttu-id="21064-156">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="21064-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="21064-157">System. String</span><span class="sxs-lookup"><span data-stu-id="21064-157">System.String</span></span>

## <span data-ttu-id="21064-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21064-158">OUTPUTS</span></span>

### <span data-ttu-id="21064-159">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="21064-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="21064-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="21064-160">NOTES</span></span>

## <span data-ttu-id="21064-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21064-161">RELATED LINKS</span></span>

<span data-ttu-id="21064-162">[Neu – AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Neu – AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [Neu – AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="21064-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
