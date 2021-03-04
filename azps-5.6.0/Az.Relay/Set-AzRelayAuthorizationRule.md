---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 3165905cc86d2255670127cd90c015ce20096c14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943745"
---
# <span data-ttu-id="7a390-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7a390-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="7a390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a390-102">SYNOPSIS</span></span>
<span data-ttu-id="7a390-103">Aktualisiert die angegebene Beschreibung der Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="7a390-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7a390-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a390-104">SYNTAX</span></span>

### <span data-ttu-id="7a390-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a390-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a390-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7a390-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a390-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7a390-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a390-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a390-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a390-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7a390-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a390-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a390-110">DESCRIPTION</span></span>
<span data-ttu-id="7a390-111">Das **Cmdlet Set-AzRelayAuthorizationRule** aktualisiert die Beschreibung für die angegebene Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="7a390-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="7a390-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a390-112">EXAMPLES</span></span>

### <span data-ttu-id="7a390-113">Beispiel 1.1 – Namespace mit InputObject</span><span class="sxs-lookup"><span data-stu-id="7a390-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="7a390-114">Fügt **Senden** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` im Namespace `TestNameSpace-Relay1` hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a390-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="7a390-115">Beispiel 1.2 – Namespace mit Dem Parameter "Rechte"</span><span class="sxs-lookup"><span data-stu-id="7a390-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="7a390-116">Fügt **Senden** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` im Namespace `TestNameSpace-Relay1` hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a390-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="7a390-117">Beispiel 2.1 – WcfRelay mit InputObject</span><span class="sxs-lookup"><span data-stu-id="7a390-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="7a390-118">Fügt **Senden** den Zugriffsrechten der Autorisierungsregel `AuthoRule1` von WcfRelay `TestWCFRelay1` hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a390-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="7a390-119">Beispiel 2.2 – WcfRelay mit dem Parameter "Rechte"</span><span class="sxs-lookup"><span data-stu-id="7a390-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="7a390-120">Fügt **Senden** den Zugriffsrechten der Autorisierungsregel `AuthoRule1` von WcfRelay `TestWCFRelay1` hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a390-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="7a390-121">Beispiel 3.1 – HybridVerbinden mit InputObject</span><span class="sxs-lookup"><span data-stu-id="7a390-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="7a390-122">Fügt **Senden** den Zugriffsrechten der Autorisierungsregel `AuthoRule1` der HybridConnection `TestHybridConnection` hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a390-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="7a390-123">Beispiel 3.2 – Parameter HybridVerbinden mit Rechten</span><span class="sxs-lookup"><span data-stu-id="7a390-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="7a390-124">Fügt **Senden** den Zugriffsrechten der Autorisierungsregel `AuthoRule1` der HybridConnection `TestHybridConnection` hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a390-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="7a390-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7a390-125">PARAMETERS</span></span>

### <span data-ttu-id="7a390-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a390-126">-DefaultProfile</span></span>
<span data-ttu-id="7a390-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a390-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a390-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="7a390-128">-HybridConnection</span></span>
<span data-ttu-id="7a390-129">HybridVerbindeungsname.</span><span class="sxs-lookup"><span data-stu-id="7a390-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a390-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a390-130">-InputObject</span></span>
<span data-ttu-id="7a390-131">Relay AuthorizationRule-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7a390-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a390-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7a390-132">-Name</span></span>
<span data-ttu-id="7a390-133">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="7a390-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a390-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a390-134">-Namespace</span></span>
<span data-ttu-id="7a390-135">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="7a390-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a390-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a390-136">-ResourceGroupName</span></span>
<span data-ttu-id="7a390-137">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="7a390-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a390-138">-Rechte</span><span class="sxs-lookup"><span data-stu-id="7a390-138">-Rights</span></span>
<span data-ttu-id="7a390-139">Rechte, z. B. @("Hören";Senden","Verwalten")</span><span class="sxs-lookup"><span data-stu-id="7a390-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a390-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="7a390-140">-WcfRelay</span></span>
<span data-ttu-id="7a390-141">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="7a390-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a390-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a390-142">-Confirm</span></span>
<span data-ttu-id="7a390-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a390-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a390-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a390-144">-WhatIf</span></span>
<span data-ttu-id="7a390-145">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a390-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a390-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a390-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a390-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a390-147">CommonParameters</span></span>
<span data-ttu-id="7a390-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a390-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a390-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a390-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a390-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a390-150">INPUTS</span></span>

### <span data-ttu-id="7a390-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7a390-151">System.String</span></span>

### <span data-ttu-id="7a390-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7a390-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="7a390-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7a390-153">System.String[]</span></span>

## <span data-ttu-id="7a390-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a390-154">OUTPUTS</span></span>

### <span data-ttu-id="7a390-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7a390-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7a390-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7a390-156">NOTES</span></span>

## <span data-ttu-id="7a390-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7a390-157">RELATED LINKS</span></span>
