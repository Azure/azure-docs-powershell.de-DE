---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996104"
---
# <span data-ttu-id="b26b1-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b26b1-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="b26b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b26b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b26b1-103">Aktualisiert eine Firewall-Richtlinie für Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="b26b1-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="b26b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b26b1-104">SYNTAX</span></span>

### <span data-ttu-id="b26b1-105">ByFactoryObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b26b1-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26b1-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="b26b1-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b26b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b26b1-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b26b1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b26b1-108">DESCRIPTION</span></span>
<span data-ttu-id="b26b1-109">Das Cmdlet " **Satz-AzApplicationGatewayFirewallPolicy** " aktualisiert eine Azure Application Gateway-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b26b1-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="b26b1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b26b1-110">EXAMPLES</span></span>

### <span data-ttu-id="b26b1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b26b1-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="b26b1-112">Dieser Befehl aktualisiert die Firewall-Richtlinie des Anwendungs Gateways mit den Einstellungen in der $AppGwFirewallPolicy-Variable und speichert das aktualisierte Gateway in der $UpdatedAppGwFirewallPolicy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b26b1-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="b26b1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b26b1-113">PARAMETERS</span></span>

### <span data-ttu-id="b26b1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b26b1-114">-AsJob</span></span>
<span data-ttu-id="b26b1-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b26b1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b26b1-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="b26b1-116">-CustomRule</span></span>
<span data-ttu-id="b26b1-117">Die Liste der customrules</span><span class="sxs-lookup"><span data-stu-id="b26b1-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="b26b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b26b1-118">-DefaultProfile</span></span>
<span data-ttu-id="b26b1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b26b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b26b1-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b26b1-120">-InputObject</span></span>
<span data-ttu-id="b26b1-121">Die applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b26b1-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="b26b1-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b26b1-122">-ManagedRule</span></span>
<span data-ttu-id="b26b1-123">ManagedRules der Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b26b1-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="b26b1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b26b1-124">-Name</span></span>
<span data-ttu-id="b26b1-125">Der Name der Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b26b1-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="b26b1-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="b26b1-126">-PolicySetting</span></span>
<span data-ttu-id="b26b1-127">Policysettings der Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="b26b1-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="b26b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="b26b1-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b26b1-129">The resource group name.</span></span>

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

### <span data-ttu-id="b26b1-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b26b1-130">-ResourceId</span></span>
<span data-ttu-id="b26b1-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b26b1-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b26b1-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b26b1-132">-Confirm</span></span>
<span data-ttu-id="b26b1-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b26b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b26b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26b1-134">-WhatIf</span></span>
<span data-ttu-id="b26b1-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b26b1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b26b1-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b26b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b26b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26b1-137">CommonParameters</span></span>
<span data-ttu-id="b26b1-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b26b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26b1-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b26b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26b1-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b26b1-140">INPUTS</span></span>

### <span data-ttu-id="b26b1-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b26b1-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="b26b1-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b26b1-142">OUTPUTS</span></span>

### <span data-ttu-id="b26b1-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b26b1-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="b26b1-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b26b1-144">NOTES</span></span>

## <span data-ttu-id="b26b1-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b26b1-145">RELATED LINKS</span></span>
