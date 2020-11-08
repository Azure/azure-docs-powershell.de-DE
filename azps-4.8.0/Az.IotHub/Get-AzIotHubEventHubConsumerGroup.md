---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010207"
---
# <span data-ttu-id="96487-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="96487-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="96487-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96487-102">SYNOPSIS</span></span>
<span data-ttu-id="96487-103">Ruft alle eventhub-consumergroups ab.</span><span class="sxs-lookup"><span data-stu-id="96487-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="96487-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96487-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96487-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96487-105">DESCRIPTION</span></span>
<span data-ttu-id="96487-106">Ruft alle eventhub-consumergroups für die verschiedenen von IotHub verwendeten EventHubs ab.</span><span class="sxs-lookup"><span data-stu-id="96487-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="96487-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96487-107">EXAMPLES</span></span>

### <span data-ttu-id="96487-108">Beispiel 1 ruft alle eventhub-consumergroups für das Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="96487-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="96487-109">Ruft alle eventhub-consumergroups für die Telemetrie-eventhub für die iothub mit dem Namen myiothub ab.</span><span class="sxs-lookup"><span data-stu-id="96487-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="96487-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96487-110">PARAMETERS</span></span>

### <span data-ttu-id="96487-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96487-111">-DefaultProfile</span></span>
<span data-ttu-id="96487-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="96487-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96487-113">-Name</span><span class="sxs-lookup"><span data-stu-id="96487-113">-Name</span></span>
<span data-ttu-id="96487-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="96487-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="96487-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96487-115">-ResourceGroupName</span></span>
<span data-ttu-id="96487-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="96487-116">Resource Group Name</span></span>

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

### <span data-ttu-id="96487-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96487-117">CommonParameters</span></span>
<span data-ttu-id="96487-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96487-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96487-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96487-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96487-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96487-120">INPUTS</span></span>

### <span data-ttu-id="96487-121">System. String</span><span class="sxs-lookup"><span data-stu-id="96487-121">System.String</span></span>

## <span data-ttu-id="96487-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96487-122">OUTPUTS</span></span>

### <span data-ttu-id="96487-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="96487-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="96487-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="96487-124">NOTES</span></span>

## <span data-ttu-id="96487-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96487-125">RELATED LINKS</span></span>
