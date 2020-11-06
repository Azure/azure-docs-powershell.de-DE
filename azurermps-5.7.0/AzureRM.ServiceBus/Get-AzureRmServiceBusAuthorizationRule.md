---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480906"
---
# <span data-ttu-id="d6827-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d6827-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="d6827-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6827-102">SYNOPSIS</span></span>
<span data-ttu-id="d6827-103">Ruft eine Beschreibung der angegebenen Autorisierungsregel für einen bestimmten Namespace oder eine bestimmte Warteschlange oder ein bestimmtes Thema oder einen Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="d6827-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6827-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6827-104">SYNTAX</span></span>

### <span data-ttu-id="d6827-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6827-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6827-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6827-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6827-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6827-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6827-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6827-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6827-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6827-109">DESCRIPTION</span></span>
<span data-ttu-id="d6827-110">Das Cmdlet " **Get-AzureRmServiceBusAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel im angegebenen Namespace oder in einer Warteschlange oder einem Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="d6827-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="d6827-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6827-111">EXAMPLES</span></span>

### <span data-ttu-id="d6827-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6827-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="d6827-113">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="d6827-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="d6827-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d6827-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="d6827-115">Gibt die angegebene Autorisierungsregel Beschreibung für eine angegebene Warteschlange zurück.</span><span class="sxs-lookup"><span data-stu-id="d6827-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="d6827-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d6827-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="d6827-117">Gibt die angegebene Autorisierungsregel Beschreibung für ein angegebenes Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="d6827-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="d6827-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d6827-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="d6827-119">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace und Alias zurück.</span><span class="sxs-lookup"><span data-stu-id="d6827-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="d6827-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6827-120">PARAMETERS</span></span>

### <span data-ttu-id="d6827-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="d6827-121">-AliasName</span></span>
<span data-ttu-id="d6827-122">GeoDR-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="d6827-122">GeoDR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6827-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6827-123">-DefaultProfile</span></span>
<span data-ttu-id="d6827-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6827-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6827-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d6827-125">-Name</span></span>
<span data-ttu-id="d6827-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="d6827-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6827-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d6827-127">-Namespace</span></span>
<span data-ttu-id="d6827-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d6827-128">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6827-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="d6827-129">-Queue</span></span>
<span data-ttu-id="d6827-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="d6827-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6827-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6827-131">-ResourceGroupName</span></span>
<span data-ttu-id="d6827-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d6827-132">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6827-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="d6827-133">-Topic</span></span>
<span data-ttu-id="d6827-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="d6827-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6827-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6827-135">CommonParameters</span></span>
<span data-ttu-id="d6827-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6827-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d6827-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6827-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6827-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6827-138">INPUTS</span></span>

### <span data-ttu-id="d6827-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d6827-139">System.String</span></span>


## <span data-ttu-id="d6827-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6827-140">OUTPUTS</span></span>

### <span data-ttu-id="d6827-141">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d6827-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="d6827-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6827-142">NOTES</span></span>

## <span data-ttu-id="d6827-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6827-143">RELATED LINKS</span></span>
