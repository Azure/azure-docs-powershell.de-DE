---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477685"
---
# <span data-ttu-id="5b6a9-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="5b6a9-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="5b6a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6a9-103">Entfernt das Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b6a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b6a9-104">SYNTAX</span></span>

### <span data-ttu-id="5b6a9-105">TopicPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b6a9-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b6a9-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b6a9-106">TopicInputObjectSet</span></span>
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b6a9-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b6a9-107">TopicResourceIdSet</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b6a9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b6a9-108">DESCRIPTION</span></span>
<span data-ttu-id="5b6a9-109">Das Cmdlet **Remove-AzureRmServiceBusTopic** entfernt das Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-109">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5b6a9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b6a9-110">EXAMPLES</span></span>

### <span data-ttu-id="5b6a9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b6a9-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="5b6a9-112">Entfernt das Thema `SB-Topic_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5b6a9-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="5b6a9-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="5b6a9-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="5b6a9-114">Beispiel 2,2-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="5b6a9-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### <span data-ttu-id="5b6a9-115">Beispiel 3,1-Sourcecode mit Variable:</span><span class="sxs-lookup"><span data-stu-id="5b6a9-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="5b6a9-116">Beispiel 3,2-resourcecode mit Zeichenfolgenwert</span><span class="sxs-lookup"><span data-stu-id="5b6a9-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="5b6a9-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b6a9-117">PARAMETERS</span></span>

### <span data-ttu-id="5b6a9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b6a9-118">-AsJob</span></span>
<span data-ttu-id="5b6a9-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5b6a9-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6a9-120">-DefaultProfile</span></span>
<span data-ttu-id="5b6a9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b6a9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5b6a9-122">-InputObject</span></span>
<span data-ttu-id="5b6a9-123">Service Bus Topic-Objekt</span><span class="sxs-lookup"><span data-stu-id="5b6a9-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6a9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5b6a9-124">-Name</span></span>
<span data-ttu-id="5b6a9-125">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="5b6a9-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6a9-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5b6a9-126">-Namespace</span></span>
<span data-ttu-id="5b6a9-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5b6a9-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6a9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b6a9-128">-PassThru</span></span>
<span data-ttu-id="5b6a9-129">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-129">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6a9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b6a9-130">-ResourceGroupName</span></span>
<span data-ttu-id="5b6a9-131">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5b6a9-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6a9-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5b6a9-132">-ResourceId</span></span>
<span data-ttu-id="5b6a9-133">Service Bus Topic-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5b6a9-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6a9-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b6a9-134">-Confirm</span></span>
<span data-ttu-id="5b6a9-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b6a9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b6a9-136">-WhatIf</span></span>
<span data-ttu-id="5b6a9-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b6a9-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b6a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6a9-139">CommonParameters</span></span>
<span data-ttu-id="5b6a9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b6a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b6a9-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b6a9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6a9-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b6a9-142">INPUTS</span></span>

### <span data-ttu-id="5b6a9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5b6a9-143">System.String</span></span>

### <span data-ttu-id="5b6a9-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="5b6a9-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="5b6a9-145">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b6a9-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5b6a9-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b6a9-146">OUTPUTS</span></span>

### <span data-ttu-id="5b6a9-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b6a9-147">System.Boolean</span></span>

## <span data-ttu-id="5b6a9-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b6a9-148">NOTES</span></span>

## <span data-ttu-id="5b6a9-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b6a9-149">RELATED LINKS</span></span>
