---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504130"
---
# <span data-ttu-id="2bb3a-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2bb3a-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="2bb3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb3a-103">Löscht eine eventhub-verbrauchergroup.</span><span class="sxs-lookup"><span data-stu-id="2bb3a-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bb3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bb3a-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bb3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bb3a-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb3a-106">Löscht eine eventhub-verbrauchergroup.</span><span class="sxs-lookup"><span data-stu-id="2bb3a-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="2bb3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bb3a-107">EXAMPLES</span></span>

### <span data-ttu-id="2bb3a-108">Beispiel 1 Entfernen von eventhub consumergroup aus der Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="2bb3a-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="2bb3a-109">Entfernt die verbrauchergroup mit dem Namen "myconsumergroup" aus dem IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="2bb3a-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2bb3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bb3a-110">PARAMETERS</span></span>

### <span data-ttu-id="2bb3a-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb3a-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="2bb3a-112">Name der EventHub-consumergruppe</span><span class="sxs-lookup"><span data-stu-id="2bb3a-112">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="2bb3a-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="2bb3a-113">-EventHubEndpointName</span></span>
<span data-ttu-id="2bb3a-114">EventHub-Endpunkt Name</span><span class="sxs-lookup"><span data-stu-id="2bb3a-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="2bb3a-115">Mögliche Werte: Ereignisse, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="2bb3a-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="2bb3a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2bb3a-116">-Name</span></span>
<span data-ttu-id="2bb3a-117">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="2bb3a-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="2bb3a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb3a-118">-ResourceGroupName</span></span>
<span data-ttu-id="2bb3a-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2bb3a-119">Resource Group Name</span></span>

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

### <span data-ttu-id="2bb3a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bb3a-120">-Confirm</span></span>
<span data-ttu-id="2bb3a-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bb3a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bb3a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bb3a-122">-WhatIf</span></span>
<span data-ttu-id="2bb3a-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb3a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bb3a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bb3a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bb3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb3a-125">-DefaultProfile</span></span>
<span data-ttu-id="2bb3a-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bb3a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bb3a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb3a-127">CommonParameters</span></span>
<span data-ttu-id="2bb3a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb3a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb3a-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb3a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb3a-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bb3a-130">INPUTS</span></span>

### <span data-ttu-id="2bb3a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2bb3a-131">System.String</span></span>

## <span data-ttu-id="2bb3a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bb3a-132">OUTPUTS</span></span>

### <span data-ttu-id="2bb3a-133">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2bb3a-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2bb3a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bb3a-134">NOTES</span></span>

## <span data-ttu-id="2bb3a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bb3a-135">RELATED LINKS</span></span>

