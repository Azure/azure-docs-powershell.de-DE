---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 6efd58497adc1e59f1bf6d2c2151386ee773f66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501062"
---
# <span data-ttu-id="83ebc-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="83ebc-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="83ebc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="83ebc-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für den ServiceBus-Namespace oder die Warteschlange oder das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="83ebc-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83ebc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83ebc-104">SYNTAX</span></span>

### <span data-ttu-id="83ebc-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="83ebc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83ebc-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="83ebc-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83ebc-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="83ebc-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83ebc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83ebc-108">DESCRIPTION</span></span>
<span data-ttu-id="83ebc-109">Mit dem Cmdlet **New-AzureRmServiceBusKey** werden neue primäre oder sekundäre Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema und die Autorisierungsregel generiert.</span><span class="sxs-lookup"><span data-stu-id="83ebc-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="83ebc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83ebc-110">EXAMPLES</span></span>

### <span data-ttu-id="83ebc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83ebc-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="83ebc-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="83ebc-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="83ebc-113">Beispiel 1,1</span><span class="sxs-lookup"><span data-stu-id="83ebc-113">Example 1.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="83ebc-114">Generiert die primären oder sekundären Verbindungszeichenfolgen mit dem bereitgestellten Schlüsselwert für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="83ebc-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="83ebc-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="83ebc-115">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="83ebc-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für die Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="83ebc-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="83ebc-117">Beispiel 2,2</span><span class="sxs-lookup"><span data-stu-id="83ebc-117">Example 2.2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="83ebc-118">Generiert die primären oder sekundären Verbindungszeichenfolgen mit dem bereitgestellten Schlüsselwert für die Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="83ebc-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="83ebc-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="83ebc-119">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="83ebc-120">Generiert die primären oder sekundären Verbindungszeichenfolgen für das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="83ebc-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="83ebc-121">Beispiel 3,1</span><span class="sxs-lookup"><span data-stu-id="83ebc-121">Example 3.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="83ebc-122">Generiert die primären oder sekundären Verbindungszeichenfolgen mit dem bereitgestellten Schlüsselwert für das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="83ebc-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="83ebc-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="83ebc-123">PARAMETERS</span></span>

### <span data-ttu-id="83ebc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ebc-124">-DefaultProfile</span></span>
<span data-ttu-id="83ebc-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83ebc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ebc-126">-Keywert</span><span class="sxs-lookup"><span data-stu-id="83ebc-126">-KeyValue</span></span>
<span data-ttu-id="83ebc-127">Ein Base64-codierter 256-Bit-Schlüssel zum Signieren und Validieren des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="83ebc-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ebc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="83ebc-128">-Name</span></span>
<span data-ttu-id="83ebc-129">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="83ebc-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="83ebc-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="83ebc-130">-Namespace</span></span>
<span data-ttu-id="83ebc-131">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="83ebc-131">Namespace Name</span></span>

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

### <span data-ttu-id="83ebc-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="83ebc-132">-Queue</span></span>
<span data-ttu-id="83ebc-133">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="83ebc-133">Queue Name</span></span>

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

### <span data-ttu-id="83ebc-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="83ebc-134">-RegenerateKey</span></span>
<span data-ttu-id="83ebc-135">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="83ebc-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83ebc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ebc-136">-ResourceGroupName</span></span>
<span data-ttu-id="83ebc-137">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="83ebc-137">Resource Group Name</span></span>

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

### <span data-ttu-id="83ebc-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="83ebc-138">-Topic</span></span>
<span data-ttu-id="83ebc-139">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="83ebc-139">Topic Name</span></span>

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

### <span data-ttu-id="83ebc-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83ebc-140">-Confirm</span></span>
<span data-ttu-id="83ebc-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83ebc-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83ebc-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ebc-142">-WhatIf</span></span>
<span data-ttu-id="83ebc-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83ebc-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ebc-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83ebc-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83ebc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ebc-145">CommonParameters</span></span>
<span data-ttu-id="83ebc-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ebc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ebc-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ebc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ebc-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83ebc-148">INPUTS</span></span>

### <span data-ttu-id="83ebc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="83ebc-149">System.String</span></span>

## <span data-ttu-id="83ebc-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83ebc-150">OUTPUTS</span></span>

### <span data-ttu-id="83ebc-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="83ebc-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="83ebc-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="83ebc-152">NOTES</span></span>

## <span data-ttu-id="83ebc-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83ebc-153">RELATED LINKS</span></span>
