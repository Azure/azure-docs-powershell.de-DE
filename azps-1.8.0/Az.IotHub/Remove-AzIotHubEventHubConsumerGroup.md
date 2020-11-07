---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59a180d422a27ca9d2c3e1e4932d843ba7c70093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819724"
---
# <span data-ttu-id="94c16-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="94c16-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="94c16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94c16-102">SYNOPSIS</span></span>
<span data-ttu-id="94c16-103">Löscht eine eventhub-verbrauchergroup.</span><span class="sxs-lookup"><span data-stu-id="94c16-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="94c16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94c16-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94c16-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94c16-105">DESCRIPTION</span></span>
<span data-ttu-id="94c16-106">Löscht eine eventhub-verbrauchergroup.</span><span class="sxs-lookup"><span data-stu-id="94c16-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="94c16-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94c16-107">EXAMPLES</span></span>

### <span data-ttu-id="94c16-108">Beispiel 1 Entfernen von eventhub consumergroup aus der Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="94c16-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="94c16-109">Entfernt die verbrauchergroup mit dem Namen "myconsumergroup" aus dem IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="94c16-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="94c16-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="94c16-110">PARAMETERS</span></span>

### <span data-ttu-id="94c16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c16-111">-DefaultProfile</span></span>
<span data-ttu-id="94c16-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="94c16-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94c16-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="94c16-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="94c16-114">Name der EventHub-consumergruppe</span><span class="sxs-lookup"><span data-stu-id="94c16-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c16-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="94c16-115">-EventHubEndpointName</span></span>
<span data-ttu-id="94c16-116">EventHub-Endpunkt Name</span><span class="sxs-lookup"><span data-stu-id="94c16-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="94c16-117">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="94c16-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="94c16-118">-Name</span><span class="sxs-lookup"><span data-stu-id="94c16-118">-Name</span></span>
<span data-ttu-id="94c16-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="94c16-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="94c16-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c16-120">-ResourceGroupName</span></span>
<span data-ttu-id="94c16-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="94c16-121">Resource Group Name</span></span>

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

### <span data-ttu-id="94c16-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94c16-122">-Confirm</span></span>
<span data-ttu-id="94c16-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94c16-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c16-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c16-124">-WhatIf</span></span>
<span data-ttu-id="94c16-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94c16-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c16-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94c16-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c16-127">CommonParameters</span></span>
<span data-ttu-id="94c16-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c16-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c16-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c16-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94c16-130">INPUTS</span></span>

### <span data-ttu-id="94c16-131">System. String</span><span class="sxs-lookup"><span data-stu-id="94c16-131">System.String</span></span>

## <span data-ttu-id="94c16-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94c16-132">OUTPUTS</span></span>

### <span data-ttu-id="94c16-133">System. String</span><span class="sxs-lookup"><span data-stu-id="94c16-133">System.String</span></span>

## <span data-ttu-id="94c16-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="94c16-134">NOTES</span></span>

## <span data-ttu-id="94c16-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94c16-135">RELATED LINKS</span></span>
