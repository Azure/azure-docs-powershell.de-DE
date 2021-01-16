---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297190"
---
# <span data-ttu-id="126bc-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="126bc-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="126bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="126bc-102">SYNOPSIS</span></span>
<span data-ttu-id="126bc-103">Ruft die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder topic oder alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="126bc-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="126bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="126bc-104">SYNTAX</span></span>

### <span data-ttu-id="126bc-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="126bc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="126bc-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="126bc-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="126bc-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="126bc-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="126bc-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="126bc-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="126bc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="126bc-109">DESCRIPTION</span></span>
<span data-ttu-id="126bc-110">Das **Cmdlet "Get-AzServiceBusKey"** gibt die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange bzw. für topic oder alias (GeoDR Configurations) zurück.</span><span class="sxs-lookup"><span data-stu-id="126bc-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="126bc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="126bc-111">EXAMPLES</span></span>

### <span data-ttu-id="126bc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="126bc-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="126bc-113">Primäre und sekundäre Verbindungszeichenfolge zum angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="126bc-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="126bc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="126bc-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="126bc-115">Primäre und sekundäre Verbindungszeichenfolge zur angegebenen Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="126bc-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="126bc-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="126bc-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="126bc-117">Primäre und sekundäre Verbindungszeichenfolge zum angegebenen Thema.</span><span class="sxs-lookup"><span data-stu-id="126bc-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="126bc-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="126bc-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="126bc-119">Primäre und sekundäre Verbindungszeichenfolge zum angegebenen Namespace und Alias.</span><span class="sxs-lookup"><span data-stu-id="126bc-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="126bc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="126bc-120">PARAMETERS</span></span>

### <span data-ttu-id="126bc-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="126bc-121">-AliasName</span></span>
<span data-ttu-id="126bc-122">Aliasname</span><span class="sxs-lookup"><span data-stu-id="126bc-122">Alias Name</span></span>

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

### <span data-ttu-id="126bc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126bc-123">-DefaultProfile</span></span>
<span data-ttu-id="126bc-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="126bc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="126bc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="126bc-125">-Name</span></span>
<span data-ttu-id="126bc-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="126bc-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="126bc-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="126bc-127">-Namespace</span></span>
<span data-ttu-id="126bc-128">Namespacename</span><span class="sxs-lookup"><span data-stu-id="126bc-128">Namespace Name</span></span>

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

### <span data-ttu-id="126bc-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="126bc-129">-Queue</span></span>
<span data-ttu-id="126bc-130">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="126bc-130">Queue Name</span></span>

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

### <span data-ttu-id="126bc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="126bc-131">-ResourceGroupName</span></span>
<span data-ttu-id="126bc-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="126bc-132">Resource Group Name</span></span>

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

### <span data-ttu-id="126bc-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="126bc-133">-Topic</span></span>
<span data-ttu-id="126bc-134">Themaname</span><span class="sxs-lookup"><span data-stu-id="126bc-134">Topic Name</span></span>

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

### <span data-ttu-id="126bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126bc-135">CommonParameters</span></span>
<span data-ttu-id="126bc-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126bc-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="126bc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126bc-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="126bc-138">INPUTS</span></span>

### <span data-ttu-id="126bc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="126bc-139">System.String</span></span>

## <span data-ttu-id="126bc-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="126bc-140">OUTPUTS</span></span>

### <span data-ttu-id="126bc-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="126bc-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="126bc-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="126bc-142">NOTES</span></span>

## <span data-ttu-id="126bc-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="126bc-143">RELATED LINKS</span></span>
