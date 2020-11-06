---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503205"
---
# <span data-ttu-id="be116-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="be116-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="be116-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be116-102">SYNOPSIS</span></span>
<span data-ttu-id="be116-103">Gibt die Beschreibung der angegebenen Autorisierungsregel Beschreibung für das angegebene Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="be116-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be116-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be116-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be116-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be116-105">DESCRIPTION</span></span>
<span data-ttu-id="be116-106">Das Cmdlet " **Get-AzureRmServiceBusTopicAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel für das angegebene ServiceBus-Thema ab.</span><span class="sxs-lookup"><span data-stu-id="be116-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="be116-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be116-107">EXAMPLES</span></span>

### <span data-ttu-id="be116-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be116-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="be116-109">Gibt die Beschreibung der angegebenen Autorisierungsregel für das angegebene Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="be116-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="be116-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be116-110">PARAMETERS</span></span>

### <span data-ttu-id="be116-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be116-111">-ResourceGroup</span></span>
<span data-ttu-id="be116-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be116-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="be116-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be116-113">-DefaultProfile</span></span>
<span data-ttu-id="be116-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be116-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be116-115">-Name</span><span class="sxs-lookup"><span data-stu-id="be116-115">-Name</span></span>
<span data-ttu-id="be116-116">Thema-AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="be116-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="be116-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="be116-117">-Namespace</span></span>
<span data-ttu-id="be116-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="be116-118">Namespace Name.</span></span>

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

### <span data-ttu-id="be116-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="be116-119">-Topic</span></span>
<span data-ttu-id="be116-120">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="be116-120">Topic Name.</span></span>

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

### <span data-ttu-id="be116-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be116-121">CommonParameters</span></span>
<span data-ttu-id="be116-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be116-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be116-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be116-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be116-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be116-124">INPUTS</span></span>

### <span data-ttu-id="be116-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be116-125">-ResourceGroup</span></span>
 <span data-ttu-id="be116-126">System. String</span><span class="sxs-lookup"><span data-stu-id="be116-126">System.String</span></span>
 

### <span data-ttu-id="be116-127">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="be116-127">-NamespaceName</span></span>
 <span data-ttu-id="be116-128">System. String</span><span class="sxs-lookup"><span data-stu-id="be116-128">System.String</span></span>
 

### <span data-ttu-id="be116-129">-Topicname</span><span class="sxs-lookup"><span data-stu-id="be116-129">-TopicName</span></span>
 <span data-ttu-id="be116-130">System. String</span><span class="sxs-lookup"><span data-stu-id="be116-130">System.String</span></span>
 

### <span data-ttu-id="be116-131">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="be116-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="be116-132">System. String</span><span class="sxs-lookup"><span data-stu-id="be116-132">System.String</span></span>

## <span data-ttu-id="be116-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be116-133">OUTPUTS</span></span>

### <span data-ttu-id="be116-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="be116-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="be116-135">ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/ResourceGroups/default-ServiceBus-westus/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/topics/SB-Topic_example1/authorizati onrules/SBTopicAuthoRule1 Typ: Microsoft. ServiceBus/authorizationrules Name: SBTopicAuthoRule1 Ort: West US Tags: Rights: {Listen, senden}</span><span class="sxs-lookup"><span data-stu-id="be116-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="be116-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="be116-136">NOTES</span></span>

## <span data-ttu-id="be116-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be116-137">RELATED LINKS</span></span>

