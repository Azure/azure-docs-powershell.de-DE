---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361120"
---
# <span data-ttu-id="d7e0c-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d7e0c-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d7e0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e0c-103">Ruft alle eventhub-Consumergruppen ab.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="d7e0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7e0c-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7e0c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="d7e0c-106">Ruft alle eventhub-Consumergruppen für die verschiedenen eventHubs ab, die von IotHub verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="d7e0c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="d7e0c-108">Beispiel 1 Ruft alle Eventhub-Consumergruppen für den Telemetrieereignishub ab.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d7e0c-109">Ruft alle eventhub-Consumergruppen für den Telemetrieereignishub für den iothub mit dem Namen "myiothub" ab.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="d7e0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="d7e0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e0c-111">-DefaultProfile</span></span>
<span data-ttu-id="d7e0c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d7e0c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7e0c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d7e0c-113">-Name</span></span>
<span data-ttu-id="d7e0c-114">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="d7e0c-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="d7e0c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e0c-115">-ResourceGroupName</span></span>
<span data-ttu-id="d7e0c-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d7e0c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d7e0c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e0c-117">CommonParameters</span></span>
<span data-ttu-id="d7e0c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e0c-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e0c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e0c-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7e0c-120">INPUTS</span></span>

### <span data-ttu-id="d7e0c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d7e0c-121">System.String</span></span>

## <span data-ttu-id="d7e0c-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7e0c-122">OUTPUTS</span></span>

### <span data-ttu-id="d7e0c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="d7e0c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="d7e0c-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d7e0c-124">NOTES</span></span>

## <span data-ttu-id="d7e0c-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d7e0c-125">RELATED LINKS</span></span>
