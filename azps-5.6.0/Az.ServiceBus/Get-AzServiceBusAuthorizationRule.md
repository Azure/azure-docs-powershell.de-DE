---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 39f43af6685f754cacfd1340560fd4c3429f792d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923456"
---
# <span data-ttu-id="99f29-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="99f29-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="99f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f29-102">SYNOPSIS</span></span>
<span data-ttu-id="99f29-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine Warteschlange oder ein Thema oder alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="99f29-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="99f29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99f29-104">SYNTAX</span></span>

### <span data-ttu-id="99f29-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="99f29-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f29-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f29-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f29-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f29-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f29-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f29-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99f29-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99f29-109">DESCRIPTION</span></span>
<span data-ttu-id="99f29-110">Das **Get-AzServiceBusAuthorizationRule-Cmdlet** ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in der Warteschlange oder im Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="99f29-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="99f29-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99f29-111">EXAMPLES</span></span>

### <span data-ttu-id="99f29-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99f29-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="99f29-113">Gibt die angegebene Beschreibung der Autorisierungsregel für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="99f29-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="99f29-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="99f29-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="99f29-115">Gibt die angegebene Beschreibung der Autorisierungsregel für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="99f29-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="99f29-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="99f29-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="99f29-117">Gibt die angegebene Beschreibung der Autorisierungsregel für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="99f29-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="99f29-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="99f29-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="99f29-119">Gibt die angegebene Beschreibung der Autorisierungsregel für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="99f29-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="99f29-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99f29-120">PARAMETERS</span></span>

### <span data-ttu-id="99f29-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="99f29-121">-AliasName</span></span>
<span data-ttu-id="99f29-122">Name der GeoDR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="99f29-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="99f29-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f29-123">-DefaultProfile</span></span>
<span data-ttu-id="99f29-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99f29-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f29-125">-Name</span><span class="sxs-lookup"><span data-stu-id="99f29-125">-Name</span></span>
<span data-ttu-id="99f29-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="99f29-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="99f29-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="99f29-127">-Namespace</span></span>
<span data-ttu-id="99f29-128">Namespacename</span><span class="sxs-lookup"><span data-stu-id="99f29-128">Namespace Name</span></span>

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

### <span data-ttu-id="99f29-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="99f29-129">-Queue</span></span>
<span data-ttu-id="99f29-130">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="99f29-130">Queue Name</span></span>

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

### <span data-ttu-id="99f29-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f29-131">-ResourceGroupName</span></span>
<span data-ttu-id="99f29-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="99f29-132">Resource Group Name</span></span>

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

### <span data-ttu-id="99f29-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="99f29-133">-Topic</span></span>
<span data-ttu-id="99f29-134">Topic Name</span><span class="sxs-lookup"><span data-stu-id="99f29-134">Topic Name</span></span>

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

### <span data-ttu-id="99f29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f29-135">CommonParameters</span></span>
<span data-ttu-id="99f29-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f29-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f29-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f29-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99f29-138">INPUTS</span></span>

### <span data-ttu-id="99f29-139">System.String</span><span class="sxs-lookup"><span data-stu-id="99f29-139">System.String</span></span>

## <span data-ttu-id="99f29-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99f29-140">OUTPUTS</span></span>

### <span data-ttu-id="99f29-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="99f29-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="99f29-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99f29-142">NOTES</span></span>

## <span data-ttu-id="99f29-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99f29-143">RELATED LINKS</span></span>
