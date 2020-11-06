---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 208ba1055523a1dc76de88d665a7b1dbd097144e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497126"
---
# <span data-ttu-id="6dd5f-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="6dd5f-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="6dd5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6dd5f-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd5f-103">Ruft die Stapelverarbeitungs Dienst Kontingente für Ihr Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="6dd5f-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dd5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dd5f-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dd5f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dd5f-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd5f-106">Ruft die Stapelverarbeitungs Dienst Kontingente für das angegebene Abonnement an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="6dd5f-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="6dd5f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6dd5f-107">EXAMPLES</span></span>

### <span data-ttu-id="6dd5f-108">Beispiel 1: Abrufen der Batch Dienst Kontingente für das Abonnement in der Region West Amerika</span><span class="sxs-lookup"><span data-stu-id="6dd5f-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="6dd5f-109">Dieser Befehl ruft die Kontingente für das aktuelle Abonnement in der West US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="6dd5f-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="6dd5f-110">Der Rückgabewert gibt an, dass dieses Abonnement nur ein Stapelverarbeitungs Konto in diesem Bereich erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6dd5f-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="6dd5f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dd5f-111">PARAMETERS</span></span>

### <span data-ttu-id="6dd5f-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="6dd5f-112">-Location</span></span>
<span data-ttu-id="6dd5f-113">Gibt den Bereich an, für den das Cmdlet die Kontingente überprüft.</span><span class="sxs-lookup"><span data-stu-id="6dd5f-113">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="6dd5f-114">Weitere Informationen finden Sie unter Azure-Bereiche ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="6dd5f-114">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="6dd5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd5f-115">-DefaultProfile</span></span>
<span data-ttu-id="6dd5f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6dd5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dd5f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd5f-117">CommonParameters</span></span>
<span data-ttu-id="6dd5f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd5f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd5f-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd5f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd5f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6dd5f-120">INPUTS</span></span>

## <span data-ttu-id="6dd5f-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6dd5f-121">OUTPUTS</span></span>

### <span data-ttu-id="6dd5f-122">Microsoft.Azure.Commands.Batch. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="6dd5f-122">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="6dd5f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="6dd5f-123">NOTES</span></span>

## <span data-ttu-id="6dd5f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6dd5f-124">RELATED LINKS</span></span>

