---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 96b95a4a6641e3bcfc2c1a18653da4231bee5c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477686"
---
# <span data-ttu-id="d8601-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="d8601-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="d8601-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8601-102">SYNOPSIS</span></span>
<span data-ttu-id="d8601-103">Ruft die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema oder den Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="d8601-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8601-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8601-104">SYNTAX</span></span>

### <span data-ttu-id="d8601-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8601-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8601-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8601-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8601-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8601-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8601-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="d8601-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8601-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8601-109">DESCRIPTION</span></span>
<span data-ttu-id="d8601-110">Das Cmdlet " **Get-AzureRmServiceBusKey** " gibt die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema oder den Alias (GeoDR-Konfigurationen) zurück.</span><span class="sxs-lookup"><span data-stu-id="d8601-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="d8601-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8601-111">EXAMPLES</span></span>

### <span data-ttu-id="d8601-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8601-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="d8601-113">Primäre und sekundäre Verbindungszeichenfolge für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="d8601-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="d8601-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d8601-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="d8601-115">Primäre und sekundäre Verbindungszeichenfolge zur angegebenen Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="d8601-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="d8601-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d8601-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="d8601-117">Primäre und sekundäre Verbindungszeichenfolge für das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="d8601-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="d8601-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d8601-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="d8601-119">Primäre und sekundäre Verbindungszeichenfolge für den angegebenen Namespace und Alias.</span><span class="sxs-lookup"><span data-stu-id="d8601-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="d8601-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8601-120">PARAMETERS</span></span>

### <span data-ttu-id="d8601-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="d8601-121">-AliasName</span></span>
<span data-ttu-id="d8601-122">Alias Name</span><span class="sxs-lookup"><span data-stu-id="d8601-122">Alias Name</span></span>

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

### <span data-ttu-id="d8601-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8601-123">-DefaultProfile</span></span>
<span data-ttu-id="d8601-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8601-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8601-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d8601-125">-Name</span></span>
<span data-ttu-id="d8601-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="d8601-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8601-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d8601-127">-Namespace</span></span>
<span data-ttu-id="d8601-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d8601-128">Namespace Name</span></span>

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

### <span data-ttu-id="d8601-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="d8601-129">-Queue</span></span>
<span data-ttu-id="d8601-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="d8601-130">Queue Name</span></span>

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

### <span data-ttu-id="d8601-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8601-131">-ResourceGroupName</span></span>
<span data-ttu-id="d8601-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d8601-132">Resource Group Name</span></span>

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

### <span data-ttu-id="d8601-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="d8601-133">-Topic</span></span>
<span data-ttu-id="d8601-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="d8601-134">Topic Name</span></span>

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

### <span data-ttu-id="d8601-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8601-135">CommonParameters</span></span>
<span data-ttu-id="d8601-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8601-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8601-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8601-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8601-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8601-138">INPUTS</span></span>

### <span data-ttu-id="d8601-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d8601-139">System.String</span></span>

## <span data-ttu-id="d8601-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8601-140">OUTPUTS</span></span>

### <span data-ttu-id="d8601-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="d8601-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="d8601-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8601-142">NOTES</span></span>

## <span data-ttu-id="d8601-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8601-143">RELATED LINKS</span></span>
