---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664432"
---
# <span data-ttu-id="b95cb-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b95cb-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="b95cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b95cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b95cb-103">Aktualisiert die angegebene Autorisierungsregel Beschreibung für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="b95cb-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b95cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b95cb-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b95cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b95cb-105">DESCRIPTION</span></span>
<span data-ttu-id="b95cb-106">Das Cmdlet " **Satz-AzureRmServiceBusTopicAuthorizationRule** " aktualisiert die Beschreibung für die angegebene Autorisierungsregel des angegebenen ServiceBus-Themas.</span><span class="sxs-lookup"><span data-stu-id="b95cb-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="b95cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b95cb-107">EXAMPLES</span></span>

### <span data-ttu-id="b95cb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b95cb-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="b95cb-109">Fügt " **Verwalten** " den Zugriffsrechten der Autorisierungsregel `SBTopicAuthoRule1` zum Thema hinzu `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="b95cb-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="b95cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b95cb-110">PARAMETERS</span></span>

### <span data-ttu-id="b95cb-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b95cb-111">-ResourceGroup</span></span>
<span data-ttu-id="b95cb-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b95cb-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b95cb-113">-Rechte</span><span class="sxs-lookup"><span data-stu-id="b95cb-113">-Rights</span></span>
<span data-ttu-id="b95cb-114">Rechte Beispiel: @ ("Listen", "Senden", "verwalten").</span><span class="sxs-lookup"><span data-stu-id="b95cb-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="b95cb-115">Erforderlich **, wenn-AuthruleObj** nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b95cb-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95cb-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b95cb-116">-Confirm</span></span>
<span data-ttu-id="b95cb-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b95cb-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95cb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b95cb-118">-WhatIf</span></span>
<span data-ttu-id="b95cb-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b95cb-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b95cb-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b95cb-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b95cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95cb-121">-DefaultProfile</span></span>
<span data-ttu-id="b95cb-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b95cb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b95cb-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="b95cb-123">-InputObj</span></span>
<span data-ttu-id="b95cb-124">ServiceBus Topic AuthorizationRule-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b95cb-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95cb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b95cb-125">-Name</span></span>
<span data-ttu-id="b95cb-126">AuthorizationRule-Name – erforderlich, wenn "AuthruleObj" nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b95cb-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95cb-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b95cb-127">-Namespace</span></span>
<span data-ttu-id="b95cb-128">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="b95cb-128">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95cb-129">-Topic</span><span class="sxs-lookup"><span data-stu-id="b95cb-129">-Topic</span></span>
<span data-ttu-id="b95cb-130">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="b95cb-130">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b95cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95cb-131">CommonParameters</span></span>
<span data-ttu-id="b95cb-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b95cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95cb-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b95cb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95cb-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b95cb-134">INPUTS</span></span>

### <span data-ttu-id="b95cb-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b95cb-135">-ResourceGroup</span></span>
 <span data-ttu-id="b95cb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b95cb-136">System.String</span></span>

### <span data-ttu-id="b95cb-137">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="b95cb-137">-NamespaceName</span></span>
 <span data-ttu-id="b95cb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b95cb-138">System.String</span></span>

### <span data-ttu-id="b95cb-139">-Topicname</span><span class="sxs-lookup"><span data-stu-id="b95cb-139">-TopicName</span></span>
 <span data-ttu-id="b95cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b95cb-140">System.String</span></span>

### <span data-ttu-id="b95cb-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="b95cb-141">-AuthRuleObj</span></span>
 <span data-ttu-id="b95cb-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b95cb-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b95cb-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b95cb-143">OUTPUTS</span></span>

### <span data-ttu-id="b95cb-144">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b95cb-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="b95cb-145">ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/ResourceGroups/default-ServiceBus-westus/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/topics/SB-Topic_exampl1/Authorization Rules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/authorizationrules Name: SBTopicAuthoRule1 Ort: West US Tags: Rights: {Listen, senden, verwalten}</span><span class="sxs-lookup"><span data-stu-id="b95cb-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="b95cb-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="b95cb-146">NOTES</span></span>

## <span data-ttu-id="b95cb-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b95cb-147">RELATED LINKS</span></span>

