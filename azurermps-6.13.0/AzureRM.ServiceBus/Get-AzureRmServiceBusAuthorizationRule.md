---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 8c69ab59f539180c3146f01c7a5fce9907b40c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662296"
---
# <span data-ttu-id="287fa-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="287fa-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="287fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="287fa-102">SYNOPSIS</span></span>
<span data-ttu-id="287fa-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema oder einen Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="287fa-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="287fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="287fa-104">SYNTAX</span></span>

### <span data-ttu-id="287fa-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="287fa-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="287fa-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="287fa-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="287fa-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="287fa-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="287fa-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="287fa-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="287fa-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="287fa-109">DESCRIPTION</span></span>
<span data-ttu-id="287fa-110">Das Cmdlet " **Get-AzureRmServiceBusAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in einer Warteschlange oder einem Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="287fa-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="287fa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="287fa-111">EXAMPLES</span></span>

### <span data-ttu-id="287fa-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="287fa-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="287fa-113">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="287fa-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="287fa-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="287fa-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="287fa-115">Gibt die angegebene Autorisierungsregel Beschreibung für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="287fa-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="287fa-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="287fa-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="287fa-117">Gibt die angegebene Autorisierungsregel Beschreibung für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="287fa-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="287fa-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="287fa-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="287fa-119">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="287fa-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="287fa-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="287fa-120">PARAMETERS</span></span>

### <span data-ttu-id="287fa-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="287fa-121">-AliasName</span></span>
<span data-ttu-id="287fa-122">GeoDR-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="287fa-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="287fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287fa-123">-DefaultProfile</span></span>
<span data-ttu-id="287fa-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="287fa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="287fa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="287fa-125">-Name</span></span>
<span data-ttu-id="287fa-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="287fa-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="287fa-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="287fa-127">-Namespace</span></span>
<span data-ttu-id="287fa-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="287fa-128">Namespace Name</span></span>

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

### <span data-ttu-id="287fa-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="287fa-129">-Queue</span></span>
<span data-ttu-id="287fa-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="287fa-130">Queue Name</span></span>

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

### <span data-ttu-id="287fa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287fa-131">-ResourceGroupName</span></span>
<span data-ttu-id="287fa-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="287fa-132">Resource Group Name</span></span>

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

### <span data-ttu-id="287fa-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="287fa-133">-Topic</span></span>
<span data-ttu-id="287fa-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="287fa-134">Topic Name</span></span>

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

### <span data-ttu-id="287fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287fa-135">CommonParameters</span></span>
<span data-ttu-id="287fa-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287fa-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287fa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287fa-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="287fa-138">INPUTS</span></span>

### <span data-ttu-id="287fa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="287fa-139">System.String</span></span>

## <span data-ttu-id="287fa-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="287fa-140">OUTPUTS</span></span>

### <span data-ttu-id="287fa-141">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="287fa-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="287fa-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="287fa-142">NOTES</span></span>

## <span data-ttu-id="287fa-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="287fa-143">RELATED LINKS</span></span>
