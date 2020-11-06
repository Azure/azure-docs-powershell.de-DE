---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502493"
---
# <span data-ttu-id="77abd-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="77abd-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="77abd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77abd-102">SYNOPSIS</span></span>
<span data-ttu-id="77abd-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="77abd-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77abd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77abd-104">SYNTAX</span></span>

### <span data-ttu-id="77abd-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="77abd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77abd-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="77abd-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77abd-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="77abd-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77abd-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77abd-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77abd-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="77abd-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77abd-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77abd-110">DESCRIPTION</span></span>
<span data-ttu-id="77abd-111">Das Cmdlet " **Satz-AzureRmRelayAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="77abd-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="77abd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77abd-112">EXAMPLES</span></span>

### <span data-ttu-id="77abd-113">Example 1,1-Namespace mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="77abd-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="77abd-114">Fügt **Send** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace hinzu `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="77abd-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="77abd-115">Beispiel für 1,2-Namespace mit rights-Parameter</span><span class="sxs-lookup"><span data-stu-id="77abd-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="77abd-116">Fügt **Send** aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace hinzu `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="77abd-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="77abd-117">Beispiel 2,1-WcfRelay mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="77abd-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="77abd-118">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="77abd-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="77abd-119">Beispiel 2,2-WcfRelay mit rights-Parameter</span><span class="sxs-lookup"><span data-stu-id="77abd-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="77abd-120">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="77abd-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="77abd-121">Beispiel 3,1-HybridConnection mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="77abd-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="77abd-122">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="77abd-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="77abd-123">Beispiel 3,2-HybridConnection mit rights-Parameter</span><span class="sxs-lookup"><span data-stu-id="77abd-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="77abd-124">Fügt **Send** an die Zugriffsrechte der Autorisierungsregel `AuthoRule1` des HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="77abd-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="77abd-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="77abd-125">PARAMETERS</span></span>

### <span data-ttu-id="77abd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77abd-126">-DefaultProfile</span></span>
<span data-ttu-id="77abd-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77abd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="77abd-128">-HybridConnection</span></span>
<span data-ttu-id="77abd-129">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="77abd-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77abd-130">-InputObject</span></span>
<span data-ttu-id="77abd-131">Relay-AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="77abd-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-132">-Name</span><span class="sxs-lookup"><span data-stu-id="77abd-132">-Name</span></span>
<span data-ttu-id="77abd-133">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="77abd-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="77abd-134">-Namespace</span></span>
<span data-ttu-id="77abd-135">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="77abd-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77abd-136">-ResourceGroupName</span></span>
<span data-ttu-id="77abd-137">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="77abd-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-138">-Rechte</span><span class="sxs-lookup"><span data-stu-id="77abd-138">-Rights</span></span>
<span data-ttu-id="77abd-139">Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="77abd-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="77abd-140">-WcfRelay</span></span>
<span data-ttu-id="77abd-141">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="77abd-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77abd-142">-Confirm</span></span>
<span data-ttu-id="77abd-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77abd-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77abd-144">-WhatIf</span></span>
<span data-ttu-id="77abd-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77abd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77abd-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77abd-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77abd-147">CommonParameters</span></span>
<span data-ttu-id="77abd-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77abd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77abd-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77abd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77abd-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77abd-150">INPUTS</span></span>

### <span data-ttu-id="77abd-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77abd-151">-ResourceGroupName</span></span>
 <span data-ttu-id="77abd-152">System. String</span><span class="sxs-lookup"><span data-stu-id="77abd-152">System.String</span></span> 

### <span data-ttu-id="77abd-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="77abd-153">-Namespace</span></span>
 <span data-ttu-id="77abd-154">System. String</span><span class="sxs-lookup"><span data-stu-id="77abd-154">System.String</span></span> 
 

### <span data-ttu-id="77abd-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="77abd-155">-WcfRelay</span></span>
 <span data-ttu-id="77abd-156">System. String</span><span class="sxs-lookup"><span data-stu-id="77abd-156">System.String</span></span> 

### <span data-ttu-id="77abd-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="77abd-157">-HybridConnection</span></span>
 <span data-ttu-id="77abd-158">System. String</span><span class="sxs-lookup"><span data-stu-id="77abd-158">System.String</span></span> 
 

### <span data-ttu-id="77abd-159">-Name</span><span class="sxs-lookup"><span data-stu-id="77abd-159">-Name</span></span>
 <span data-ttu-id="77abd-160">System. String</span><span class="sxs-lookup"><span data-stu-id="77abd-160">System.String</span></span>

### <span data-ttu-id="77abd-161">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77abd-161">-InputObject</span></span>
 <span data-ttu-id="77abd-162">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="77abd-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="77abd-163">-Rechte</span><span class="sxs-lookup"><span data-stu-id="77abd-163">-Rights</span></span>
 <span data-ttu-id="77abd-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="77abd-164">System.String []</span></span>

## <span data-ttu-id="77abd-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77abd-165">OUTPUTS</span></span>

### <span data-ttu-id="77abd-166">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="77abd-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="77abd-167">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="77abd-167">Example 1 - Namespace</span></span>
<span data-ttu-id="77abd-168">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="77abd-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="77abd-169">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="77abd-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="77abd-170">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="77abd-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="77abd-171">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="77abd-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="77abd-172">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="77abd-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="77abd-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="77abd-173">NOTES</span></span>

## <span data-ttu-id="77abd-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77abd-174">RELATED LINKS</span></span>

