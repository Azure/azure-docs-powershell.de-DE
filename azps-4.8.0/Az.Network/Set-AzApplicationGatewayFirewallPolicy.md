---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009063"
---
# <span data-ttu-id="b119c-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b119c-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="b119c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b119c-102">SYNOPSIS</span></span>
<span data-ttu-id="b119c-103">Aktualisiert eine Firewall-Richtlinie für Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="b119c-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="b119c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b119c-104">SYNTAX</span></span>

### <span data-ttu-id="b119c-105">ByFactoryObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b119c-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b119c-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="b119c-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b119c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b119c-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b119c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b119c-108">DESCRIPTION</span></span>
<span data-ttu-id="b119c-109">Das Cmdlet " **Satz-AzApplicationGatewayFirewallPolicy** " aktualisiert eine Azure Application Gateway-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b119c-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="b119c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b119c-110">EXAMPLES</span></span>

### <span data-ttu-id="b119c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b119c-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="b119c-112">Dieser Befehl aktualisiert die Firewall-Richtlinie des Anwendungs Gateways mit den Einstellungen in der $AppGwFirewallPolicy-Variable und speichert das aktualisierte Gateway in der $UpdatedAppGwFirewallPolicy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b119c-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="b119c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b119c-113">PARAMETERS</span></span>

### <span data-ttu-id="b119c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b119c-114">-AsJob</span></span>
<span data-ttu-id="b119c-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b119c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b119c-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="b119c-116">-CustomRule</span></span>
<span data-ttu-id="b119c-117">Die Liste der customrules</span><span class="sxs-lookup"><span data-stu-id="b119c-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="b119c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b119c-118">-DefaultProfile</span></span>
<span data-ttu-id="b119c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b119c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b119c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b119c-120">-InputObject</span></span>
<span data-ttu-id="b119c-121">Die applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b119c-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="b119c-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b119c-122">-ManagedRule</span></span>
<span data-ttu-id="b119c-123">ManagedRules der Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b119c-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="b119c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b119c-124">-Name</span></span>
<span data-ttu-id="b119c-125">Der Name der Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b119c-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="b119c-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="b119c-126">-PolicySetting</span></span>
<span data-ttu-id="b119c-127">Policysettings der Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b119c-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="b119c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b119c-128">-ResourceGroupName</span></span>
<span data-ttu-id="b119c-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b119c-129">The resource group name.</span></span>

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

### <span data-ttu-id="b119c-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b119c-130">-ResourceId</span></span>
<span data-ttu-id="b119c-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b119c-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b119c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b119c-132">-Confirm</span></span>
<span data-ttu-id="b119c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b119c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b119c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b119c-134">-WhatIf</span></span>
<span data-ttu-id="b119c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b119c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b119c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b119c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b119c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b119c-137">CommonParameters</span></span>
<span data-ttu-id="b119c-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b119c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b119c-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b119c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b119c-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b119c-140">INPUTS</span></span>

### <span data-ttu-id="b119c-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b119c-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="b119c-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b119c-142">OUTPUTS</span></span>

### <span data-ttu-id="b119c-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b119c-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="b119c-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b119c-144">NOTES</span></span>

## <span data-ttu-id="b119c-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b119c-145">RELATED LINKS</span></span>
