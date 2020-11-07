---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: 46a3551e309504d9938359a0fed4d37860fcb524
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824788"
---
# <span data-ttu-id="df2fa-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="df2fa-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="df2fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="df2fa-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für den ServiceBus-Namespace oder die Warteschlange oder das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="df2fa-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="df2fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df2fa-104">SYNTAX</span></span>

### <span data-ttu-id="df2fa-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="df2fa-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df2fa-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="df2fa-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df2fa-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="df2fa-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df2fa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df2fa-108">DESCRIPTION</span></span>
<span data-ttu-id="df2fa-109">Mit dem Cmdlet **New-AzServiceBusKey** werden neue primäre oder sekundäre Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema und die Autorisierungsregel generiert.</span><span class="sxs-lookup"><span data-stu-id="df2fa-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="df2fa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df2fa-110">EXAMPLES</span></span>

### <span data-ttu-id="df2fa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df2fa-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="df2fa-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="df2fa-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="df2fa-113">Beispiel 1,1</span><span class="sxs-lookup"><span data-stu-id="df2fa-113">Example 1.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="df2fa-114">Generiert die primären oder sekundären Verbindungszeichenfolgen mit dem bereitgestellten Schlüsselwert für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="df2fa-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="df2fa-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="df2fa-115">Example 2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="df2fa-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für die Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="df2fa-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="df2fa-117">Beispiel 2,2</span><span class="sxs-lookup"><span data-stu-id="df2fa-117">Example 2.2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="df2fa-118">Generiert die primären oder sekundären Verbindungszeichenfolgen mit dem bereitgestellten Schlüsselwert für die Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="df2fa-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="df2fa-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="df2fa-119">Example 3</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="df2fa-120">Generiert die primären oder sekundären Verbindungszeichenfolgen für das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="df2fa-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="df2fa-121">Beispiel 3,1</span><span class="sxs-lookup"><span data-stu-id="df2fa-121">Example 3.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="df2fa-122">Generiert die primären oder sekundären Verbindungszeichenfolgen mit dem bereitgestellten Schlüsselwert für das Thema neu.</span><span class="sxs-lookup"><span data-stu-id="df2fa-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="df2fa-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="df2fa-123">PARAMETERS</span></span>

### <span data-ttu-id="df2fa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df2fa-124">-DefaultProfile</span></span>
<span data-ttu-id="df2fa-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df2fa-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df2fa-126">-Keywert</span><span class="sxs-lookup"><span data-stu-id="df2fa-126">-KeyValue</span></span>
<span data-ttu-id="df2fa-127">Ein Base64-codierter 256-Bit-Schlüssel zum Signieren und Validieren des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="df2fa-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="df2fa-128">-Name</span><span class="sxs-lookup"><span data-stu-id="df2fa-128">-Name</span></span>
<span data-ttu-id="df2fa-129">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="df2fa-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="df2fa-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df2fa-130">-Namespace</span></span>
<span data-ttu-id="df2fa-131">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="df2fa-131">Namespace Name</span></span>

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

### <span data-ttu-id="df2fa-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="df2fa-132">-Queue</span></span>
<span data-ttu-id="df2fa-133">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="df2fa-133">Queue Name</span></span>

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

### <span data-ttu-id="df2fa-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="df2fa-134">-RegenerateKey</span></span>
<span data-ttu-id="df2fa-135">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="df2fa-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="df2fa-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df2fa-136">-ResourceGroupName</span></span>
<span data-ttu-id="df2fa-137">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="df2fa-137">Resource Group Name</span></span>

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

### <span data-ttu-id="df2fa-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="df2fa-138">-Topic</span></span>
<span data-ttu-id="df2fa-139">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="df2fa-139">Topic Name</span></span>

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

### <span data-ttu-id="df2fa-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df2fa-140">-Confirm</span></span>
<span data-ttu-id="df2fa-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df2fa-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df2fa-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df2fa-142">-WhatIf</span></span>
<span data-ttu-id="df2fa-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df2fa-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df2fa-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df2fa-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df2fa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df2fa-145">CommonParameters</span></span>
<span data-ttu-id="df2fa-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df2fa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df2fa-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df2fa-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df2fa-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df2fa-148">INPUTS</span></span>

### <span data-ttu-id="df2fa-149">System. String</span><span class="sxs-lookup"><span data-stu-id="df2fa-149">System.String</span></span>

## <span data-ttu-id="df2fa-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df2fa-150">OUTPUTS</span></span>

### <span data-ttu-id="df2fa-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="df2fa-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="df2fa-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="df2fa-152">NOTES</span></span>

## <span data-ttu-id="df2fa-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df2fa-153">RELATED LINKS</span></span>
