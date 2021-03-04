---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e643bf488073f6da685265cea4a2a0c6cb7cebf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927872"
---
# <span data-ttu-id="8b316-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8b316-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="8b316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b316-102">SYNOPSIS</span></span>
<span data-ttu-id="8b316-103">Erstellt eine Anwendungsgatewayfirewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8b316-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="8b316-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b316-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b316-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b316-105">DESCRIPTION</span></span>
<span data-ttu-id="8b316-106">Das **Cmdlet New-AzApplicationGatewayFirewallPolicy** erstellt eine Firewallrichtlinie für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8b316-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="8b316-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b316-107">EXAMPLES</span></span>

### <span data-ttu-id="8b316-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b316-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="8b316-109">Mit diesem Befehl wird eine neue Azure-Anwendungsgatewayfirewallrichtlinie mit dem Namen "wafResource1" in der Ressourcengruppe "rg1" am Speicherort "westus" mit benutzerdefinierten Regeln erstellt, die in der Variablen "$customRule" definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8b316-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="8b316-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8b316-110">PARAMETERS</span></span>

### <span data-ttu-id="8b316-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b316-111">-AsJob</span></span>
<span data-ttu-id="8b316-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8b316-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b316-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="8b316-113">-CustomRule</span></span>
<span data-ttu-id="8b316-114">Die Liste der CustomRules</span><span class="sxs-lookup"><span data-stu-id="8b316-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="8b316-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b316-115">-DefaultProfile</span></span>
<span data-ttu-id="8b316-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b316-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b316-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8b316-117">-Force</span></span>
<span data-ttu-id="8b316-118">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="8b316-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8b316-119">-Location</span><span class="sxs-lookup"><span data-stu-id="8b316-119">-Location</span></span>
<span data-ttu-id="8b316-120">speicherort.</span><span class="sxs-lookup"><span data-stu-id="8b316-120">location.</span></span>

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

### <span data-ttu-id="8b316-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8b316-121">-ManagedRule</span></span>
<span data-ttu-id="8b316-122">Einstellung für verwaltete Regeln</span><span class="sxs-lookup"><span data-stu-id="8b316-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="8b316-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8b316-123">-Name</span></span>
<span data-ttu-id="8b316-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8b316-124">The resource name.</span></span>

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

### <span data-ttu-id="8b316-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="8b316-125">-PolicySetting</span></span>
<span data-ttu-id="8b316-126">Richtlinieneinstellungen für die Webanwendungsfirewall</span><span class="sxs-lookup"><span data-stu-id="8b316-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="8b316-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b316-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b316-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8b316-128">The resource group name.</span></span>

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

### <span data-ttu-id="8b316-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b316-129">-Tag</span></span>
<span data-ttu-id="8b316-130">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b316-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8b316-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b316-131">-Confirm</span></span>
<span data-ttu-id="8b316-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b316-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b316-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b316-133">-WhatIf</span></span>
<span data-ttu-id="8b316-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b316-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b316-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b316-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b316-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b316-136">CommonParameters</span></span>
<span data-ttu-id="8b316-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b316-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b316-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b316-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b316-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b316-139">INPUTS</span></span>

### <span data-ttu-id="8b316-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8b316-140">System.String</span></span>

### <span data-ttu-id="8b316-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="8b316-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="8b316-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="8b316-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="8b316-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="8b316-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="8b316-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b316-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8b316-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b316-145">OUTPUTS</span></span>

### <span data-ttu-id="8b316-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8b316-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="8b316-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8b316-147">NOTES</span></span>

## <span data-ttu-id="8b316-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8b316-148">RELATED LINKS</span></span>
