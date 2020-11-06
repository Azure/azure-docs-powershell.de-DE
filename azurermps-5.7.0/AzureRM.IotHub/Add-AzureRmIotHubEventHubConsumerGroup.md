---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 192a20ee3d49bd79dff833a05ffd3ff98bcc30ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503765"
---
# <span data-ttu-id="4d353-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4d353-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="4d353-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d353-102">SYNOPSIS</span></span>
<span data-ttu-id="4d353-103">Erstellt eine eventhub-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="4d353-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d353-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d353-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d353-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d353-105">DESCRIPTION</span></span>
<span data-ttu-id="4d353-106">Erstellt eine Consumer-Gruppe in der Eventhub, die dem angegebenen IotHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4d353-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="4d353-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d353-107">EXAMPLES</span></span>

### <span data-ttu-id="4d353-108">Beispiel 1: Hinzufügen einer Consumer-Gruppe zum Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="4d353-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="4d353-109">Fügt der eventhub für Telemetrie-Ereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d353-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="4d353-110">Beispiel 2: Hinzufügen einer Consumer-Gruppe zum Vorgangs Überwachungs eventhub</span><span class="sxs-lookup"><span data-stu-id="4d353-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="4d353-111">Fügt der eventhub für Operations-Überwachungsereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="4d353-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="4d353-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d353-112">PARAMETERS</span></span>

### <span data-ttu-id="4d353-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d353-113">-DefaultProfile</span></span>
<span data-ttu-id="4d353-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4d353-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d353-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="4d353-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="4d353-116">Der Name der EventHub-verbrauchergroup, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="4d353-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d353-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="4d353-117">-EventHubEndpointName</span></span>
<span data-ttu-id="4d353-118">Der Name des EventHub-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="4d353-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="4d353-119">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="4d353-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d353-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d353-120">-Name</span></span>
<span data-ttu-id="4d353-121">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="4d353-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4d353-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d353-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d353-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d353-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="4d353-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d353-124">-Confirm</span></span>
<span data-ttu-id="4d353-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d353-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d353-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d353-126">-WhatIf</span></span>
<span data-ttu-id="4d353-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d353-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d353-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d353-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d353-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d353-129">CommonParameters</span></span>
<span data-ttu-id="4d353-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d353-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d353-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d353-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d353-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d353-132">INPUTS</span></span>

### <span data-ttu-id="4d353-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4d353-133">System.String</span></span>

## <span data-ttu-id="4d353-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d353-134">OUTPUTS</span></span>

### <span data-ttu-id="4d353-135">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4d353-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4d353-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d353-136">NOTES</span></span>

## <span data-ttu-id="4d353-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d353-137">RELATED LINKS</span></span>

