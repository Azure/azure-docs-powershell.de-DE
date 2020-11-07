---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664978"
---
# <span data-ttu-id="e0958-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="e0958-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="e0958-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0958-102">SYNOPSIS</span></span>
<span data-ttu-id="e0958-103">Generiert die primären oder sekundären Verbindungszeichenfolgen für die ServiceBus-Warteschlange erneut.</span><span class="sxs-lookup"><span data-stu-id="e0958-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0958-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0958-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0958-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0958-105">DESCRIPTION</span></span>
<span data-ttu-id="e0958-106">Das Cmdlet **New-AzureRmServiceBusQueueKey** generiert die primären oder sekundären Verbindungszeichenfolgen für die angegebene ServiceBus-Warteschlange und Autorisierungsregel erneut.</span><span class="sxs-lookup"><span data-stu-id="e0958-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="e0958-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0958-107">EXAMPLES</span></span>

### <span data-ttu-id="e0958-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0958-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="e0958-109">Generiert die primäre Verbindungszeichenfolge für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="e0958-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="e0958-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e0958-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="e0958-111">Generiert die sekundäre Verbindungszeichenfolge für den Namespace erneut.</span><span class="sxs-lookup"><span data-stu-id="e0958-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="e0958-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0958-112">PARAMETERS</span></span>

### <span data-ttu-id="e0958-113">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="e0958-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="e0958-114">Der Name der Autorisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="e0958-114">The authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-115">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="e0958-115">-NamespaceName</span></span>
<span data-ttu-id="e0958-116">Der Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="e0958-116">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-117">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="e0958-117">-QueueName</span></span>
<span data-ttu-id="e0958-118">Der Name der ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e0958-118">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="e0958-119">-RegenerateKeys</span></span>
<span data-ttu-id="e0958-120">Gibt an, ob die primären oder sekundären Schlüssel neu generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e0958-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0958-121">-ResourceGroup</span></span>
<span data-ttu-id="e0958-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0958-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0958-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0958-123">-Confirm</span></span>
<span data-ttu-id="e0958-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0958-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0958-125">-WhatIf</span></span>
<span data-ttu-id="e0958-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0958-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0958-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0958-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0958-128">CommonParameters</span></span>
<span data-ttu-id="e0958-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0958-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0958-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0958-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0958-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0958-131">INPUTS</span></span>

### <span data-ttu-id="e0958-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0958-132">-ResourceGroup</span></span>
 <span data-ttu-id="e0958-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e0958-133">System.String</span></span>
 

### <span data-ttu-id="e0958-134">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="e0958-134">-NamespaceName</span></span>
 <span data-ttu-id="e0958-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e0958-135">System.String</span></span>
 

### <span data-ttu-id="e0958-136">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="e0958-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e0958-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e0958-137">System.String</span></span>
 

### <span data-ttu-id="e0958-138">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="e0958-138">-QueueName</span></span>
 <span data-ttu-id="e0958-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e0958-139">System.String</span></span>
 

### <span data-ttu-id="e0958-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="e0958-140">-RegenerateKeys</span></span>
 <span data-ttu-id="e0958-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e0958-141">System.String</span></span>

## <span data-ttu-id="e0958-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0958-142">OUTPUTS</span></span>

### <span data-ttu-id="e0958-143">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="e0958-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="e0958-144">PrimaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: Endpunkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Wert}; EntityPath = SB-Queue_exa mpl1 Primary: {Primärwert} SecondaryKey: {SecondaryKey Wert} keyName: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="e0958-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="e0958-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0958-145">NOTES</span></span>

## <span data-ttu-id="e0958-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0958-146">RELATED LINKS</span></span>

