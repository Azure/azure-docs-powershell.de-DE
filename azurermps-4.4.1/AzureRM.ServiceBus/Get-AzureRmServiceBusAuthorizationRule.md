---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504730"
---
# <span data-ttu-id="f41a5-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f41a5-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f41a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f41a5-102">SYNOPSIS</span></span>
<span data-ttu-id="f41a5-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema ab.</span><span class="sxs-lookup"><span data-stu-id="f41a5-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f41a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f41a5-104">SYNTAX</span></span>

### <span data-ttu-id="f41a5-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f41a5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f41a5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f41a5-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f41a5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f41a5-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f41a5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f41a5-108">DESCRIPTION</span></span>
<span data-ttu-id="f41a5-109">Das Cmdlet " **Get-AzureRmServiceBusAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in einer Warteschlange oder einem bestimmten Thema ab.</span><span class="sxs-lookup"><span data-stu-id="f41a5-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="f41a5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f41a5-110">EXAMPLES</span></span>

### <span data-ttu-id="f41a5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f41a5-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f41a5-112">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="f41a5-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="f41a5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f41a5-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f41a5-114">Gibt die angegebene Autorisierungsregel Beschreibung für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="f41a5-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="f41a5-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f41a5-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f41a5-116">Gibt die angegebene Autorisierungsregel Beschreibung für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="f41a5-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="f41a5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f41a5-117">PARAMETERS</span></span>

### <span data-ttu-id="f41a5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f41a5-118">-Name</span></span>
<span data-ttu-id="f41a5-119">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="f41a5-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f41a5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f41a5-120">-Namespace</span></span>
<span data-ttu-id="f41a5-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="f41a5-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f41a5-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="f41a5-122">-Queue</span></span>
<span data-ttu-id="f41a5-123">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="f41a5-123">Queue Name.</span></span>

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

### <span data-ttu-id="f41a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="f41a5-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f41a5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f41a5-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="f41a5-126">-Topic</span></span>
<span data-ttu-id="f41a5-127">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="f41a5-127">Topic Name.</span></span>

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

### <span data-ttu-id="f41a5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41a5-128">-DefaultProfile</span></span>
<span data-ttu-id="f41a5-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f41a5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f41a5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41a5-130">CommonParameters</span></span>
<span data-ttu-id="f41a5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f41a5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41a5-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f41a5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41a5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f41a5-133">INPUTS</span></span>

### <span data-ttu-id="f41a5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f41a5-134">System.String</span></span>

## <span data-ttu-id="f41a5-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f41a5-135">OUTPUTS</span></span>

### <span data-ttu-id="f41a5-136">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f41a5-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f41a5-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f41a5-137">NOTES</span></span>
## <span data-ttu-id="f41a5-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f41a5-138">RELATED LINKS</span></span>

## <span data-ttu-id="f41a5-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f41a5-139">RELATED LINKS</span></span>

