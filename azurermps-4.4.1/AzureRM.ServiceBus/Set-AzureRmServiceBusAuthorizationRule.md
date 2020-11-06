---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503953"
---
# <span data-ttu-id="48d8c-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="48d8c-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="48d8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="48d8c-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.</span><span class="sxs-lookup"><span data-stu-id="48d8c-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48d8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48d8c-104">SYNTAX</span></span>

### <span data-ttu-id="48d8c-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="48d8c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d8c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="48d8c-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d8c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="48d8c-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d8c-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="48d8c-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48d8c-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="48d8c-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d8c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48d8c-110">DESCRIPTION</span></span>
<span data-ttu-id="48d8c-111">Das Cmdlet " **Satz-AzureRmServiceBusAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel im angegebenen ServiceBus-Namespace oder in einer Warteschlange oder einem bestimmten Thema.</span><span class="sxs-lookup"><span data-stu-id="48d8c-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="48d8c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48d8c-112">EXAMPLES</span></span>

### <span data-ttu-id="48d8c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48d8c-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="48d8c-114">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="48d8c-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="48d8c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="48d8c-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="48d8c-116">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` in der Warteschlange `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="48d8c-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="48d8c-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="48d8c-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="48d8c-118">Entfernt " **Manage** " aus den Zugriffsrechten der Autorisierungsregel `AuthoRule1` im Thema `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="48d8c-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="48d8c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="48d8c-119">PARAMETERS</span></span>

### <span data-ttu-id="48d8c-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48d8c-120">-Confirm</span></span>
<span data-ttu-id="48d8c-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48d8c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d8c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48d8c-122">-InputObject</span></span>
<span data-ttu-id="48d8c-123">ServiceBus-AuthorizationRule-Objekt.</span><span class="sxs-lookup"><span data-stu-id="48d8c-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48d8c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="48d8c-124">-Name</span></span>
<span data-ttu-id="48d8c-125">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="48d8c-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="48d8c-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="48d8c-126">-Namespace</span></span>
<span data-ttu-id="48d8c-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="48d8c-127">Namespace Name.</span></span>

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

### <span data-ttu-id="48d8c-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="48d8c-128">-Queue</span></span>
<span data-ttu-id="48d8c-129">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="48d8c-129">Queue Name.</span></span>

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

### <span data-ttu-id="48d8c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48d8c-130">-ResourceGroupName</span></span>
<span data-ttu-id="48d8c-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="48d8c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="48d8c-132">-Rechte</span><span class="sxs-lookup"><span data-stu-id="48d8c-132">-Rights</span></span>
<span data-ttu-id="48d8c-133">Rechte, z.b. @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="48d8c-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48d8c-134">-Topic</span><span class="sxs-lookup"><span data-stu-id="48d8c-134">-Topic</span></span>
<span data-ttu-id="48d8c-135">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="48d8c-135">Topic Name.</span></span>

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

### <span data-ttu-id="48d8c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d8c-136">-WhatIf</span></span>
<span data-ttu-id="48d8c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48d8c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48d8c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48d8c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d8c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d8c-139">-DefaultProfile</span></span>
<span data-ttu-id="48d8c-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48d8c-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48d8c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d8c-141">CommonParameters</span></span>
<span data-ttu-id="48d8c-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48d8c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d8c-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d8c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d8c-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48d8c-144">INPUTS</span></span>

### <span data-ttu-id="48d8c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="48d8c-145">System.String</span></span>
<span data-ttu-id="48d8c-146">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes System. String []</span><span class="sxs-lookup"><span data-stu-id="48d8c-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="48d8c-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48d8c-147">OUTPUTS</span></span>

### <span data-ttu-id="48d8c-148">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="48d8c-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="48d8c-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="48d8c-149">NOTES</span></span>

## <span data-ttu-id="48d8c-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48d8c-150">RELATED LINKS</span></span>

