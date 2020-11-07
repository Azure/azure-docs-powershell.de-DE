---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: daa2d1539a97b7aff7348fe8e603179c857c73db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664215"
---
# <span data-ttu-id="25775-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="25775-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="25775-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25775-102">SYNOPSIS</span></span>
<span data-ttu-id="25775-103">Erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="25775-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25775-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25775-104">SYNTAX</span></span>

### <span data-ttu-id="25775-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25775-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25775-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="25775-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25775-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="25775-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25775-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25775-108">DESCRIPTION</span></span>
<span data-ttu-id="25775-109">Das Cmdlet **New-AzureRmRelayAuthorizationRule** erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="25775-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="25775-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25775-110">EXAMPLES</span></span>

### <span data-ttu-id="25775-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="25775-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="25775-112">Erstellt `AuthoRule1` mit **Listen** rechten für den Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="25775-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="25775-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="25775-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="25775-114">Erstellt eine Autorisierungsregel `AuthoRule1` mit **Listen** rechten für das WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="25775-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="25775-115">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="25775-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="25775-116">Erstellt `AuthoRule1` mit **Listen** rechten für den Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="25775-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="25775-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="25775-117">PARAMETERS</span></span>

### <span data-ttu-id="25775-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25775-118">-DefaultProfile</span></span>
<span data-ttu-id="25775-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25775-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25775-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="25775-120">-HybridConnection</span></span>
<span data-ttu-id="25775-121">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="25775-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="25775-122">-Name</span><span class="sxs-lookup"><span data-stu-id="25775-122">-Name</span></span>
<span data-ttu-id="25775-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="25775-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="25775-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25775-124">-Namespace</span></span>
<span data-ttu-id="25775-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="25775-125">Namespace Name.</span></span>

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

### <span data-ttu-id="25775-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25775-126">-ResourceGroupName</span></span>
<span data-ttu-id="25775-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25775-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="25775-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="25775-128">-Rights</span></span>
<span data-ttu-id="25775-129">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="25775-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25775-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="25775-130">-WcfRelay</span></span>
<span data-ttu-id="25775-131">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="25775-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="25775-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25775-132">-Confirm</span></span>
<span data-ttu-id="25775-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25775-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25775-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25775-134">-WhatIf</span></span>
<span data-ttu-id="25775-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25775-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25775-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25775-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25775-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25775-137">CommonParameters</span></span>
<span data-ttu-id="25775-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25775-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25775-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25775-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25775-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25775-140">INPUTS</span></span>

### <span data-ttu-id="25775-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25775-141">-ResourceGroupName</span></span>
 <span data-ttu-id="25775-142">System. String</span><span class="sxs-lookup"><span data-stu-id="25775-142">System.String</span></span> 

### <span data-ttu-id="25775-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="25775-143">-Namespace</span></span>
 <span data-ttu-id="25775-144">System. String</span><span class="sxs-lookup"><span data-stu-id="25775-144">System.String</span></span> 
 

### <span data-ttu-id="25775-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="25775-145">-WcfRelay</span></span>
 <span data-ttu-id="25775-146">System. String</span><span class="sxs-lookup"><span data-stu-id="25775-146">System.String</span></span> 

### <span data-ttu-id="25775-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="25775-147">-HybridConnection</span></span>
 <span data-ttu-id="25775-148">System. String</span><span class="sxs-lookup"><span data-stu-id="25775-148">System.String</span></span> 
 

### <span data-ttu-id="25775-149">-Name</span><span class="sxs-lookup"><span data-stu-id="25775-149">-Name</span></span>
 <span data-ttu-id="25775-150">System. String</span><span class="sxs-lookup"><span data-stu-id="25775-150">System.String</span></span>
 

### <span data-ttu-id="25775-151">-Rechte</span><span class="sxs-lookup"><span data-stu-id="25775-151">-Rights</span></span>
 <span data-ttu-id="25775-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="25775-152">System.String []</span></span>

## <span data-ttu-id="25775-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25775-153">OUTPUTS</span></span>

### <span data-ttu-id="25775-154">Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="25775-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="25775-155">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="25775-155">Example 1 - Namespace</span></span>
<span data-ttu-id="25775-156">Rights: {Listen} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="25775-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="25775-157">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="25775-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="25775-158">Rights: {Listen} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="25775-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="25775-159">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="25775-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="25775-160">Rights: {Listen} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="25775-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="25775-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="25775-161">NOTES</span></span>

## <span data-ttu-id="25775-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25775-162">RELATED LINKS</span></span>

