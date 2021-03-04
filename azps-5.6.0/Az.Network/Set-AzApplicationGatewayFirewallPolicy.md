---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e6b9c873110118392e9380418276bfa0f4d938a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933467"
---
# <span data-ttu-id="15f69-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="15f69-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="15f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f69-102">SYNOPSIS</span></span>
<span data-ttu-id="15f69-103">Aktualisiert eine Anwendungsgatewayfirewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="15f69-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="15f69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15f69-104">SYNTAX</span></span>

### <span data-ttu-id="15f69-105">ByFactoryObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="15f69-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15f69-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="15f69-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15f69-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="15f69-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15f69-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15f69-108">DESCRIPTION</span></span>
<span data-ttu-id="15f69-109">Das **Cmdlet Set-AzApplicationGatewayFirewallPolicy** aktualisiert eine Azure-Anwendungsgateway-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="15f69-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="15f69-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15f69-110">EXAMPLES</span></span>

### <span data-ttu-id="15f69-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15f69-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="15f69-112">Mit diesem Befehl wird die Firewallrichtlinie für das Anwendungsgateway mit den Einstellungen in der $AppGwFirewallPolicy aktualisiert und das aktualisierte Gateway in der $UpdatedAppGwFirewallPolicy gespeichert.</span><span class="sxs-lookup"><span data-stu-id="15f69-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="15f69-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="15f69-113">PARAMETERS</span></span>

### <span data-ttu-id="15f69-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15f69-114">-AsJob</span></span>
<span data-ttu-id="15f69-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="15f69-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15f69-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="15f69-116">-CustomRule</span></span>
<span data-ttu-id="15f69-117">Die Liste der CustomRules</span><span class="sxs-lookup"><span data-stu-id="15f69-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="15f69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f69-118">-DefaultProfile</span></span>
<span data-ttu-id="15f69-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15f69-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15f69-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15f69-120">-InputObject</span></span>
<span data-ttu-id="15f69-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="15f69-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15f69-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="15f69-122">-ManagedRule</span></span>
<span data-ttu-id="15f69-123">Verwaltete Regeln der Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="15f69-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="15f69-124">-Name</span><span class="sxs-lookup"><span data-stu-id="15f69-124">-Name</span></span>
<span data-ttu-id="15f69-125">Der Name der Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="15f69-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f69-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="15f69-126">-PolicySetting</span></span>
<span data-ttu-id="15f69-127">Richtlinieneinstellungen der Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="15f69-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="15f69-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15f69-128">-ResourceGroupName</span></span>
<span data-ttu-id="15f69-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15f69-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15f69-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15f69-130">-ResourceId</span></span>
<span data-ttu-id="15f69-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="15f69-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15f69-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15f69-132">-Confirm</span></span>
<span data-ttu-id="15f69-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15f69-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15f69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15f69-134">-WhatIf</span></span>
<span data-ttu-id="15f69-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15f69-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15f69-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15f69-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15f69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f69-137">CommonParameters</span></span>
<span data-ttu-id="15f69-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15f69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f69-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15f69-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f69-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15f69-140">INPUTS</span></span>

### <span data-ttu-id="15f69-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="15f69-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="15f69-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15f69-142">OUTPUTS</span></span>

### <span data-ttu-id="15f69-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="15f69-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="15f69-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="15f69-144">NOTES</span></span>

## <span data-ttu-id="15f69-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="15f69-145">RELATED LINKS</span></span>
