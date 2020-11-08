---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003958"
---
# <span data-ttu-id="cfc70-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="cfc70-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="cfc70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cfc70-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc70-103">Ruft die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema oder den Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="cfc70-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="cfc70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfc70-104">SYNTAX</span></span>

### <span data-ttu-id="cfc70-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cfc70-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfc70-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfc70-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfc70-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfc70-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfc70-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfc70-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfc70-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfc70-109">DESCRIPTION</span></span>
<span data-ttu-id="cfc70-110">Das Cmdlet " **Get-AzServiceBusKey** " gibt die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema oder den Alias (GeoDR-Konfigurationen) zurück.</span><span class="sxs-lookup"><span data-stu-id="cfc70-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="cfc70-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfc70-111">EXAMPLES</span></span>

### <span data-ttu-id="cfc70-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cfc70-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="cfc70-113">Primäre und sekundäre Verbindungszeichenfolge für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="cfc70-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="cfc70-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cfc70-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="cfc70-115">Primäre und sekundäre Verbindungszeichenfolge zur angegebenen Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="cfc70-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="cfc70-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cfc70-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="cfc70-117">Primäre und sekundäre Verbindungszeichenfolge für das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="cfc70-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="cfc70-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cfc70-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="cfc70-119">Primäre und sekundäre Verbindungszeichenfolge für den angegebenen Namespace und Alias.</span><span class="sxs-lookup"><span data-stu-id="cfc70-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="cfc70-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfc70-120">PARAMETERS</span></span>

### <span data-ttu-id="cfc70-121">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="cfc70-121">-AliasName</span></span>
<span data-ttu-id="cfc70-122">Alias Name</span><span class="sxs-lookup"><span data-stu-id="cfc70-122">Alias Name</span></span>

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

### <span data-ttu-id="cfc70-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc70-123">-DefaultProfile</span></span>
<span data-ttu-id="cfc70-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cfc70-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc70-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cfc70-125">-Name</span></span>
<span data-ttu-id="cfc70-126">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="cfc70-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="cfc70-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cfc70-127">-Namespace</span></span>
<span data-ttu-id="cfc70-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="cfc70-128">Namespace Name</span></span>

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

### <span data-ttu-id="cfc70-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="cfc70-129">-Queue</span></span>
<span data-ttu-id="cfc70-130">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="cfc70-130">Queue Name</span></span>

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

### <span data-ttu-id="cfc70-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfc70-131">-ResourceGroupName</span></span>
<span data-ttu-id="cfc70-132">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="cfc70-132">Resource Group Name</span></span>

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

### <span data-ttu-id="cfc70-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="cfc70-133">-Topic</span></span>
<span data-ttu-id="cfc70-134">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="cfc70-134">Topic Name</span></span>

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

### <span data-ttu-id="cfc70-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc70-135">CommonParameters</span></span>
<span data-ttu-id="cfc70-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc70-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc70-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc70-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc70-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cfc70-138">INPUTS</span></span>

### <span data-ttu-id="cfc70-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc70-139">System.String</span></span>

## <span data-ttu-id="cfc70-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cfc70-140">OUTPUTS</span></span>

### <span data-ttu-id="cfc70-141">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="cfc70-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="cfc70-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="cfc70-142">NOTES</span></span>

## <span data-ttu-id="cfc70-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cfc70-143">RELATED LINKS</span></span>
