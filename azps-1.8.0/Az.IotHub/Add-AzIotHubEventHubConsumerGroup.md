---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: c4378b156d17759c180ee3bf966bc20d06d00b41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819812"
---
# <span data-ttu-id="99042-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="99042-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="99042-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99042-102">SYNOPSIS</span></span>
<span data-ttu-id="99042-103">Erstellt eine eventhub-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="99042-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="99042-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99042-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99042-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99042-105">DESCRIPTION</span></span>
<span data-ttu-id="99042-106">Erstellt eine Consumer-Gruppe in der Eventhub, die dem angegebenen IotHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="99042-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="99042-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99042-107">EXAMPLES</span></span>

### <span data-ttu-id="99042-108">Beispiel 1: Hinzufügen einer Consumer-Gruppe zum Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="99042-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="99042-109">Fügt der eventhub für Telemetrie-Ereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="99042-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="99042-110">Beispiel 2: Hinzufügen einer Consumer-Gruppe zum Vorgangs Überwachungs eventhub</span><span class="sxs-lookup"><span data-stu-id="99042-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="99042-111">Fügt der eventhub für Operations-Überwachungsereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="99042-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="99042-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="99042-112">PARAMETERS</span></span>

### <span data-ttu-id="99042-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99042-113">-DefaultProfile</span></span>
<span data-ttu-id="99042-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="99042-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99042-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="99042-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="99042-116">Der Name der EventHub-verbrauchergroup, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="99042-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="99042-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="99042-117">-EventHubEndpointName</span></span>
<span data-ttu-id="99042-118">Der Name des EventHub-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="99042-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="99042-119">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="99042-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99042-120">-Name</span><span class="sxs-lookup"><span data-stu-id="99042-120">-Name</span></span>
<span data-ttu-id="99042-121">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="99042-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="99042-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99042-122">-ResourceGroupName</span></span>
<span data-ttu-id="99042-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99042-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="99042-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99042-124">-Confirm</span></span>
<span data-ttu-id="99042-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99042-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99042-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99042-126">-WhatIf</span></span>
<span data-ttu-id="99042-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99042-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99042-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99042-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99042-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99042-129">CommonParameters</span></span>
<span data-ttu-id="99042-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99042-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99042-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99042-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99042-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99042-132">INPUTS</span></span>

### <span data-ttu-id="99042-133">System. String</span><span class="sxs-lookup"><span data-stu-id="99042-133">System.String</span></span>

## <span data-ttu-id="99042-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99042-134">OUTPUTS</span></span>

### <span data-ttu-id="99042-135">System. String</span><span class="sxs-lookup"><span data-stu-id="99042-135">System.String</span></span>

## <span data-ttu-id="99042-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="99042-136">NOTES</span></span>

## <span data-ttu-id="99042-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99042-137">RELATED LINKS</span></span>
