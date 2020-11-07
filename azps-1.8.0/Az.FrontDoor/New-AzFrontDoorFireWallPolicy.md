---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 67caf6c97c493ad1d19b95ef00c896cb96a47582
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820048"
---
# <span data-ttu-id="ca435-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="ca435-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="ca435-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca435-102">SYNOPSIS</span></span>
<span data-ttu-id="ca435-103">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ca435-103">Create WAF policy</span></span>

## <span data-ttu-id="ca435-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca435-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca435-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca435-105">DESCRIPTION</span></span>
<span data-ttu-id="ca435-106">Das Cmdlet **New-AzFrontDoorFireWallPolicy** erstellt eine neue Azure WAF-Richtlinie in der angegebenen Ressourcengruppe unter Aktuelles Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca435-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="ca435-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca435-107">EXAMPLES</span></span>

### <span data-ttu-id="ca435-108">Beispiel 1: Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ca435-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="ca435-109">Erstellen einer WAF-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ca435-109">Create WAF policy</span></span>

## <span data-ttu-id="ca435-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca435-110">PARAMETERS</span></span>

### <span data-ttu-id="ca435-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="ca435-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="ca435-112">Benutzerdefinierter Antworttext</span><span class="sxs-lookup"><span data-stu-id="ca435-112">Custom Response Body</span></span>

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

### <span data-ttu-id="ca435-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="ca435-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="ca435-114">Benutzerdefinierter Antwort Status Code</span><span class="sxs-lookup"><span data-stu-id="ca435-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="ca435-115">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="ca435-115">-Customrule</span></span>
<span data-ttu-id="ca435-116">Benutzerdefinierte Regeln in der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ca435-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="ca435-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca435-117">-DefaultProfile</span></span>
<span data-ttu-id="ca435-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca435-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca435-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ca435-119">-EnabledState</span></span>
<span data-ttu-id="ca435-120">Gibt an, ob sich die Richtlinie im Status "aktiviert" oder "deaktiviert" befindet.</span><span class="sxs-lookup"><span data-stu-id="ca435-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="ca435-121">Mögliche Werte sind: "deaktiviert", "aktiviert"</span><span class="sxs-lookup"><span data-stu-id="ca435-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="ca435-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="ca435-122">-ManagedRule</span></span>
<span data-ttu-id="ca435-123">Verwaltete Regeln innerhalb der Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ca435-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="ca435-124">-Modus</span><span class="sxs-lookup"><span data-stu-id="ca435-124">-Mode</span></span>
<span data-ttu-id="ca435-125">Beschreibt, ob sich der Erkennungsmodus oder der verhindermodus auf Richtlinienebene befindet.</span><span class="sxs-lookup"><span data-stu-id="ca435-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="ca435-126">Mögliche Werte sind: "Vorbeugung", "Erkennung"</span><span class="sxs-lookup"><span data-stu-id="ca435-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="ca435-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ca435-127">-Name</span></span>
<span data-ttu-id="ca435-128">WebApplicationFireWallPolicy-Name.</span><span class="sxs-lookup"><span data-stu-id="ca435-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="ca435-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="ca435-129">-RedirectUrl</span></span>
<span data-ttu-id="ca435-130">URL umleiten</span><span class="sxs-lookup"><span data-stu-id="ca435-130">Redirect URL</span></span>

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

### <span data-ttu-id="ca435-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca435-131">-ResourceGroupName</span></span>
<span data-ttu-id="ca435-132">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ca435-132">The resource group name</span></span>

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

### <span data-ttu-id="ca435-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ca435-133">-Confirm</span></span>
<span data-ttu-id="ca435-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca435-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca435-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca435-135">-WhatIf</span></span>
<span data-ttu-id="ca435-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca435-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca435-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca435-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca435-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca435-138">CommonParameters</span></span>
<span data-ttu-id="ca435-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca435-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca435-140">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca435-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca435-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca435-141">INPUTS</span></span>

### <span data-ttu-id="ca435-142">Keine</span><span class="sxs-lookup"><span data-stu-id="ca435-142">None</span></span>

## <span data-ttu-id="ca435-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca435-143">OUTPUTS</span></span>

### <span data-ttu-id="ca435-144">Microsoft. Azure. Commands. Haustür. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ca435-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="ca435-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca435-145">NOTES</span></span>

## <span data-ttu-id="ca435-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca435-146">RELATED LINKS</span></span>

<span data-ttu-id="ca435-147">[Satz-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [Neu – AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [Neu – AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="ca435-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
