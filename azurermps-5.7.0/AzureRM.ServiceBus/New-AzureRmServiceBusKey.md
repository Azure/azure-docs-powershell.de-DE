---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0dc0e2ebf22d995577abd37e2eef2b16b0ea4001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500409"
---
# <span data-ttu-id="c3fb7-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="c3fb7-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="c3fb7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fb7-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für den ServiceBus-Namespace oder die Warteschlange oder das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3fb7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3fb7-104">SYNTAX</span></span>

### <span data-ttu-id="c3fb7-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3fb7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fb7-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3fb7-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3fb7-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c3fb7-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3fb7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3fb7-108">DESCRIPTION</span></span>
<span data-ttu-id="c3fb7-109">Mit dem Cmdlet **New-AzureRmServiceBusKey** werden neue primäre oder sekundäre Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema und die Autorisierungsregel generiert.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="c3fb7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3fb7-110">EXAMPLES</span></span>

### <span data-ttu-id="c3fb7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3fb7-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c3fb7-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="c3fb7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3fb7-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c3fb7-114">Generiert die primären oder sekundären Verbindungszeichenfolgen für die Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="c3fb7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c3fb7-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c3fb7-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="c3fb7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3fb7-117">PARAMETERS</span></span>

### <span data-ttu-id="c3fb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fb7-118">-DefaultProfile</span></span>
<span data-ttu-id="c3fb7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3fb7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c3fb7-120">-Name</span></span>
<span data-ttu-id="c3fb7-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fb7-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c3fb7-122">-Namespace</span></span>
<span data-ttu-id="c3fb7-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c3fb7-123">Namespace Name</span></span>

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

### <span data-ttu-id="c3fb7-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="c3fb7-124">-Queue</span></span>
<span data-ttu-id="c3fb7-125">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="c3fb7-125">Queue Name</span></span>

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

### <span data-ttu-id="c3fb7-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c3fb7-126">-RegenerateKey</span></span>
<span data-ttu-id="c3fb7-127">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="c3fb7-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fb7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fb7-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3fb7-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c3fb7-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c3fb7-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="c3fb7-130">-Topic</span></span>
<span data-ttu-id="c3fb7-131">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="c3fb7-131">Topic Name</span></span>

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

### <span data-ttu-id="c3fb7-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3fb7-132">-Confirm</span></span>
<span data-ttu-id="c3fb7-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fb7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3fb7-134">-WhatIf</span></span>
<span data-ttu-id="c3fb7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3fb7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fb7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fb7-137">CommonParameters</span></span>
<span data-ttu-id="c3fb7-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3fb7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c3fb7-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fb7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fb7-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3fb7-140">INPUTS</span></span>

### <span data-ttu-id="c3fb7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c3fb7-141">System.String</span></span>


## <span data-ttu-id="c3fb7-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3fb7-142">OUTPUTS</span></span>

### <span data-ttu-id="c3fb7-143">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c3fb7-143">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="c3fb7-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3fb7-144">NOTES</span></span>

## <span data-ttu-id="c3fb7-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3fb7-145">RELATED LINKS</span></span>
