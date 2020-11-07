---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 19a3098eff598c223014b65381e524d063f7d425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663572"
---
# <span data-ttu-id="89232-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="89232-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="89232-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89232-102">SYNOPSIS</span></span>
<span data-ttu-id="89232-103">Erstellt eine eventhub-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="89232-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89232-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89232-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89232-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89232-105">DESCRIPTION</span></span>
<span data-ttu-id="89232-106">Erstellt eine Consumer-Gruppe in der Eventhub, die dem angegebenen IotHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="89232-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="89232-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89232-107">EXAMPLES</span></span>

### <span data-ttu-id="89232-108">Beispiel 1: Hinzufügen einer Consumer-Gruppe zum Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="89232-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="89232-109">Fügt der eventhub für Telemetrie-Ereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="89232-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="89232-110">Beispiel 2: Hinzufügen einer Consumer-Gruppe zum Vorgangs Überwachungs eventhub</span><span class="sxs-lookup"><span data-stu-id="89232-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="89232-111">Fügt der eventhub für Operations-Überwachungsereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="89232-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="89232-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="89232-112">PARAMETERS</span></span>

### <span data-ttu-id="89232-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="89232-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="89232-114">Der Name der EventHub-verbrauchergroup, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="89232-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89232-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="89232-115">-EventHubEndpointName</span></span>
<span data-ttu-id="89232-116">Der Name des EventHub-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="89232-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="89232-117">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="89232-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89232-118">-Name</span><span class="sxs-lookup"><span data-stu-id="89232-118">-Name</span></span>
<span data-ttu-id="89232-119">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="89232-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89232-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89232-120">-ResourceGroupName</span></span>
<span data-ttu-id="89232-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89232-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="89232-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="89232-122">-Confirm</span></span>
<span data-ttu-id="89232-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89232-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89232-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89232-124">-WhatIf</span></span>
<span data-ttu-id="89232-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89232-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89232-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89232-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89232-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89232-127">-DefaultProfile</span></span>
<span data-ttu-id="89232-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89232-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89232-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89232-129">CommonParameters</span></span>
<span data-ttu-id="89232-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89232-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89232-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89232-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89232-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89232-132">INPUTS</span></span>

### <span data-ttu-id="89232-133">System. String</span><span class="sxs-lookup"><span data-stu-id="89232-133">System.String</span></span>

## <span data-ttu-id="89232-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89232-134">OUTPUTS</span></span>

### <span data-ttu-id="89232-135">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="89232-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="89232-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="89232-136">NOTES</span></span>

## <span data-ttu-id="89232-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89232-137">RELATED LINKS</span></span>

