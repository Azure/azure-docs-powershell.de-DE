---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178781"
---
# <span data-ttu-id="0421f-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0421f-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="0421f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0421f-102">SYNOPSIS</span></span>
<span data-ttu-id="0421f-103">Erstellt eine Firewall-Richtlinie für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0421f-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="0421f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0421f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0421f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0421f-105">DESCRIPTION</span></span>
<span data-ttu-id="0421f-106">Das Cmdlet **New-AzApplicationGatewayFirewallPolicy** erstellt eine Firewall-Richtlinie für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0421f-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="0421f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0421f-107">EXAMPLES</span></span>

### <span data-ttu-id="0421f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0421f-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="0421f-109">Dieser Befehl erstellt eine neue Azure Application Gateway-Firewallrichtlinie mit dem Namen "wafResource1" in der Ressourcengruppe "RG1" an Ort "westus" mit benutzerdefinierten Regeln, die in der $CustomRule Variablen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0421f-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="0421f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0421f-110">PARAMETERS</span></span>

### <span data-ttu-id="0421f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0421f-111">-AsJob</span></span>
<span data-ttu-id="0421f-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0421f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0421f-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="0421f-113">-CustomRule</span></span>
<span data-ttu-id="0421f-114">Die Liste der customrules</span><span class="sxs-lookup"><span data-stu-id="0421f-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0421f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0421f-115">-DefaultProfile</span></span>
<span data-ttu-id="0421f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0421f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0421f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0421f-117">-Force</span></span>
<span data-ttu-id="0421f-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="0421f-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0421f-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="0421f-119">-Location</span></span>
<span data-ttu-id="0421f-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="0421f-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0421f-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0421f-121">-ManagedRule</span></span>
<span data-ttu-id="0421f-122">Einstellung für verwaltete Regel</span><span class="sxs-lookup"><span data-stu-id="0421f-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0421f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0421f-123">-Name</span></span>
<span data-ttu-id="0421f-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0421f-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0421f-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="0421f-125">-PolicySetting</span></span>
<span data-ttu-id="0421f-126">Richtlinieneinstellungen für Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="0421f-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0421f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0421f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0421f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0421f-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0421f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="0421f-129">-Tag</span></span>
<span data-ttu-id="0421f-130">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0421f-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0421f-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0421f-131">-Confirm</span></span>
<span data-ttu-id="0421f-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0421f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0421f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0421f-133">-WhatIf</span></span>
<span data-ttu-id="0421f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0421f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0421f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0421f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0421f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0421f-136">CommonParameters</span></span>
<span data-ttu-id="0421f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0421f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0421f-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0421f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0421f-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0421f-139">INPUTS</span></span>

### <span data-ttu-id="0421f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0421f-140">System.String</span></span>

### <span data-ttu-id="0421f-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="0421f-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="0421f-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="0421f-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="0421f-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="0421f-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="0421f-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0421f-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0421f-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0421f-145">OUTPUTS</span></span>

### <span data-ttu-id="0421f-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0421f-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="0421f-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="0421f-147">NOTES</span></span>

## <span data-ttu-id="0421f-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0421f-148">RELATED LINKS</span></span>
