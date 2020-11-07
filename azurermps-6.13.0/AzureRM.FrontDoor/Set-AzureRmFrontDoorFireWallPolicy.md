---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662174"
---
# <span data-ttu-id="d29dd-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="d29dd-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="d29dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d29dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d29dd-103">Aktualisieren der WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d29dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d29dd-104">SYNTAX</span></span>

### <span data-ttu-id="d29dd-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d29dd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d29dd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d29dd-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d29dd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d29dd-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d29dd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d29dd-108">DESCRIPTION</span></span>
<span data-ttu-id="d29dd-109">Das Cmdlet " **Satz-AzureRmFrontDoor** " aktualisiert eine vorhandene WAF-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d29dd-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="d29dd-110">Wenn keine Eingabeparameter bereitgestellt werden, werden alte Parameter aus der vorhandenen WAF-Richtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="d29dd-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="d29dd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d29dd-111">EXAMPLES</span></span>

### <span data-ttu-id="d29dd-112">Beispiel 1: Aktualisieren einer vorhandenen WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d29dd-113">Aktualisieren einer vorhandenen WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-113">update an existing WAF policy</span></span>

### <span data-ttu-id="d29dd-114">Beispiel 2: Aktualisieren einer vorhandenen WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d29dd-115">Aktualisieren einer vorhandenen WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-115">update an existing WAF policy</span></span>

### <span data-ttu-id="d29dd-116">Beispiel 3: Aktualisieren einer vorhandenen WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d29dd-117">Aktualisieren einer vorhandenen WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-117">update an existing WAF policy</span></span>

### <span data-ttu-id="d29dd-118">Beispiel 4: Aktualisieren aller WAF-Richtlinien in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="d29dd-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="d29dd-119">Aktualisieren aller WAF-Richtlinien in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="d29dd-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="d29dd-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d29dd-120">PARAMETERS</span></span>

### <span data-ttu-id="d29dd-121">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="d29dd-121">-Customrule</span></span>
<span data-ttu-id="d29dd-122">Benutzerdefinierte Regeln in der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-122">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="d29dd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29dd-123">-DefaultProfile</span></span>
<span data-ttu-id="d29dd-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d29dd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d29dd-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d29dd-125">-EnabledState</span></span>
<span data-ttu-id="d29dd-126">Gibt an, ob sich die Richtlinie im Status "aktiviert" oder "deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="d29dd-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="d29dd-127">Mögliche Werte sind: "deaktiviert", "aktiviert"</span><span class="sxs-lookup"><span data-stu-id="d29dd-127">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="d29dd-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d29dd-128">-InputObject</span></span>
<span data-ttu-id="d29dd-129">Das zu Aktualisier FireWallPolicy-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d29dd-129">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="d29dd-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d29dd-130">-ManagedRule</span></span>
<span data-ttu-id="d29dd-131">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d29dd-131">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="d29dd-132">-Modus</span><span class="sxs-lookup"><span data-stu-id="d29dd-132">-Mode</span></span>
<span data-ttu-id="d29dd-133">Beschreibt, ob sich der Erkennungsmodus oder der verhindermodus auf Richtlinienebene befindet.</span><span class="sxs-lookup"><span data-stu-id="d29dd-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="d29dd-134">Mögliche Werte sind: "Vorbeugung", "Erkennung"</span><span class="sxs-lookup"><span data-stu-id="d29dd-134">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="d29dd-135">-Name</span><span class="sxs-lookup"><span data-stu-id="d29dd-135">-Name</span></span>
<span data-ttu-id="d29dd-136">Der Name des zu Aktualisier FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="d29dd-136">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="d29dd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d29dd-137">-ResourceGroupName</span></span>
<span data-ttu-id="d29dd-138">Die Ressourcengruppe, zu der die FireWallPolicy gehört.</span><span class="sxs-lookup"><span data-stu-id="d29dd-138">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="d29dd-139">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d29dd-139">-ResourceId</span></span>
<span data-ttu-id="d29dd-140">Ressourcen-ID des zu Aktualisier FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="d29dd-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d29dd-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d29dd-141">-Confirm</span></span>
<span data-ttu-id="d29dd-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d29dd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d29dd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d29dd-143">-WhatIf</span></span>
<span data-ttu-id="d29dd-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d29dd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d29dd-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d29dd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d29dd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29dd-146">CommonParameters</span></span>
<span data-ttu-id="d29dd-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d29dd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29dd-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29dd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29dd-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d29dd-149">INPUTS</span></span>

### <span data-ttu-id="d29dd-150">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d29dd-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="d29dd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d29dd-151">System.String</span></span>

## <span data-ttu-id="d29dd-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d29dd-152">OUTPUTS</span></span>

### <span data-ttu-id="d29dd-153">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d29dd-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="d29dd-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="d29dd-154">NOTES</span></span>

## <span data-ttu-id="d29dd-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d29dd-155">RELATED LINKS</span></span>

<span data-ttu-id="d29dd-156">[Neu – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Neu – AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [Neu – AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="d29dd-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
