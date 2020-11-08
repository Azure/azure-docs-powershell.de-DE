---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003195"
---
# <span data-ttu-id="048c7-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="048c7-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="048c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="048c7-102">SYNOPSIS</span></span>
<span data-ttu-id="048c7-103">Ruft alle eventhub-consumergroups ab.</span><span class="sxs-lookup"><span data-stu-id="048c7-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="048c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="048c7-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="048c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="048c7-105">DESCRIPTION</span></span>
<span data-ttu-id="048c7-106">Ruft alle eventhub-consumergroups für die verschiedenen von IotHub verwendeten EventHubs ab.</span><span class="sxs-lookup"><span data-stu-id="048c7-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="048c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="048c7-107">EXAMPLES</span></span>

### <span data-ttu-id="048c7-108">Beispiel 1 ruft alle eventhub-consumergroups für das Telemetrie-eventhub</span><span class="sxs-lookup"><span data-stu-id="048c7-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="048c7-109">Ruft alle eventhub-consumergroups für die Telemetrie-eventhub für die iothub mit dem Namen myiothub ab.</span><span class="sxs-lookup"><span data-stu-id="048c7-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="048c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="048c7-110">PARAMETERS</span></span>

### <span data-ttu-id="048c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048c7-111">-DefaultProfile</span></span>
<span data-ttu-id="048c7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="048c7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="048c7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="048c7-113">-Name</span></span>
<span data-ttu-id="048c7-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="048c7-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="048c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="048c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="048c7-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="048c7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="048c7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048c7-117">CommonParameters</span></span>
<span data-ttu-id="048c7-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048c7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048c7-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048c7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048c7-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="048c7-120">INPUTS</span></span>

### <span data-ttu-id="048c7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="048c7-121">System.String</span></span>

## <span data-ttu-id="048c7-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="048c7-122">OUTPUTS</span></span>

### <span data-ttu-id="048c7-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="048c7-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="048c7-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="048c7-124">NOTES</span></span>

## <span data-ttu-id="048c7-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="048c7-125">RELATED LINKS</span></span>
