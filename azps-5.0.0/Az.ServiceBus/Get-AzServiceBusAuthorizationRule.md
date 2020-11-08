---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175893"
---
# <span data-ttu-id="102cf-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="102cf-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="102cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="102cf-102">SYNOPSIS</span></span>
<span data-ttu-id="102cf-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema oder einen Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="102cf-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="102cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="102cf-104">SYNTAX</span></span>

### <span data-ttu-id="102cf-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="102cf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="102cf-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="102cf-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="102cf-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="102cf-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="102cf-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="102cf-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="102cf-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="102cf-109">DESCRIPTION</span></span>
<span data-ttu-id="102cf-110">Das Cmdlet " **Get-AzServiceBusAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in einer Warteschlange oder einem Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="102cf-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="102cf-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="102cf-111">EXAMPLES</span></span>

### <span data-ttu-id="102cf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="102cf-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="102cf-113">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="102cf-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="102cf-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="102cf-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="102cf-115">Gibt die angegebene Autorisierungsregel Beschreibung für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="102cf-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="102cf-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="102cf-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="102cf-117">Gibt die angegebene Autorisierungsregel Beschreibung für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="102cf-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="102cf-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="102cf-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="102cf-119">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="102cf-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="102cf-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="102cf-120">PARAMETERS</span></span>

### <span data-ttu-id="102cf-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="102cf-121">-AliasName</span></span>
<span data-ttu-id="102cf-122">GeoDR-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="102cf-122">GeoDR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="102cf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102cf-123">-DefaultProfile</span></span>
<span data-ttu-id="102cf-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="102cf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="102cf-125">-Name</span><span class="sxs-lookup"><span data-stu-id="102cf-125">-Name</span></span>
<span data-ttu-id="102cf-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="102cf-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="102cf-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="102cf-127">-Namespace</span></span>
<span data-ttu-id="102cf-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="102cf-128">Namespace Name</span></span>

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

### <span data-ttu-id="102cf-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="102cf-129">-Queue</span></span>
<span data-ttu-id="102cf-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="102cf-130">Queue Name</span></span>

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

### <span data-ttu-id="102cf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="102cf-131">-ResourceGroupName</span></span>
<span data-ttu-id="102cf-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="102cf-132">Resource Group Name</span></span>

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

### <span data-ttu-id="102cf-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="102cf-133">-Topic</span></span>
<span data-ttu-id="102cf-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="102cf-134">Topic Name</span></span>

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

### <span data-ttu-id="102cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102cf-135">CommonParameters</span></span>
<span data-ttu-id="102cf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="102cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102cf-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="102cf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102cf-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="102cf-138">INPUTS</span></span>

### <span data-ttu-id="102cf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="102cf-139">System.String</span></span>

## <span data-ttu-id="102cf-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="102cf-140">OUTPUTS</span></span>

### <span data-ttu-id="102cf-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="102cf-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="102cf-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="102cf-142">NOTES</span></span>

## <span data-ttu-id="102cf-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="102cf-143">RELATED LINKS</span></span>
