---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004338"
---
# <span data-ttu-id="cee0d-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="cee0d-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="cee0d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cee0d-102">SYNOPSIS</span></span>
<span data-ttu-id="cee0d-103">Ruft die Stapelverarbeitungs Dienst Kontingente für Ihr Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="cee0d-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="cee0d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cee0d-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cee0d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cee0d-105">DESCRIPTION</span></span>
<span data-ttu-id="cee0d-106">Ruft die Stapelverarbeitungs Dienst Kontingente für das angegebene Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="cee0d-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="cee0d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cee0d-107">EXAMPLES</span></span>

### <span data-ttu-id="cee0d-108">Beispiel 1: Abrufen der Batch Dienst Kontingente für das Abonnement in der Region West Amerika</span><span class="sxs-lookup"><span data-stu-id="cee0d-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="cee0d-109">Dieser Befehl ruft die Kontingente für das aktuelle Abonnement in der West US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="cee0d-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="cee0d-110">Der Rückgabewert gibt an, dass dieses Abonnement nur ein Stapelverarbeitungs Konto in diesem Bereich erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="cee0d-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="cee0d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cee0d-111">PARAMETERS</span></span>

### <span data-ttu-id="cee0d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee0d-112">-DefaultProfile</span></span>
<span data-ttu-id="cee0d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cee0d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee0d-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="cee0d-114">-Location</span></span>
<span data-ttu-id="cee0d-115">Gibt den Bereich an, für den das Cmdlet die Kontingente überprüft.</span><span class="sxs-lookup"><span data-stu-id="cee0d-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="cee0d-116">Weitere Informationen finden Sie unter Azure-Bereiche ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="cee0d-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="cee0d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee0d-117">CommonParameters</span></span>
<span data-ttu-id="cee0d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cee0d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee0d-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cee0d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee0d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cee0d-120">INPUTS</span></span>

### <span data-ttu-id="cee0d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cee0d-121">System.String</span></span>

## <span data-ttu-id="cee0d-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cee0d-122">OUTPUTS</span></span>

### <span data-ttu-id="cee0d-123">Microsoft.Azure.Commands.Batch. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="cee0d-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="cee0d-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="cee0d-124">NOTES</span></span>

## <span data-ttu-id="cee0d-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cee0d-125">RELATED LINKS</span></span>
