---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 743928771fdba7ed17fe2643cf9e92ae7c2d9860
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476781"
---
# <span data-ttu-id="356e2-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="356e2-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="356e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="356e2-102">SYNOPSIS</span></span>
<span data-ttu-id="356e2-103">Aktualisiert die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="356e2-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="356e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="356e2-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="356e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="356e2-105">DESCRIPTION</span></span>
<span data-ttu-id="356e2-106">Das Set-AzureRmEventHubConsumerGroup-Cmdlet aktualisiert die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="356e2-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="356e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="356e2-107">EXAMPLES</span></span>

### <span data-ttu-id="356e2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="356e2-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="356e2-109">Legt die Benutzer Metadaten der Verbrauchergruppe \` MyConsumerGroupName \` auf "testen" fest.</span><span class="sxs-lookup"><span data-stu-id="356e2-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="356e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="356e2-110">PARAMETERS</span></span>

### <span data-ttu-id="356e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356e2-111">-DefaultProfile</span></span>
<span data-ttu-id="356e2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="356e2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="356e2-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="356e2-113">-EventHub</span></span>
<span data-ttu-id="356e2-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="356e2-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="356e2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="356e2-115">-Name</span></span>
<span data-ttu-id="356e2-116">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="356e2-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="356e2-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="356e2-117">-Namespace</span></span>
<span data-ttu-id="356e2-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="356e2-118">Namespace Name</span></span>

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

### <span data-ttu-id="356e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="356e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="356e2-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="356e2-120">Resource Group Name</span></span>

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

### <span data-ttu-id="356e2-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="356e2-121">-UserMetadata</span></span>
<span data-ttu-id="356e2-122">Benutzer Metadaten für consumergroup</span><span class="sxs-lookup"><span data-stu-id="356e2-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="356e2-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="356e2-123">-Confirm</span></span>
<span data-ttu-id="356e2-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="356e2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356e2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356e2-125">-WhatIf</span></span>
<span data-ttu-id="356e2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="356e2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="356e2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="356e2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356e2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356e2-128">CommonParameters</span></span>
<span data-ttu-id="356e2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356e2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="356e2-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="356e2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356e2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="356e2-131">INPUTS</span></span>

### <span data-ttu-id="356e2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="356e2-132">System.String</span></span>


## <span data-ttu-id="356e2-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="356e2-133">OUTPUTS</span></span>

### <span data-ttu-id="356e2-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="356e2-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="356e2-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="356e2-135">NOTES</span></span>

## <span data-ttu-id="356e2-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="356e2-136">RELATED LINKS</span></span>
