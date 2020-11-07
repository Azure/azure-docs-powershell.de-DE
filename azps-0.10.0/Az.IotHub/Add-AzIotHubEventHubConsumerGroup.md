---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 2592284be483793ea246d30e95a4c9065fdd6e3c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843992"
---
# <span data-ttu-id="aa494-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="aa494-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="aa494-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa494-102">SYNOPSIS</span></span>
<span data-ttu-id="aa494-103">Erstellt eine eventhub-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="aa494-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="aa494-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa494-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa494-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa494-105">DESCRIPTION</span></span>
<span data-ttu-id="aa494-106">Erstellt eine Consumer-Gruppe in der Eventhub, die dem angegebenen IotHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aa494-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="aa494-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa494-107">EXAMPLES</span></span>

### <span data-ttu-id="aa494-108">Beispiel 1: Hinzufügen einer Consumer-Gruppe zum Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="aa494-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="aa494-109">Fügt der eventhub für Telemetrie-Ereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="aa494-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="aa494-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa494-110">PARAMETERS</span></span>

### <span data-ttu-id="aa494-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa494-111">-DefaultProfile</span></span>
<span data-ttu-id="aa494-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="aa494-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa494-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="aa494-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="aa494-114">Der Name der EventHub-verbrauchergroup, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="aa494-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="aa494-115">-Name</span><span class="sxs-lookup"><span data-stu-id="aa494-115">-Name</span></span>
<span data-ttu-id="aa494-116">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="aa494-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aa494-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa494-117">-ResourceGroupName</span></span>
<span data-ttu-id="aa494-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa494-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="aa494-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa494-119">-Confirm</span></span>
<span data-ttu-id="aa494-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa494-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa494-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa494-121">-WhatIf</span></span>
<span data-ttu-id="aa494-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa494-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa494-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa494-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa494-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa494-124">CommonParameters</span></span>
<span data-ttu-id="aa494-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa494-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa494-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa494-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa494-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa494-127">INPUTS</span></span>

### <span data-ttu-id="aa494-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aa494-128">System.String</span></span>

## <span data-ttu-id="aa494-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa494-129">OUTPUTS</span></span>

### <span data-ttu-id="aa494-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aa494-130">System.String</span></span>

## <span data-ttu-id="aa494-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa494-131">NOTES</span></span>

## <span data-ttu-id="aa494-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa494-132">RELATED LINKS</span></span>
