---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824756"
---
# <span data-ttu-id="0ba4d-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0ba4d-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="0ba4d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ba4d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba4d-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="0ba4d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ba4d-104">SYNTAX</span></span>

### <span data-ttu-id="0ba4d-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ba4d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ba4d-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ba4d-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ba4d-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ba4d-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ba4d-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0ba4d-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ba4d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ba4d-109">DESCRIPTION</span></span>
<span data-ttu-id="0ba4d-110">Das Cmdlet " **Satz-AzServiceBusAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel im angegebenen ServiceBus-Namespace oder in einer Warteschlange oder einem bestimmten Thema.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="0ba4d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ba4d-111">EXAMPLES</span></span>

### <span data-ttu-id="0ba4d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ba4d-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="0ba4d-113">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0ba4d-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="0ba4d-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0ba4d-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="0ba4d-115">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in der Warteschlange `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="0ba4d-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="0ba4d-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0ba4d-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="0ba4d-117">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` im Thema `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="0ba4d-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="0ba4d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ba4d-118">PARAMETERS</span></span>

### <span data-ttu-id="0ba4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba4d-119">-DefaultProfile</span></span>
<span data-ttu-id="0ba4d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ba4d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ba4d-121">-InputObject</span></span>
<span data-ttu-id="0ba4d-122">ServiceBus-AuthorizationRule-Objekt</span><span class="sxs-lookup"><span data-stu-id="0ba4d-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="0ba4d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0ba4d-123">-Name</span></span>
<span data-ttu-id="0ba4d-124">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="0ba4d-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="0ba4d-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0ba4d-125">-Namespace</span></span>
<span data-ttu-id="0ba4d-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="0ba4d-126">Namespace Name</span></span>

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

### <span data-ttu-id="0ba4d-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="0ba4d-127">-Queue</span></span>
<span data-ttu-id="0ba4d-128">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="0ba4d-128">Queue Name</span></span>

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

### <span data-ttu-id="0ba4d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba4d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0ba4d-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0ba4d-130">Resource Group Name</span></span>

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

### <span data-ttu-id="0ba4d-131">-Rechte</span><span class="sxs-lookup"><span data-stu-id="0ba4d-131">-Rights</span></span>
<span data-ttu-id="0ba4d-132">Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="0ba4d-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="0ba4d-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="0ba4d-133">-Topic</span></span>
<span data-ttu-id="0ba4d-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="0ba4d-134">Topic Name</span></span>

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

### <span data-ttu-id="0ba4d-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ba4d-135">-Confirm</span></span>
<span data-ttu-id="0ba4d-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ba4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ba4d-137">-WhatIf</span></span>
<span data-ttu-id="0ba4d-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ba4d-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ba4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba4d-140">CommonParameters</span></span>
<span data-ttu-id="0ba4d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba4d-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba4d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba4d-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ba4d-143">INPUTS</span></span>

### <span data-ttu-id="0ba4d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0ba4d-144">System.String</span></span>

### <span data-ttu-id="0ba4d-145">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0ba4d-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="0ba4d-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="0ba4d-146">System.String[]</span></span>

## <span data-ttu-id="0ba4d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ba4d-147">OUTPUTS</span></span>

### <span data-ttu-id="0ba4d-148">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0ba4d-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0ba4d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ba4d-149">NOTES</span></span>

## <span data-ttu-id="0ba4d-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ba4d-150">RELATED LINKS</span></span>
