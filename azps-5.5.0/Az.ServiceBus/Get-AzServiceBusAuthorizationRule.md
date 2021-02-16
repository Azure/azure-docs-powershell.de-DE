---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168916"
---
# <span data-ttu-id="95dff-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95dff-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="95dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95dff-102">SYNOPSIS</span></span>
<span data-ttu-id="95dff-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine Warteschlange oder ein Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="95dff-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="95dff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95dff-104">SYNTAX</span></span>

### <span data-ttu-id="95dff-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95dff-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95dff-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="95dff-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95dff-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="95dff-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95dff-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="95dff-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95dff-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95dff-109">DESCRIPTION</span></span>
<span data-ttu-id="95dff-110">Das **Cmdlet "Get-AzServiceBusAuthorizationRule"** ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in der angegebenen Warteschlange oder im Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="95dff-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="95dff-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95dff-111">EXAMPLES</span></span>

### <span data-ttu-id="95dff-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95dff-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="95dff-113">Gibt die Beschreibung der angegebenen Autorisierungsregel für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="95dff-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="95dff-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95dff-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="95dff-115">Gibt die Beschreibung der angegebenen Autorisierungsregel für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="95dff-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="95dff-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="95dff-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="95dff-117">Gibt die Beschreibung der angegebenen Autorisierungsregel für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="95dff-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="95dff-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="95dff-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="95dff-119">Gibt die Beschreibung der angegebenen Autorisierungsregel für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="95dff-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="95dff-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95dff-120">PARAMETERS</span></span>

### <span data-ttu-id="95dff-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="95dff-121">-AliasName</span></span>
<span data-ttu-id="95dff-122">Name der GeoDR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="95dff-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="95dff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95dff-123">-DefaultProfile</span></span>
<span data-ttu-id="95dff-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95dff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95dff-125">-Name</span><span class="sxs-lookup"><span data-stu-id="95dff-125">-Name</span></span>
<span data-ttu-id="95dff-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="95dff-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="95dff-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="95dff-127">-Namespace</span></span>
<span data-ttu-id="95dff-128">Namespacename</span><span class="sxs-lookup"><span data-stu-id="95dff-128">Namespace Name</span></span>

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

### <span data-ttu-id="95dff-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="95dff-129">-Queue</span></span>
<span data-ttu-id="95dff-130">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="95dff-130">Queue Name</span></span>

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

### <span data-ttu-id="95dff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95dff-131">-ResourceGroupName</span></span>
<span data-ttu-id="95dff-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="95dff-132">Resource Group Name</span></span>

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

### <span data-ttu-id="95dff-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="95dff-133">-Topic</span></span>
<span data-ttu-id="95dff-134">Themaname</span><span class="sxs-lookup"><span data-stu-id="95dff-134">Topic Name</span></span>

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

### <span data-ttu-id="95dff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95dff-135">CommonParameters</span></span>
<span data-ttu-id="95dff-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95dff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95dff-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95dff-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95dff-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95dff-138">INPUTS</span></span>

### <span data-ttu-id="95dff-139">System.String</span><span class="sxs-lookup"><span data-stu-id="95dff-139">System.String</span></span>

## <span data-ttu-id="95dff-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95dff-140">OUTPUTS</span></span>

### <span data-ttu-id="95dff-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="95dff-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="95dff-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95dff-142">NOTES</span></span>

## <span data-ttu-id="95dff-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95dff-143">RELATED LINKS</span></span>
