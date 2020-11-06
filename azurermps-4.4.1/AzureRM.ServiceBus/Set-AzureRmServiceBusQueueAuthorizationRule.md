---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503941"
---
# <span data-ttu-id="e2a5b-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2a5b-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="e2a5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a5b-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für die angegebene ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2a5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2a5b-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2a5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="e2a5b-106">Das Cmdlet " **Satz-AzureRmServiceBusQueueAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel der angegebenen ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="e2a5b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2a5b-107">EXAMPLES</span></span>

### <span data-ttu-id="e2a5b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2a5b-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="e2a5b-109">Fügt " **Manage** " den Zugriffsrechten der Autorisierungsregel `SBAuthoRule1` der Warteschlange hinzu `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="e2a5b-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="e2a5b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2a5b-110">PARAMETERS</span></span>

### <span data-ttu-id="e2a5b-111">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="e2a5b-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="e2a5b-112">Der Name der Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-112">The authorization rule name.</span></span> <span data-ttu-id="e2a5b-113">Erforderlich **, wenn-AuthruleObj** nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a5b-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="e2a5b-114">-AuthRuleObj</span></span>
<span data-ttu-id="e2a5b-115">Das Service Bus-Warteschlangen Autorisierungsregel Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a5b-116">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="e2a5b-116">-NamespaceName</span></span>
<span data-ttu-id="e2a5b-117">Der Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a5b-118">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="e2a5b-118">-QueueName</span></span>
<span data-ttu-id="e2a5b-119">Der Name der ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a5b-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2a5b-120">-ResourceGroup</span></span>
<span data-ttu-id="e2a5b-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2a5b-122">-Rechte</span><span class="sxs-lookup"><span data-stu-id="e2a5b-122">-Rights</span></span>
<span data-ttu-id="e2a5b-123">Die Rechte; Beispiel: @ ("Listen", "Senden", "verwalten").</span><span class="sxs-lookup"><span data-stu-id="e2a5b-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="e2a5b-124">Erforderlich, wenn "AuthruleObj" nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a5b-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e2a5b-125">-Confirm</span></span>
<span data-ttu-id="e2a5b-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a5b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2a5b-127">-WhatIf</span></span>
<span data-ttu-id="e2a5b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2a5b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a5b-130">CommonParameters</span></span>
<span data-ttu-id="e2a5b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a5b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a5b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a5b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2a5b-133">INPUTS</span></span>

### <span data-ttu-id="e2a5b-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2a5b-134">-ResourceGroup</span></span>
 <span data-ttu-id="e2a5b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a5b-135">System.String</span></span>

### <span data-ttu-id="e2a5b-136">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="e2a5b-136">-NamespaceName</span></span>
 <span data-ttu-id="e2a5b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a5b-137">System.String</span></span>

### <span data-ttu-id="e2a5b-138">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="e2a5b-138">-QueueName</span></span>
 <span data-ttu-id="e2a5b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a5b-139">System.String</span></span>

### <span data-ttu-id="e2a5b-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="e2a5b-140">-AuthRuleObj</span></span>
 <span data-ttu-id="e2a5b-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2a5b-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e2a5b-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2a5b-142">OUTPUTS</span></span>

### <span data-ttu-id="e2a5b-143">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2a5b-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e2a5b-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2a5b-144">NOTES</span></span>

## <span data-ttu-id="e2a5b-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2a5b-145">RELATED LINKS</span></span>

