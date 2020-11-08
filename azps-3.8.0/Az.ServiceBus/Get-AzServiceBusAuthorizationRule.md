---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003963"
---
# <span data-ttu-id="6b536-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6b536-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="6b536-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b536-102">SYNOPSIS</span></span>
<span data-ttu-id="6b536-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema oder einen Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="6b536-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="6b536-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b536-104">SYNTAX</span></span>

### <span data-ttu-id="6b536-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b536-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b536-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b536-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b536-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b536-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b536-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b536-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b536-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b536-109">DESCRIPTION</span></span>
<span data-ttu-id="6b536-110">Das Cmdlet " **Get-AzServiceBusAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in einer Warteschlange oder einem Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="6b536-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="6b536-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b536-111">EXAMPLES</span></span>

### <span data-ttu-id="6b536-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b536-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="6b536-113">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="6b536-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="6b536-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6b536-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="6b536-115">Gibt die angegebene Autorisierungsregel Beschreibung für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="6b536-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="6b536-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6b536-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="6b536-117">Gibt die angegebene Autorisierungsregel Beschreibung für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="6b536-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="6b536-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="6b536-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="6b536-119">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="6b536-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="6b536-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b536-120">PARAMETERS</span></span>

### <span data-ttu-id="6b536-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="6b536-121">-AliasName</span></span>
<span data-ttu-id="6b536-122">GeoDR-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="6b536-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="6b536-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b536-123">-DefaultProfile</span></span>
<span data-ttu-id="6b536-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b536-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b536-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6b536-125">-Name</span></span>
<span data-ttu-id="6b536-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="6b536-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="6b536-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6b536-127">-Namespace</span></span>
<span data-ttu-id="6b536-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="6b536-128">Namespace Name</span></span>

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

### <span data-ttu-id="6b536-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="6b536-129">-Queue</span></span>
<span data-ttu-id="6b536-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="6b536-130">Queue Name</span></span>

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

### <span data-ttu-id="6b536-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b536-131">-ResourceGroupName</span></span>
<span data-ttu-id="6b536-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6b536-132">Resource Group Name</span></span>

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

### <span data-ttu-id="6b536-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="6b536-133">-Topic</span></span>
<span data-ttu-id="6b536-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="6b536-134">Topic Name</span></span>

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

### <span data-ttu-id="6b536-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b536-135">CommonParameters</span></span>
<span data-ttu-id="6b536-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b536-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b536-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b536-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b536-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b536-138">INPUTS</span></span>

### <span data-ttu-id="6b536-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6b536-139">System.String</span></span>

## <span data-ttu-id="6b536-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b536-140">OUTPUTS</span></span>

### <span data-ttu-id="6b536-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6b536-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6b536-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b536-142">NOTES</span></span>

## <span data-ttu-id="6b536-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b536-143">RELATED LINKS</span></span>
