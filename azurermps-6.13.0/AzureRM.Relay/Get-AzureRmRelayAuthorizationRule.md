---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 13de3f05879234a0db1af34517d37172c2a5a6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664519"
---
# <span data-ttu-id="26eef-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="26eef-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="26eef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26eef-102">SYNOPSIS</span></span>
<span data-ttu-id="26eef-103">Ruft die Beschreibung einer angegebenen Autorisierungsregel für eine bestimmte Relay-Entitäten (Namespace/WcfRelay/HybridConnection) ab.</span><span class="sxs-lookup"><span data-stu-id="26eef-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26eef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26eef-104">SYNTAX</span></span>

### <span data-ttu-id="26eef-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="26eef-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26eef-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="26eef-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26eef-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="26eef-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26eef-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26eef-108">DESCRIPTION</span></span>
<span data-ttu-id="26eef-109">Das Cmdlet " **Get-AzureRmRelayAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel in den angegebenen Relay-Entitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="26eef-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="26eef-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26eef-110">EXAMPLES</span></span>

### <span data-ttu-id="26eef-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="26eef-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="26eef-112">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="26eef-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="26eef-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="26eef-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="26eef-114">Gibt die angegebene Autorisierungsregel Beschreibung für eine bestimmte WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="26eef-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="26eef-115">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="26eef-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="26eef-116">Gibt die angegebene Autorisierungsregel Beschreibung für eine bestimmte HybridConnection zurück.</span><span class="sxs-lookup"><span data-stu-id="26eef-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="26eef-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="26eef-117">PARAMETERS</span></span>

### <span data-ttu-id="26eef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26eef-118">-DefaultProfile</span></span>
<span data-ttu-id="26eef-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26eef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26eef-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="26eef-120">-HybridConnection</span></span>
<span data-ttu-id="26eef-121">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="26eef-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="26eef-122">-Name</span><span class="sxs-lookup"><span data-stu-id="26eef-122">-Name</span></span>
<span data-ttu-id="26eef-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="26eef-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="26eef-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="26eef-124">-Namespace</span></span>
<span data-ttu-id="26eef-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="26eef-125">Namespace Name.</span></span>

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

### <span data-ttu-id="26eef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26eef-126">-ResourceGroupName</span></span>
<span data-ttu-id="26eef-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="26eef-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="26eef-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="26eef-128">-WcfRelay</span></span>
<span data-ttu-id="26eef-129">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="26eef-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="26eef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26eef-130">CommonParameters</span></span>
<span data-ttu-id="26eef-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26eef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26eef-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26eef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26eef-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26eef-133">INPUTS</span></span>

### <span data-ttu-id="26eef-134">System. String</span><span class="sxs-lookup"><span data-stu-id="26eef-134">System.String</span></span>


## <span data-ttu-id="26eef-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26eef-135">OUTPUTS</span></span>

### <span data-ttu-id="26eef-136">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="26eef-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="26eef-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="26eef-137">NOTES</span></span>

## <span data-ttu-id="26eef-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26eef-138">RELATED LINKS</span></span>
