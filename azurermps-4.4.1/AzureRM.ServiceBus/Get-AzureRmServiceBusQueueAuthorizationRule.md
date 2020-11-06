---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481598"
---
# <span data-ttu-id="726c6-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="726c6-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="726c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="726c6-102">SYNOPSIS</span></span>
<span data-ttu-id="726c6-103">Ruft die Beschreibung einer angegebenen Autorisierungsregel für eine angegebene ServiceBus-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="726c6-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="726c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="726c6-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="726c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="726c6-105">DESCRIPTION</span></span>
<span data-ttu-id="726c6-106">Das Cmdlet " **Get-AzureRmServiceBusQueueAuthorizationRule** " Ruft die Beschreibung einer angegebenen Autorisierungsregel für die angegebene ServiceBus-Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="726c6-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="726c6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="726c6-107">EXAMPLES</span></span>

### <span data-ttu-id="726c6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="726c6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="726c6-109">Gibt die angegebene Autorisierungsregel Beschreibung für eine bestimmte Service Bus-Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="726c6-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="726c6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="726c6-110">PARAMETERS</span></span>

### <span data-ttu-id="726c6-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="726c6-111">-ResourceGroup</span></span>
<span data-ttu-id="726c6-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="726c6-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="726c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726c6-113">-DefaultProfile</span></span>
<span data-ttu-id="726c6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="726c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="726c6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="726c6-115">-Name</span></span>
<span data-ttu-id="726c6-116">EventHub-AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="726c6-116">EventHub AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="726c6-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="726c6-117">-Namespace</span></span>
<span data-ttu-id="726c6-118">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="726c6-118">Namespace Name.</span></span>

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

### <span data-ttu-id="726c6-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="726c6-119">-Queue</span></span>
<span data-ttu-id="726c6-120">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="726c6-120">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="726c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726c6-121">CommonParameters</span></span>
<span data-ttu-id="726c6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="726c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726c6-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726c6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726c6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="726c6-124">INPUTS</span></span>

### <span data-ttu-id="726c6-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="726c6-125">-ResourceGroup</span></span>
 <span data-ttu-id="726c6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="726c6-126">System.String</span></span>
 

### <span data-ttu-id="726c6-127">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="726c6-127">-NamespaceName</span></span>
 <span data-ttu-id="726c6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="726c6-128">System.String</span></span>
 

### <span data-ttu-id="726c6-129">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="726c6-129">-QueueName</span></span>
 <span data-ttu-id="726c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="726c6-130">System.String</span></span>
 

### <span data-ttu-id="726c6-131">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="726c6-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="726c6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="726c6-132">System.String</span></span>

## <span data-ttu-id="726c6-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="726c6-133">OUTPUTS</span></span>

### <span data-ttu-id="726c6-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="726c6-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="726c6-135">ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/ResourceGroups/default-ServiceBus-westus/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/Queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 Typ: Microsoft. ServiceBus/authorizationrules Name: SBAuthoRule1 Ort: West US Tags: Rights: {Listen, senden}</span><span class="sxs-lookup"><span data-stu-id="726c6-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="726c6-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="726c6-136">NOTES</span></span>

## <span data-ttu-id="726c6-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="726c6-137">RELATED LINKS</span></span>

