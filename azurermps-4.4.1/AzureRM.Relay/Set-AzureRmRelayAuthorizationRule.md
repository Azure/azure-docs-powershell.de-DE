---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 64c839140907b10d62b4f71025afab985d5ba736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500777"
---
# <span data-ttu-id="475d9-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="475d9-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="475d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="475d9-102">SYNOPSIS</span></span>
<span data-ttu-id="475d9-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="475d9-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="475d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="475d9-104">SYNTAX</span></span>

### <span data-ttu-id="475d9-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="475d9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="475d9-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="475d9-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="475d9-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="475d9-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-InputObject <AuthorizationRuleAttributes>]
 [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="475d9-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="475d9-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 -InputObject <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="475d9-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="475d9-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> -Rights <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="475d9-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="475d9-110">DESCRIPTION</span></span>
<span data-ttu-id="475d9-111">Das Cmdlet " **Satz-AzureRmRelayAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="475d9-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="475d9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="475d9-112">EXAMPLES</span></span>

### <span data-ttu-id="475d9-113">Example 1,1-Namespace mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="475d9-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="475d9-114">Fügt **Send** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace hinzu `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="475d9-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="475d9-115">Beispiel für 1,2-Namespace mit rights-Parameter</span><span class="sxs-lookup"><span data-stu-id="475d9-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="475d9-116">Fügt **Send** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace hinzu `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="475d9-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="475d9-117">Beispiel 2,1-WcfRelay mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="475d9-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="475d9-118">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="475d9-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="475d9-119">Beispiel 2,2-WcfRelay mit rights-Parameter</span><span class="sxs-lookup"><span data-stu-id="475d9-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="475d9-120">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="475d9-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="475d9-121">Beispiel 3,1-HybridConnection mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="475d9-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="475d9-122">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="475d9-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="475d9-123">Beispiel 3,2-HybridConnection mit rights-Parameter</span><span class="sxs-lookup"><span data-stu-id="475d9-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="475d9-124">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="475d9-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="475d9-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="475d9-125">PARAMETERS</span></span>

### <span data-ttu-id="475d9-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="475d9-126">-Confirm</span></span>
<span data-ttu-id="475d9-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="475d9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="475d9-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="475d9-128">-HybridConnection</span></span>
<span data-ttu-id="475d9-129">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="475d9-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="475d9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="475d9-130">-Name</span></span>
<span data-ttu-id="475d9-131">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="475d9-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="475d9-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="475d9-132">-Namespace</span></span>
<span data-ttu-id="475d9-133">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="475d9-133">Namespace Name.</span></span>

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

### <span data-ttu-id="475d9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475d9-134">-ResourceGroupName</span></span>
<span data-ttu-id="475d9-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="475d9-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="475d9-136">-Rechte</span><span class="sxs-lookup"><span data-stu-id="475d9-136">-Rights</span></span>
<span data-ttu-id="475d9-137">Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="475d9-137">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475d9-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="475d9-138">-WcfRelay</span></span>
<span data-ttu-id="475d9-139">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="475d9-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="475d9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="475d9-140">-WhatIf</span></span>
<span data-ttu-id="475d9-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="475d9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="475d9-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="475d9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="475d9-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475d9-143">-DefaultProfile</span></span>
<span data-ttu-id="475d9-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="475d9-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475d9-145">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="475d9-145">-InputObject</span></span>
<span data-ttu-id="475d9-146">{{Fill Inputobject Description}}</span><span class="sxs-lookup"><span data-stu-id="475d9-146">{{Fill InputObject Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475d9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475d9-147">CommonParameters</span></span>
<span data-ttu-id="475d9-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475d9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475d9-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475d9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475d9-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="475d9-150">INPUTS</span></span>

### <span data-ttu-id="475d9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475d9-151">-ResourceGroupName</span></span>
 <span data-ttu-id="475d9-152">System. String</span><span class="sxs-lookup"><span data-stu-id="475d9-152">System.String</span></span> 

### <span data-ttu-id="475d9-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="475d9-153">-Namespace</span></span>
 <span data-ttu-id="475d9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="475d9-154">System.String</span></span> 
 

### <span data-ttu-id="475d9-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="475d9-155">-WcfRelay</span></span>
 <span data-ttu-id="475d9-156">System. String</span><span class="sxs-lookup"><span data-stu-id="475d9-156">System.String</span></span> 

### <span data-ttu-id="475d9-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="475d9-157">-HybridConnection</span></span>
 <span data-ttu-id="475d9-158">System. String</span><span class="sxs-lookup"><span data-stu-id="475d9-158">System.String</span></span> 
 

### <span data-ttu-id="475d9-159">-Name</span><span class="sxs-lookup"><span data-stu-id="475d9-159">-Name</span></span>
 <span data-ttu-id="475d9-160">System. String</span><span class="sxs-lookup"><span data-stu-id="475d9-160">System.String</span></span>

### <span data-ttu-id="475d9-161">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="475d9-161">-InputObject</span></span>
 <span data-ttu-id="475d9-162">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="475d9-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="475d9-163">-Rechte</span><span class="sxs-lookup"><span data-stu-id="475d9-163">-Rights</span></span>
 <span data-ttu-id="475d9-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="475d9-164">System.String []</span></span>

## <span data-ttu-id="475d9-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="475d9-165">OUTPUTS</span></span>

### <span data-ttu-id="475d9-166">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="475d9-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="475d9-167">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="475d9-167">Example 1 - Namespace</span></span>
<span data-ttu-id="475d9-168">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="475d9-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="475d9-169">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="475d9-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="475d9-170">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="475d9-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="475d9-171">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="475d9-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="475d9-172">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="475d9-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="475d9-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="475d9-173">NOTES</span></span>

## <span data-ttu-id="475d9-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="475d9-174">RELATED LINKS</span></span>

