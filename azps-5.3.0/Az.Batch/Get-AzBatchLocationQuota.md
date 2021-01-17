---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471179"
---
# <span data-ttu-id="01339-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="01339-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="01339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01339-102">SYNOPSIS</span></span>
<span data-ttu-id="01339-103">Ruft die Batchdienstkontingente für Ihr Abonnement am angegebenen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="01339-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="01339-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01339-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01339-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01339-105">DESCRIPTION</span></span>
<span data-ttu-id="01339-106">Ruft die Batchdienstkontingente für das angegebene Abonnement am angegebenen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="01339-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="01339-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01339-107">EXAMPLES</span></span>

### <span data-ttu-id="01339-108">Beispiel 1: Erhalten der Batchdienstkontingente für das Abonnement in der Region "USA, Westen"</span><span class="sxs-lookup"><span data-stu-id="01339-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="01339-109">Dieser Befehl ruft die Kontingente für das aktuelle Abonnement in der Region "USA, Westen" ab.</span><span class="sxs-lookup"><span data-stu-id="01339-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="01339-110">Der Rückgabewert gibt an, dass mit diesem Abonnement nur ein Batchkonto in dieser Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="01339-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="01339-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01339-111">PARAMETERS</span></span>

### <span data-ttu-id="01339-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01339-112">-DefaultProfile</span></span>
<span data-ttu-id="01339-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01339-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01339-114">-Location</span><span class="sxs-lookup"><span data-stu-id="01339-114">-Location</span></span>
<span data-ttu-id="01339-115">Gibt die Region an, für die dieses Cmdlet die Kontingente überprüft.</span><span class="sxs-lookup"><span data-stu-id="01339-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="01339-116">Weitere Informationen finden Sie unter "Azure-Regionen ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="01339-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="01339-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01339-117">CommonParameters</span></span>
<span data-ttu-id="01339-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01339-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01339-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01339-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01339-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01339-120">INPUTS</span></span>

### <span data-ttu-id="01339-121">System.String</span><span class="sxs-lookup"><span data-stu-id="01339-121">System.String</span></span>

## <span data-ttu-id="01339-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01339-122">OUTPUTS</span></span>

### <span data-ttu-id="01339-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="01339-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="01339-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01339-124">NOTES</span></span>

## <span data-ttu-id="01339-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01339-125">RELATED LINKS</span></span>
