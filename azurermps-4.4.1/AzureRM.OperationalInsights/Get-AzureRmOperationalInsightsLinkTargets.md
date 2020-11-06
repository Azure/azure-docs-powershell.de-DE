---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 3f0418a06b11af933cfc7ad09a2c0fc492db4f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501697"
---
# <span data-ttu-id="8fe97-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="8fe97-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="8fe97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fe97-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe97-103">Ruft Konten ab, die keinem Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8fe97-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fe97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fe97-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fe97-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fe97-105">DESCRIPTION</span></span>
<span data-ttu-id="8fe97-106">Das Cmdlet " **Get-AzureRmOperationalInsightsLinkTargets** " listet vorhandene Konten auf, die keinem Azure-Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8fe97-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="8fe97-107">Wenn Sie einen neuen Arbeitsbereich mit einem vorhandenen Konto verknüpfen möchten, verwenden Sie eine Kunden-ID, die von diesem Vorgang in der Eigenschaft Kunden-ID eines neuen Arbeitsbereichs zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8fe97-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="8fe97-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fe97-108">EXAMPLES</span></span>

### <span data-ttu-id="8fe97-109">Beispiel 1: Abrufen von unverknüpften Konten</span><span class="sxs-lookup"><span data-stu-id="8fe97-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="8fe97-110">Dieser Befehl ruft Konten mit unverknüpften Konten ab, die der ID des Anrufers gehören.</span><span class="sxs-lookup"><span data-stu-id="8fe97-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="8fe97-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fe97-111">PARAMETERS</span></span>

### <span data-ttu-id="8fe97-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe97-112">-DefaultProfile</span></span>
<span data-ttu-id="8fe97-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fe97-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fe97-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe97-114">CommonParameters</span></span>
<span data-ttu-id="8fe97-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fe97-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe97-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe97-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe97-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fe97-117">INPUTS</span></span>

## <span data-ttu-id="8fe97-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fe97-118">OUTPUTS</span></span>

### <span data-ttu-id="8fe97-119">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="8fe97-119">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="8fe97-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fe97-120">NOTES</span></span>

## <span data-ttu-id="8fe97-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fe97-121">RELATED LINKS</span></span>

[<span data-ttu-id="8fe97-122">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="8fe97-122">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


