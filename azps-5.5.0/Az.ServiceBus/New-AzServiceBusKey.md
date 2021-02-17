---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156348"
---
# <span data-ttu-id="2d115-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="2d115-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="2d115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d115-102">SYNOPSIS</span></span>
<span data-ttu-id="2d115-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für den Namespace oder die Warteschlange oder das Thema des Service Bus erneut.</span><span class="sxs-lookup"><span data-stu-id="2d115-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="2d115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d115-104">SYNTAX</span></span>

### <span data-ttu-id="2d115-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d115-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d115-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d115-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d115-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d115-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d115-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d115-108">DESCRIPTION</span></span>
<span data-ttu-id="2d115-109">Das **Cmdlet "New-AzServiceBusKey"** generiert neue primäre oder sekundäre Verbindungszeichenfolgen für den angegebenen Namespace oder die angegebene Warteschlange oder das Thema und die Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="2d115-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="2d115-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d115-110">EXAMPLES</span></span>

### <span data-ttu-id="2d115-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d115-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="2d115-112">Generiert die primären oder sekundären Verbindungszeichenfolgen für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="2d115-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="2d115-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2d115-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="2d115-114">Generiert die primären oder sekundären Verbindungszeichenfolgen erneut mit dem bereitgestellten Schlüsselwert für den Namespace.</span><span class="sxs-lookup"><span data-stu-id="2d115-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="2d115-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2d115-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="2d115-116">Generiert die primären oder sekundären Verbindungszeichenfolgen für die Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="2d115-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="2d115-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2d115-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="2d115-118">Generiert die primären oder sekundären Verbindungszeichenfolgen erneut mit dem bereitgestellten Schlüsselwert für die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2d115-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="2d115-119">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="2d115-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="2d115-120">Generiert die primären oder sekundären Verbindungszeichenfolgen für das Thema erneut.</span><span class="sxs-lookup"><span data-stu-id="2d115-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="2d115-121">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="2d115-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="2d115-122">Generiert die primären oder sekundären Verbindungszeichenfolgen erneut mit dem angegebenen Schlüsselwert für das Thema.</span><span class="sxs-lookup"><span data-stu-id="2d115-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="2d115-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d115-123">PARAMETERS</span></span>

### <span data-ttu-id="2d115-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d115-124">-DefaultProfile</span></span>
<span data-ttu-id="2d115-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d115-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d115-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="2d115-126">-KeyValue</span></span>
<span data-ttu-id="2d115-127">Ein base64-codierter 256-Bit-Schlüssel zum Signieren und Überprüfen des SAS-Tokens.</span><span class="sxs-lookup"><span data-stu-id="2d115-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="2d115-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2d115-128">-Name</span></span>
<span data-ttu-id="2d115-129">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="2d115-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2d115-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2d115-130">-Namespace</span></span>
<span data-ttu-id="2d115-131">Namespacename</span><span class="sxs-lookup"><span data-stu-id="2d115-131">Namespace Name</span></span>

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

### <span data-ttu-id="2d115-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="2d115-132">-Queue</span></span>
<span data-ttu-id="2d115-133">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="2d115-133">Queue Name</span></span>

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

### <span data-ttu-id="2d115-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="2d115-134">-RegenerateKey</span></span>
<span data-ttu-id="2d115-135">Generieren Sie schlüssel erneut – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="2d115-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="2d115-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d115-136">-ResourceGroupName</span></span>
<span data-ttu-id="2d115-137">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2d115-137">Resource Group Name</span></span>

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

### <span data-ttu-id="2d115-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="2d115-138">-Topic</span></span>
<span data-ttu-id="2d115-139">Themaname</span><span class="sxs-lookup"><span data-stu-id="2d115-139">Topic Name</span></span>

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

### <span data-ttu-id="2d115-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d115-140">-Confirm</span></span>
<span data-ttu-id="2d115-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d115-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d115-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2d115-142">-WhatIf</span></span>
<span data-ttu-id="2d115-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d115-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d115-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d115-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d115-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d115-145">CommonParameters</span></span>
<span data-ttu-id="2d115-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d115-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d115-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d115-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d115-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d115-148">INPUTS</span></span>

### <span data-ttu-id="2d115-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2d115-149">System.String</span></span>

## <span data-ttu-id="2d115-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d115-150">OUTPUTS</span></span>

### <span data-ttu-id="2d115-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2d115-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="2d115-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d115-152">NOTES</span></span>

## <span data-ttu-id="2d115-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d115-153">RELATED LINKS</span></span>
