---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: ac3b98089a3bbb710680269692685a32ef7adc03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918091"
---
# <span data-ttu-id="48a34-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="48a34-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="48a34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48a34-102">SYNOPSIS</span></span>
<span data-ttu-id="48a34-103">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für den Service Bus-Namespace oder die Warteschlange oder das Thema.</span><span class="sxs-lookup"><span data-stu-id="48a34-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="48a34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48a34-104">SYNTAX</span></span>

### <span data-ttu-id="48a34-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="48a34-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48a34-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="48a34-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48a34-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="48a34-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48a34-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48a34-108">DESCRIPTION</span></span>
<span data-ttu-id="48a34-109">Das **Cmdlet New-AzServiceBusKey** generiert neue primäre oder sekundäre Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder die Themen- und Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="48a34-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="48a34-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48a34-110">EXAMPLES</span></span>

### <span data-ttu-id="48a34-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48a34-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="48a34-112">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für den -Namespace.</span><span class="sxs-lookup"><span data-stu-id="48a34-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="48a34-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="48a34-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="48a34-114">Regeneriert die primären oder sekundären Verbindungszeichenfolgen mit dem angegebenen Schlüsselwert für den Namespace.</span><span class="sxs-lookup"><span data-stu-id="48a34-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="48a34-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="48a34-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="48a34-116">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="48a34-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="48a34-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="48a34-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="48a34-118">Regeneriert die primären oder sekundären Verbindungszeichenfolgen mit dem angegebenen Schlüsselwert für die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="48a34-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="48a34-119">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="48a34-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="48a34-120">Regeneriert die primären oder sekundären Verbindungszeichenfolgen für das Thema.</span><span class="sxs-lookup"><span data-stu-id="48a34-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="48a34-121">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="48a34-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="48a34-122">Regeneriert die primären oder sekundären Verbindungszeichenfolgen mit dem angegebenen Schlüsselwert für das Thema.</span><span class="sxs-lookup"><span data-stu-id="48a34-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="48a34-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="48a34-123">PARAMETERS</span></span>

### <span data-ttu-id="48a34-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a34-124">-DefaultProfile</span></span>
<span data-ttu-id="48a34-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48a34-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48a34-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="48a34-126">-KeyValue</span></span>
<span data-ttu-id="48a34-127">Ein base64-codierter 256-Bit-Schlüssel zum Signieren und Überprüfen des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="48a34-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="48a34-128">-Name</span><span class="sxs-lookup"><span data-stu-id="48a34-128">-Name</span></span>
<span data-ttu-id="48a34-129">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="48a34-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="48a34-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="48a34-130">-Namespace</span></span>
<span data-ttu-id="48a34-131">Namespacename</span><span class="sxs-lookup"><span data-stu-id="48a34-131">Namespace Name</span></span>

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

### <span data-ttu-id="48a34-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="48a34-132">-Queue</span></span>
<span data-ttu-id="48a34-133">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="48a34-133">Queue Name</span></span>

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

### <span data-ttu-id="48a34-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="48a34-134">-RegenerateKey</span></span>
<span data-ttu-id="48a34-135">Neu generieren von Schlüsseln – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="48a34-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="48a34-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48a34-136">-ResourceGroupName</span></span>
<span data-ttu-id="48a34-137">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="48a34-137">Resource Group Name</span></span>

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

### <span data-ttu-id="48a34-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="48a34-138">-Topic</span></span>
<span data-ttu-id="48a34-139">Topic Name</span><span class="sxs-lookup"><span data-stu-id="48a34-139">Topic Name</span></span>

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

### <span data-ttu-id="48a34-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48a34-140">-Confirm</span></span>
<span data-ttu-id="48a34-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48a34-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48a34-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48a34-142">-WhatIf</span></span>
<span data-ttu-id="48a34-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48a34-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48a34-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48a34-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48a34-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a34-145">CommonParameters</span></span>
<span data-ttu-id="48a34-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48a34-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a34-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48a34-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a34-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48a34-148">INPUTS</span></span>

### <span data-ttu-id="48a34-149">System.String</span><span class="sxs-lookup"><span data-stu-id="48a34-149">System.String</span></span>

## <span data-ttu-id="48a34-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48a34-150">OUTPUTS</span></span>

### <span data-ttu-id="48a34-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="48a34-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="48a34-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="48a34-152">NOTES</span></span>

## <span data-ttu-id="48a34-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="48a34-153">RELATED LINKS</span></span>
