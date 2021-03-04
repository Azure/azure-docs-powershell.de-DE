---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: f4a722ad01cf354cc49b3441c03ec8aaca2e5e57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936875"
---
# <span data-ttu-id="5e6c0-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5e6c0-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5e6c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6c0-103">Ruft alle Eventhub-Consumergruppen ab.</span><span class="sxs-lookup"><span data-stu-id="5e6c0-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="5e6c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e6c0-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e6c0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e6c0-105">DESCRIPTION</span></span>
<span data-ttu-id="5e6c0-106">Ruft alle Eventhub-Consumergruppen für die verschiedenen eventHubs ab, die von IotHub verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e6c0-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="5e6c0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e6c0-107">EXAMPLES</span></span>

### <span data-ttu-id="5e6c0-108">Beispiel 1 Ruft alle Ereignishub-Consumergruppen für den Telemetrieereignishub ab.</span><span class="sxs-lookup"><span data-stu-id="5e6c0-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5e6c0-109">Ruft alle Ereignishub-Consumergruppen für den Telemetrieereignishub für den Iothub mit dem Namen myiothub ab.</span><span class="sxs-lookup"><span data-stu-id="5e6c0-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="5e6c0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e6c0-110">PARAMETERS</span></span>

### <span data-ttu-id="5e6c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6c0-111">-DefaultProfile</span></span>
<span data-ttu-id="5e6c0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5e6c0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e6c0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5e6c0-113">-Name</span></span>
<span data-ttu-id="5e6c0-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="5e6c0-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="5e6c0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e6c0-115">-ResourceGroupName</span></span>
<span data-ttu-id="5e6c0-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5e6c0-116">Resource Group Name</span></span>

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

### <span data-ttu-id="5e6c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6c0-117">CommonParameters</span></span>
<span data-ttu-id="5e6c0-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e6c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6c0-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e6c0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6c0-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e6c0-120">INPUTS</span></span>

### <span data-ttu-id="5e6c0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5e6c0-121">System.String</span></span>

## <span data-ttu-id="5e6c0-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e6c0-122">OUTPUTS</span></span>

### <span data-ttu-id="5e6c0-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="5e6c0-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="5e6c0-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e6c0-124">NOTES</span></span>

## <span data-ttu-id="5e6c0-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e6c0-125">RELATED LINKS</span></span>
