---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662615"
---
# <span data-ttu-id="50ea7-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="50ea7-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="50ea7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="50ea7-103">Erstellt eine neue Autorisierungsregel für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="50ea7-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50ea7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50ea7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50ea7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="50ea7-106">Das Cmdlet **New-AzureRmServiceBusTopicAuthorizationRule** erstellt eine neue Autorisierungsregel für das angegebene Service Bus-Thema.</span><span class="sxs-lookup"><span data-stu-id="50ea7-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="50ea7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="50ea7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50ea7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="50ea7-109">Erstellt eine Autorisierungsregel `SBTopicAuthoRule1` mit **Listen** -und **Sende** rechten für das Thema `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="50ea7-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="50ea7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="50ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="50ea7-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50ea7-111">-ResourceGroup</span></span>
<span data-ttu-id="50ea7-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="50ea7-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="50ea7-113">-Rechte</span><span class="sxs-lookup"><span data-stu-id="50ea7-113">-Rights</span></span>
<span data-ttu-id="50ea7-114">Die Rechte; Beispiel: @ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="50ea7-114">The rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50ea7-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50ea7-115">-Confirm</span></span>
<span data-ttu-id="50ea7-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50ea7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50ea7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50ea7-117">-WhatIf</span></span>
<span data-ttu-id="50ea7-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50ea7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50ea7-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50ea7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50ea7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ea7-120">-DefaultProfile</span></span>
<span data-ttu-id="50ea7-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50ea7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50ea7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50ea7-122">-Name</span></span>
<span data-ttu-id="50ea7-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="50ea7-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50ea7-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="50ea7-124">-Namespace</span></span>
<span data-ttu-id="50ea7-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="50ea7-125">Namespace Name.</span></span>

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

### <span data-ttu-id="50ea7-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="50ea7-126">-Topic</span></span>
<span data-ttu-id="50ea7-127">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="50ea7-127">Topic Name.</span></span>

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

### <span data-ttu-id="50ea7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ea7-128">CommonParameters</span></span>
<span data-ttu-id="50ea7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ea7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ea7-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ea7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ea7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50ea7-131">INPUTS</span></span>

### <span data-ttu-id="50ea7-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50ea7-132">-ResourceGroup</span></span>
 <span data-ttu-id="50ea7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="50ea7-133">System.String</span></span>
 

### <span data-ttu-id="50ea7-134">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="50ea7-134">-NamespaceName</span></span>
 <span data-ttu-id="50ea7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="50ea7-135">System.String</span></span>
 

### <span data-ttu-id="50ea7-136">-Topicname</span><span class="sxs-lookup"><span data-stu-id="50ea7-136">-TopicName</span></span>
 <span data-ttu-id="50ea7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="50ea7-137">System.String</span></span>
 

### <span data-ttu-id="50ea7-138">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="50ea7-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="50ea7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="50ea7-139">System.String</span></span>

## <span data-ttu-id="50ea7-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50ea7-140">OUTPUTS</span></span>

### <span data-ttu-id="50ea7-141">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="50ea7-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="50ea7-142">ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/ResourceGroups/default-ServiceBus-westus/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/topics/SB-Topic_exampl1/authorizati onrules/SBTopicAuthoRule1 Typ: Microsoft. ServiceBus/authorizationrules Name: SBTopicAuthoRule1 Ort: West US Tags: Rights: {Listen, senden}</span><span class="sxs-lookup"><span data-stu-id="50ea7-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="50ea7-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="50ea7-143">NOTES</span></span>

## <span data-ttu-id="50ea7-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50ea7-144">RELATED LINKS</span></span>

