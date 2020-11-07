---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 4717775f840d816b8f99cc64c4036d5563e8d849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659419"
---
# <span data-ttu-id="90509-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="90509-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="90509-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90509-102">SYNOPSIS</span></span>
<span data-ttu-id="90509-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema oder einen Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="90509-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="90509-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90509-104">SYNTAX</span></span>

### <span data-ttu-id="90509-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="90509-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90509-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="90509-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90509-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="90509-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90509-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="90509-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90509-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90509-109">DESCRIPTION</span></span>
<span data-ttu-id="90509-110">Das Cmdlet " **Get-AzServiceBusAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in einer Warteschlange oder einem Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="90509-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="90509-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90509-111">EXAMPLES</span></span>

### <span data-ttu-id="90509-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90509-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="90509-113">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="90509-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="90509-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="90509-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="90509-115">Gibt die angegebene Autorisierungsregel Beschreibung für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="90509-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="90509-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="90509-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="90509-117">Gibt die angegebene Autorisierungsregel Beschreibung für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="90509-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="90509-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="90509-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="90509-119">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="90509-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="90509-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="90509-120">PARAMETERS</span></span>

### <span data-ttu-id="90509-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="90509-121">-AliasName</span></span>
<span data-ttu-id="90509-122">GeoDR-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="90509-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="90509-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90509-123">-DefaultProfile</span></span>
<span data-ttu-id="90509-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90509-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90509-125">-Name</span><span class="sxs-lookup"><span data-stu-id="90509-125">-Name</span></span>
<span data-ttu-id="90509-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="90509-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="90509-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="90509-127">-Namespace</span></span>
<span data-ttu-id="90509-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="90509-128">Namespace Name</span></span>

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

### <span data-ttu-id="90509-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="90509-129">-Queue</span></span>
<span data-ttu-id="90509-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="90509-130">Queue Name</span></span>

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

### <span data-ttu-id="90509-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90509-131">-ResourceGroupName</span></span>
<span data-ttu-id="90509-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="90509-132">Resource Group Name</span></span>

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

### <span data-ttu-id="90509-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="90509-133">-Topic</span></span>
<span data-ttu-id="90509-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="90509-134">Topic Name</span></span>

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

### <span data-ttu-id="90509-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90509-135">CommonParameters</span></span>
<span data-ttu-id="90509-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90509-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90509-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90509-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90509-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90509-138">INPUTS</span></span>

### <span data-ttu-id="90509-139">System. String</span><span class="sxs-lookup"><span data-stu-id="90509-139">System.String</span></span>

## <span data-ttu-id="90509-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90509-140">OUTPUTS</span></span>

### <span data-ttu-id="90509-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="90509-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="90509-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="90509-142">NOTES</span></span>

## <span data-ttu-id="90509-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90509-143">RELATED LINKS</span></span>
