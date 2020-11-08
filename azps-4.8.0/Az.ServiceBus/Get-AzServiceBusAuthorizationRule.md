---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008946"
---
# <span data-ttu-id="ae525-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae525-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ae525-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae525-102">SYNOPSIS</span></span>
<span data-ttu-id="ae525-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema oder einen Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="ae525-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="ae525-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae525-104">SYNTAX</span></span>

### <span data-ttu-id="ae525-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ae525-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae525-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ae525-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae525-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ae525-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae525-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="ae525-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae525-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae525-109">DESCRIPTION</span></span>
<span data-ttu-id="ae525-110">Das Cmdlet " **Get-AzServiceBusAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in einer Warteschlange oder einem Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="ae525-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="ae525-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae525-111">EXAMPLES</span></span>

### <span data-ttu-id="ae525-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae525-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="ae525-113">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="ae525-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="ae525-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ae525-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="ae525-115">Gibt die angegebene Autorisierungsregel Beschreibung für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="ae525-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="ae525-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ae525-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="ae525-117">Gibt die angegebene Autorisierungsregel Beschreibung für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="ae525-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="ae525-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ae525-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="ae525-119">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="ae525-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="ae525-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae525-120">PARAMETERS</span></span>

### <span data-ttu-id="ae525-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="ae525-121">-AliasName</span></span>
<span data-ttu-id="ae525-122">GeoDR-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="ae525-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="ae525-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae525-123">-DefaultProfile</span></span>
<span data-ttu-id="ae525-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae525-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae525-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ae525-125">-Name</span></span>
<span data-ttu-id="ae525-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="ae525-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ae525-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ae525-127">-Namespace</span></span>
<span data-ttu-id="ae525-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ae525-128">Namespace Name</span></span>

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

### <span data-ttu-id="ae525-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="ae525-129">-Queue</span></span>
<span data-ttu-id="ae525-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="ae525-130">Queue Name</span></span>

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

### <span data-ttu-id="ae525-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae525-131">-ResourceGroupName</span></span>
<span data-ttu-id="ae525-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ae525-132">Resource Group Name</span></span>

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

### <span data-ttu-id="ae525-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="ae525-133">-Topic</span></span>
<span data-ttu-id="ae525-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="ae525-134">Topic Name</span></span>

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

### <span data-ttu-id="ae525-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae525-135">CommonParameters</span></span>
<span data-ttu-id="ae525-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae525-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae525-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae525-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae525-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae525-138">INPUTS</span></span>

### <span data-ttu-id="ae525-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ae525-139">System.String</span></span>

## <span data-ttu-id="ae525-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae525-140">OUTPUTS</span></span>

### <span data-ttu-id="ae525-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ae525-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ae525-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae525-142">NOTES</span></span>

## <span data-ttu-id="ae525-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae525-143">RELATED LINKS</span></span>
