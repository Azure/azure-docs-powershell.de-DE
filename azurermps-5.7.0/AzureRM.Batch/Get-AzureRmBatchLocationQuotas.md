---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchlocationquotas
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 1390efccef67e6bfb626e9b31d1a58c72c9fb36e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663783"
---
# <span data-ttu-id="03be3-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="03be3-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="03be3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03be3-102">SYNOPSIS</span></span>
<span data-ttu-id="03be3-103">Ruft die Stapelverarbeitungs Dienst Kontingente für Ihr Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="03be3-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03be3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03be3-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03be3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03be3-105">DESCRIPTION</span></span>
<span data-ttu-id="03be3-106">Ruft die Stapelverarbeitungs Dienst Kontingente für das angegebene Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="03be3-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="03be3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03be3-107">EXAMPLES</span></span>

### <span data-ttu-id="03be3-108">Beispiel 1: Abrufen der Batch Dienst Kontingente für das Abonnement in der Region West Amerika</span><span class="sxs-lookup"><span data-stu-id="03be3-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="03be3-109">Dieser Befehl ruft die Kontingente für das aktuelle Abonnement in der West US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="03be3-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="03be3-110">Der Rückgabewert gibt an, dass dieses Abonnement nur ein Stapelverarbeitungs Konto in diesem Bereich erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="03be3-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="03be3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="03be3-111">PARAMETERS</span></span>

### <span data-ttu-id="03be3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03be3-112">-DefaultProfile</span></span>
<span data-ttu-id="03be3-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03be3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03be3-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="03be3-114">-Location</span></span>
<span data-ttu-id="03be3-115">Gibt den Bereich an, für den das Cmdlet die Kontingente überprüft.</span><span class="sxs-lookup"><span data-stu-id="03be3-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="03be3-116">Weitere Informationen finden Sie unter Azure-Bereiche ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="03be3-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03be3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03be3-117">CommonParameters</span></span>
<span data-ttu-id="03be3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03be3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03be3-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03be3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03be3-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03be3-120">INPUTS</span></span>

### <span data-ttu-id="03be3-121">Keine</span><span class="sxs-lookup"><span data-stu-id="03be3-121">None</span></span>
<span data-ttu-id="03be3-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="03be3-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03be3-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03be3-123">OUTPUTS</span></span>

### <span data-ttu-id="03be3-124">Microsoft.Azure.Commands.Batch. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="03be3-124">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="03be3-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="03be3-125">NOTES</span></span>

## <span data-ttu-id="03be3-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03be3-126">RELATED LINKS</span></span>

