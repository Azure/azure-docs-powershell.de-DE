---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: 28ecd68167a7db2f41ee64a38a4616548707096c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932248"
---
# <span data-ttu-id="3c63c-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="3c63c-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="3c63c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c63c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c63c-103">Ruft die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder Warteschlange oder Thema oder Alias (GeoDR-Konfigurationen) ab.</span><span class="sxs-lookup"><span data-stu-id="3c63c-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="3c63c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c63c-104">SYNTAX</span></span>

### <span data-ttu-id="3c63c-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c63c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c63c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c63c-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c63c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c63c-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c63c-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c63c-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c63c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c63c-109">DESCRIPTION</span></span>
<span data-ttu-id="3c63c-110">Das **Get-AzServiceBusKey-Cmdlet** gibt die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder queue oder Topic or Alias (GeoDR Configurations) zurück.</span><span class="sxs-lookup"><span data-stu-id="3c63c-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="3c63c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c63c-111">EXAMPLES</span></span>

### <span data-ttu-id="3c63c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c63c-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="3c63c-113">Primäre und sekundäre Verbindungszeichenfolge zum angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="3c63c-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="3c63c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3c63c-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="3c63c-115">Primäre und sekundäre Verbindungszeichenfolge zur angegebenen Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="3c63c-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="3c63c-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3c63c-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="3c63c-117">Primäre und sekundäre Verbindungszeichenfolge zum angegebenen Thema.</span><span class="sxs-lookup"><span data-stu-id="3c63c-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="3c63c-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="3c63c-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="3c63c-119">Primäre und sekundäre Verbindungszeichenfolge zum angegebenen Namespace und Alias.</span><span class="sxs-lookup"><span data-stu-id="3c63c-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="3c63c-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3c63c-120">PARAMETERS</span></span>

### <span data-ttu-id="3c63c-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="3c63c-121">-AliasName</span></span>
<span data-ttu-id="3c63c-122">Aliasname</span><span class="sxs-lookup"><span data-stu-id="3c63c-122">Alias Name</span></span>

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

### <span data-ttu-id="3c63c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c63c-123">-DefaultProfile</span></span>
<span data-ttu-id="3c63c-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c63c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c63c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3c63c-125">-Name</span></span>
<span data-ttu-id="3c63c-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="3c63c-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="3c63c-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3c63c-127">-Namespace</span></span>
<span data-ttu-id="3c63c-128">Namespacename</span><span class="sxs-lookup"><span data-stu-id="3c63c-128">Namespace Name</span></span>

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

### <span data-ttu-id="3c63c-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="3c63c-129">-Queue</span></span>
<span data-ttu-id="3c63c-130">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="3c63c-130">Queue Name</span></span>

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

### <span data-ttu-id="3c63c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c63c-131">-ResourceGroupName</span></span>
<span data-ttu-id="3c63c-132">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3c63c-132">Resource Group Name</span></span>

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

### <span data-ttu-id="3c63c-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="3c63c-133">-Topic</span></span>
<span data-ttu-id="3c63c-134">Topic Name</span><span class="sxs-lookup"><span data-stu-id="3c63c-134">Topic Name</span></span>

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

### <span data-ttu-id="3c63c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c63c-135">CommonParameters</span></span>
<span data-ttu-id="3c63c-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c63c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c63c-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c63c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c63c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c63c-138">INPUTS</span></span>

### <span data-ttu-id="3c63c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3c63c-139">System.String</span></span>

## <span data-ttu-id="3c63c-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c63c-140">OUTPUTS</span></span>

### <span data-ttu-id="3c63c-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3c63c-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="3c63c-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3c63c-142">NOTES</span></span>

## <span data-ttu-id="3c63c-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3c63c-143">RELATED LINKS</span></span>
