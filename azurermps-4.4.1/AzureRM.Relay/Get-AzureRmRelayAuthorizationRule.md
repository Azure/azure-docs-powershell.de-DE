---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 53a46e9c78544919c325f63b8bc8ccf9fd457f31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496938"
---
# <span data-ttu-id="a27a8-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a27a8-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="a27a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a27a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a27a8-103">Ruft die Beschreibung einer angegebenen Autorisierungsregel für eine bestimmte Relay-Entitäten (Namespace/WcfRelay/HybridConnection) ab.</span><span class="sxs-lookup"><span data-stu-id="a27a8-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a27a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a27a8-104">SYNTAX</span></span>

### <span data-ttu-id="a27a8-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a27a8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a27a8-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a27a8-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a27a8-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a27a8-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a27a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a27a8-108">DESCRIPTION</span></span>
<span data-ttu-id="a27a8-109">Das Cmdlet " **Get-AzureRmRelayAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel in den angegebenen Relay-Entitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="a27a8-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="a27a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a27a8-110">EXAMPLES</span></span>

### <span data-ttu-id="a27a8-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="a27a8-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="a27a8-112">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="a27a8-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="a27a8-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a27a8-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="a27a8-114">Gibt die angegebene Autorisierungsregel Beschreibung für eine bestimmte WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="a27a8-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="a27a8-115">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a27a8-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="a27a8-116">Gibt die angegebene Autorisierungsregel Beschreibung für eine bestimmte HybridConnection zurück.</span><span class="sxs-lookup"><span data-stu-id="a27a8-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="a27a8-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a27a8-117">PARAMETERS</span></span>

### <span data-ttu-id="a27a8-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a27a8-118">-HybridConnection</span></span>
<span data-ttu-id="a27a8-119">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="a27a8-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="a27a8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a27a8-120">-Name</span></span>
<span data-ttu-id="a27a8-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="a27a8-121">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a27a8-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a27a8-122">-Namespace</span></span>
<span data-ttu-id="a27a8-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a27a8-123">Namespace Name.</span></span>

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

### <span data-ttu-id="a27a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="a27a8-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a27a8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a27a8-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a27a8-126">-WcfRelay</span></span>
<span data-ttu-id="a27a8-127">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="a27a8-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="a27a8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27a8-128">-DefaultProfile</span></span>
<span data-ttu-id="a27a8-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a27a8-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a27a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27a8-130">CommonParameters</span></span>
<span data-ttu-id="a27a8-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27a8-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a27a8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27a8-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a27a8-133">INPUTS</span></span>

### <span data-ttu-id="a27a8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27a8-134">-ResourceGroupName</span></span>
 <span data-ttu-id="a27a8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a27a8-135">System.String</span></span> 

### <span data-ttu-id="a27a8-136">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="a27a8-136">-NamespaceName</span></span>
 <span data-ttu-id="a27a8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a27a8-137">System.String</span></span> 
 

### <span data-ttu-id="a27a8-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="a27a8-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="a27a8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a27a8-139">System.String</span></span> 

### <span data-ttu-id="a27a8-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="a27a8-140">-WcfRelayName</span></span>
 <span data-ttu-id="a27a8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a27a8-141">System.String</span></span> 

### <span data-ttu-id="a27a8-142">-Name</span><span class="sxs-lookup"><span data-stu-id="a27a8-142">-Name</span></span>
 <span data-ttu-id="a27a8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a27a8-143">System.String</span></span>

## <span data-ttu-id="a27a8-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a27a8-144">OUTPUTS</span></span>

### <span data-ttu-id="a27a8-145">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. AuthorizationRuleAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a27a8-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a27a8-146">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="a27a8-146">Example 1 - Namespace</span></span>
<span data-ttu-id="a27a8-147">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/AuthorizationRules/AUT hoRule1</span><span class="sxs-lookup"><span data-stu-id="a27a8-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="a27a8-148">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="a27a8-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="a27a8-149">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationrules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="a27a8-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="a27a8-150">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="a27a8-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="a27a8-151">Rechte: {anhören, senden} Name: AuthoRule1 Typ: Microsoft. Relay/authorizationrules-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationrules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="a27a8-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="a27a8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="a27a8-152">NOTES</span></span>

## <span data-ttu-id="a27a8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a27a8-153">RELATED LINKS</span></span>

