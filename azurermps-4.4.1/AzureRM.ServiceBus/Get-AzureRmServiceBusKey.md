---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478953"
---
# <span data-ttu-id="a7a82-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="a7a82-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="a7a82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7a82-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a82-103">Ruft die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das jeweilige Thema ab.</span><span class="sxs-lookup"><span data-stu-id="a7a82-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7a82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7a82-104">SYNTAX</span></span>

### <span data-ttu-id="a7a82-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7a82-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7a82-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7a82-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7a82-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7a82-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7a82-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7a82-108">DESCRIPTION</span></span>
<span data-ttu-id="a7a82-109">Das Cmdlet " **Get-AzureRmServiceBusKey** " gibt die primären und sekundären Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das jeweilige Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="a7a82-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="a7a82-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7a82-110">EXAMPLES</span></span>

### <span data-ttu-id="a7a82-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7a82-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="a7a82-112">Primäre und sekundäre Verbindungszeichenfolge für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="a7a82-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="a7a82-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a7a82-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="a7a82-114">Primäre und sekundäre Verbindungszeichenfolge zur angegebenen Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a7a82-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="a7a82-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a7a82-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="a7a82-116">Primäre und sekundäre Verbindungszeichenfolge für das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="a7a82-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="a7a82-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7a82-117">PARAMETERS</span></span>

### <span data-ttu-id="a7a82-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a7a82-118">-Name</span></span>
<span data-ttu-id="a7a82-119">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="a7a82-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="a7a82-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a7a82-120">-Namespace</span></span>
<span data-ttu-id="a7a82-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a7a82-121">Namespace Name.</span></span>

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

### <span data-ttu-id="a7a82-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="a7a82-122">-Queue</span></span>
<span data-ttu-id="a7a82-123">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a7a82-123">Queue Name.</span></span>

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

### <span data-ttu-id="a7a82-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a82-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7a82-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7a82-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a7a82-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="a7a82-126">-Topic</span></span>
<span data-ttu-id="a7a82-127">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="a7a82-127">Topic Name.</span></span>

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

### <span data-ttu-id="a7a82-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a82-128">-DefaultProfile</span></span>
<span data-ttu-id="a7a82-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7a82-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a82-130">CommonParameters</span></span>
<span data-ttu-id="a7a82-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a82-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a82-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a82-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7a82-133">INPUTS</span></span>

### <span data-ttu-id="a7a82-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a82-134">System.String</span></span>

## <span data-ttu-id="a7a82-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7a82-135">OUTPUTS</span></span>

### <span data-ttu-id="a7a82-136">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a7a82-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="a7a82-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7a82-137">NOTES</span></span>

## <span data-ttu-id="a7a82-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7a82-138">RELATED LINKS</span></span>

