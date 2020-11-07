---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 2b4ddf625e5565de0d345a5477d3ba368dcb186b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664007"
---
# <span data-ttu-id="18a99-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="18a99-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="18a99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18a99-102">SYNOPSIS</span></span>
<span data-ttu-id="18a99-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.</span><span class="sxs-lookup"><span data-stu-id="18a99-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18a99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18a99-104">SYNTAX</span></span>

### <span data-ttu-id="18a99-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="18a99-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a99-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="18a99-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a99-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="18a99-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18a99-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="18a99-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18a99-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18a99-109">DESCRIPTION</span></span>
<span data-ttu-id="18a99-110">Das Cmdlet " **Satz-AzureRmServiceBusAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel im angegebenen ServiceBus-Namespace oder in einer Warteschlange oder einem bestimmten Thema.</span><span class="sxs-lookup"><span data-stu-id="18a99-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="18a99-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18a99-111">EXAMPLES</span></span>

### <span data-ttu-id="18a99-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="18a99-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="18a99-113">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="18a99-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="18a99-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="18a99-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="18a99-115">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in der Warteschlange `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="18a99-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="18a99-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="18a99-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="18a99-117">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` im Thema `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="18a99-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="18a99-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="18a99-118">PARAMETERS</span></span>

### <span data-ttu-id="18a99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a99-119">-DefaultProfile</span></span>
<span data-ttu-id="18a99-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18a99-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a99-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="18a99-121">-InputObject</span></span>
<span data-ttu-id="18a99-122">ServiceBus-AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="18a99-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-123">-Name</span><span class="sxs-lookup"><span data-stu-id="18a99-123">-Name</span></span>
<span data-ttu-id="18a99-124">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="18a99-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="18a99-125">-Namespace</span></span>
<span data-ttu-id="18a99-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="18a99-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="18a99-127">-Queue</span></span>
<span data-ttu-id="18a99-128">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="18a99-128">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a99-129">-ResourceGroupName</span></span>
<span data-ttu-id="18a99-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="18a99-130">Resource Group Name</span></span>

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

### <span data-ttu-id="18a99-131">-Rechte</span><span class="sxs-lookup"><span data-stu-id="18a99-131">-Rights</span></span>
<span data-ttu-id="18a99-132">Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="18a99-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="18a99-133">-Topic</span></span>
<span data-ttu-id="18a99-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="18a99-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a99-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18a99-135">-Confirm</span></span>
<span data-ttu-id="18a99-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18a99-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a99-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a99-137">-WhatIf</span></span>
<span data-ttu-id="18a99-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18a99-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a99-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18a99-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a99-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a99-140">CommonParameters</span></span>
<span data-ttu-id="18a99-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a99-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a99-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18a99-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a99-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18a99-143">INPUTS</span></span>

### <span data-ttu-id="18a99-144">System. String</span><span class="sxs-lookup"><span data-stu-id="18a99-144">System.String</span></span>

### <span data-ttu-id="18a99-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="18a99-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="18a99-146">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="18a99-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="18a99-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="18a99-147">System.String[]</span></span>

## <span data-ttu-id="18a99-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18a99-148">OUTPUTS</span></span>

### <span data-ttu-id="18a99-149">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="18a99-149">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="18a99-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="18a99-150">NOTES</span></span>

## <span data-ttu-id="18a99-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18a99-151">RELATED LINKS</span></span>
