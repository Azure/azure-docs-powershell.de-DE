---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166667"
---
# <span data-ttu-id="69f7e-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="69f7e-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="69f7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="69f7e-103">Erstellt eine eventhub-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="69f7e-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="69f7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69f7e-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69f7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="69f7e-106">Erstellt eine Consumer-Gruppe in der Eventhub, die dem angegebenen IotHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="69f7e-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="69f7e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="69f7e-108">Beispiel 1: Hinzufügen einer Consumer-Gruppe zum Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="69f7e-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="69f7e-109">Fügt der eventhub für Telemetrie-Ereignisse im iothub mit dem Namen "myiothub" eine neue verbrauchergroup mit dem Namen "myconsumergroup" hinzu.</span><span class="sxs-lookup"><span data-stu-id="69f7e-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="69f7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="69f7e-110">PARAMETERS</span></span>

### <span data-ttu-id="69f7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f7e-111">-DefaultProfile</span></span>
<span data-ttu-id="69f7e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="69f7e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69f7e-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="69f7e-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="69f7e-114">Der Name der EventHub-verbrauchergroup, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="69f7e-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="69f7e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="69f7e-115">-Name</span></span>
<span data-ttu-id="69f7e-116">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="69f7e-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="69f7e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69f7e-117">-ResourceGroupName</span></span>
<span data-ttu-id="69f7e-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69f7e-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="69f7e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69f7e-119">-Confirm</span></span>
<span data-ttu-id="69f7e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69f7e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69f7e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69f7e-121">-WhatIf</span></span>
<span data-ttu-id="69f7e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69f7e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69f7e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69f7e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69f7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f7e-124">CommonParameters</span></span>
<span data-ttu-id="69f7e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f7e-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f7e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f7e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69f7e-127">INPUTS</span></span>

### <span data-ttu-id="69f7e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="69f7e-128">System.String</span></span>

## <span data-ttu-id="69f7e-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69f7e-129">OUTPUTS</span></span>

### <span data-ttu-id="69f7e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="69f7e-130">System.String</span></span>

## <span data-ttu-id="69f7e-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="69f7e-131">NOTES</span></span>

## <span data-ttu-id="69f7e-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69f7e-132">RELATED LINKS</span></span>
