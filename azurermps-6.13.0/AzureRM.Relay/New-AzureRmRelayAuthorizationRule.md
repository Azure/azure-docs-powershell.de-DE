---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 825c6060a77df4adf59465e372ee2511fec80803
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477746"
---
# <span data-ttu-id="795a6-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="795a6-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="795a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="795a6-102">SYNOPSIS</span></span>
<span data-ttu-id="795a6-103">Erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="795a6-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="795a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="795a6-104">SYNTAX</span></span>

### <span data-ttu-id="795a6-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="795a6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="795a6-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="795a6-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="795a6-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="795a6-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="795a6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="795a6-108">DESCRIPTION</span></span>
<span data-ttu-id="795a6-109">Das Cmdlet **New-AzureRmRelayAuthorizationRule** erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="795a6-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="795a6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="795a6-110">EXAMPLES</span></span>

### <span data-ttu-id="795a6-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="795a6-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="795a6-112">Erstellt `AuthoRule1` mit **Listen** rechten für den Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="795a6-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="795a6-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="795a6-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="795a6-114">Erstellt eine Autorisierungsregel `AuthoRule1` mit **Listen** rechten für das WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="795a6-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="795a6-115">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="795a6-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="795a6-116">Erstellt `AuthoRule1` mit **Listen** rechten für die Hybrid Verbindung `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="795a6-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="795a6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="795a6-117">PARAMETERS</span></span>

### <span data-ttu-id="795a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795a6-118">-DefaultProfile</span></span>
<span data-ttu-id="795a6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="795a6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="795a6-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="795a6-120">-HybridConnection</span></span>
<span data-ttu-id="795a6-121">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="795a6-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="795a6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="795a6-122">-Name</span></span>
<span data-ttu-id="795a6-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="795a6-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="795a6-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="795a6-124">-Namespace</span></span>
<span data-ttu-id="795a6-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="795a6-125">Namespace Name.</span></span>

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

### <span data-ttu-id="795a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="795a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="795a6-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="795a6-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="795a6-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="795a6-128">-Rights</span></span>
<span data-ttu-id="795a6-129">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="795a6-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="795a6-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="795a6-130">-WcfRelay</span></span>
<span data-ttu-id="795a6-131">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="795a6-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="795a6-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="795a6-132">-Confirm</span></span>
<span data-ttu-id="795a6-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="795a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="795a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="795a6-134">-WhatIf</span></span>
<span data-ttu-id="795a6-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="795a6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="795a6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="795a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="795a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795a6-137">CommonParameters</span></span>
<span data-ttu-id="795a6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="795a6-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="795a6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795a6-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="795a6-140">INPUTS</span></span>

### <span data-ttu-id="795a6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="795a6-141">System.String</span></span>
<span data-ttu-id="795a6-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="795a6-142">System.String[]</span></span>


## <span data-ttu-id="795a6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="795a6-143">OUTPUTS</span></span>

### <span data-ttu-id="795a6-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="795a6-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="795a6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="795a6-145">NOTES</span></span>

## <span data-ttu-id="795a6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="795a6-146">RELATED LINKS</span></span>
