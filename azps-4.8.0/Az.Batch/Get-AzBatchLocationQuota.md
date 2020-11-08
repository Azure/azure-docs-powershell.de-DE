---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010043"
---
# <span data-ttu-id="49645-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="49645-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="49645-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49645-102">SYNOPSIS</span></span>
<span data-ttu-id="49645-103">Ruft die Stapelverarbeitungs Dienst Kontingente für Ihr Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="49645-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="49645-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49645-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49645-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49645-105">DESCRIPTION</span></span>
<span data-ttu-id="49645-106">Ruft die Stapelverarbeitungs Dienst Kontingente für das angegebene Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="49645-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="49645-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49645-107">EXAMPLES</span></span>

### <span data-ttu-id="49645-108">Beispiel 1: Abrufen der Batch Dienst Kontingente für das Abonnement in der Region West Amerika</span><span class="sxs-lookup"><span data-stu-id="49645-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="49645-109">Dieser Befehl ruft die Kontingente für das aktuelle Abonnement in der West US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="49645-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="49645-110">Der Rückgabewert gibt an, dass dieses Abonnement nur ein Stapelverarbeitungs Konto in diesem Bereich erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="49645-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="49645-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="49645-111">PARAMETERS</span></span>

### <span data-ttu-id="49645-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49645-112">-DefaultProfile</span></span>
<span data-ttu-id="49645-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49645-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49645-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="49645-114">-Location</span></span>
<span data-ttu-id="49645-115">Gibt den Bereich an, für den das Cmdlet die Kontingente überprüft.</span><span class="sxs-lookup"><span data-stu-id="49645-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="49645-116">Weitere Informationen finden Sie unter Azure-Bereiche ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="49645-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="49645-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49645-117">CommonParameters</span></span>
<span data-ttu-id="49645-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49645-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49645-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49645-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49645-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49645-120">INPUTS</span></span>

### <span data-ttu-id="49645-121">System. String</span><span class="sxs-lookup"><span data-stu-id="49645-121">System.String</span></span>

## <span data-ttu-id="49645-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49645-122">OUTPUTS</span></span>

### <span data-ttu-id="49645-123">Microsoft.Azure.Commands.Batch. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="49645-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="49645-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="49645-124">NOTES</span></span>

## <span data-ttu-id="49645-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49645-125">RELATED LINKS</span></span>
