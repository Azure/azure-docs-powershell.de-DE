---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: 85dd98ac4eeb262564dcca58ec57f1f5df80842a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939960"
---
# <span data-ttu-id="aab41-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="aab41-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="aab41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab41-102">SYNOPSIS</span></span>
<span data-ttu-id="aab41-103">Liste unterstützter ServiceBus-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="aab41-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="aab41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aab41-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab41-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aab41-105">DESCRIPTION</span></span>
<span data-ttu-id="aab41-106">Im **Cmdlet Get-AzServiceBusOperation** werden die vom ServiceBus unterstützten Vorgänge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="aab41-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="aab41-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aab41-107">EXAMPLES</span></span>

### <span data-ttu-id="aab41-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aab41-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="aab41-109">Listet unterstützte ServiceBus-Vorgänge auf</span><span class="sxs-lookup"><span data-stu-id="aab41-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="aab41-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aab41-110">PARAMETERS</span></span>

### <span data-ttu-id="aab41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab41-111">-DefaultProfile</span></span>
<span data-ttu-id="aab41-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aab41-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab41-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab41-113">CommonParameters</span></span>
<span data-ttu-id="aab41-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab41-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab41-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab41-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab41-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aab41-116">INPUTS</span></span>

### <span data-ttu-id="aab41-117">Keine</span><span class="sxs-lookup"><span data-stu-id="aab41-117">None</span></span>

## <span data-ttu-id="aab41-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aab41-118">OUTPUTS</span></span>

### <span data-ttu-id="aab41-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="aab41-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="aab41-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aab41-120">NOTES</span></span>

## <span data-ttu-id="aab41-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aab41-121">RELATED LINKS</span></span>
