---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664436"
---
# <span data-ttu-id="4bc58-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="4bc58-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="4bc58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bc58-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc58-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für den ServiceBus-Namespace oder die Warteschlange oder das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="4bc58-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bc58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bc58-104">SYNTAX</span></span>

### <span data-ttu-id="4bc58-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4bc58-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bc58-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bc58-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bc58-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bc58-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bc58-108">DESCRIPTION</span></span>
<span data-ttu-id="4bc58-109">Mit dem Cmdlet **New-AzureRmServiceBusKey** werden neue primäre oder sekundäre Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema und die Autorisierungsregel generiert.</span><span class="sxs-lookup"><span data-stu-id="4bc58-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="4bc58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bc58-110">EXAMPLES</span></span>

### <span data-ttu-id="4bc58-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4bc58-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="4bc58-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="4bc58-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="4bc58-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4bc58-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="4bc58-114">Generiert die primären oder sekundären Verbindungszeichenfolgen für die Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="4bc58-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="4bc58-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4bc58-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="4bc58-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="4bc58-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="4bc58-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bc58-117">PARAMETERS</span></span>

### <span data-ttu-id="4bc58-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bc58-118">-Confirm</span></span>
<span data-ttu-id="4bc58-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bc58-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc58-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4bc58-120">-Name</span></span>
<span data-ttu-id="4bc58-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="4bc58-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="4bc58-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4bc58-122">-Namespace</span></span>
<span data-ttu-id="4bc58-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="4bc58-123">Namespace Name.</span></span>

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

### <span data-ttu-id="4bc58-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="4bc58-124">-Queue</span></span>
<span data-ttu-id="4bc58-125">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="4bc58-125">Queue Name.</span></span>

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

### <span data-ttu-id="4bc58-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="4bc58-126">-RegenerateKey</span></span>
<span data-ttu-id="4bc58-127">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="4bc58-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc58-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc58-128">-ResourceGroupName</span></span>
<span data-ttu-id="4bc58-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4bc58-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="4bc58-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="4bc58-130">-Topic</span></span>
<span data-ttu-id="4bc58-131">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="4bc58-131">Topic Name.</span></span>

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

### <span data-ttu-id="4bc58-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc58-132">-WhatIf</span></span>
<span data-ttu-id="4bc58-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bc58-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc58-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bc58-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc58-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc58-135">-DefaultProfile</span></span>
<span data-ttu-id="4bc58-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4bc58-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bc58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc58-137">CommonParameters</span></span>
<span data-ttu-id="4bc58-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc58-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc58-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc58-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bc58-140">INPUTS</span></span>

### <span data-ttu-id="4bc58-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4bc58-141">System.String</span></span>

## <span data-ttu-id="4bc58-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bc58-142">OUTPUTS</span></span>

### <span data-ttu-id="4bc58-143">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4bc58-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="4bc58-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bc58-144">NOTES</span></span>

## <span data-ttu-id="4bc58-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bc58-145">RELATED LINKS</span></span>

