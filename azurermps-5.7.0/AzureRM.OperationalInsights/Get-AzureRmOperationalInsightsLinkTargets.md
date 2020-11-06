---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightslinktargets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsLinkTargets.md
ms.openlocfilehash: 64e74b2c9d4aa5f22d48bb6cb80c5a1952424c38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481070"
---
# <span data-ttu-id="8f511-101">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="8f511-101">Get-AzureRmOperationalInsightsLinkTargets</span></span>

## <span data-ttu-id="8f511-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f511-102">SYNOPSIS</span></span>
<span data-ttu-id="8f511-103">Ruft Konten ab, die keinem Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8f511-103">Gets accounts that are not associated with a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f511-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f511-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsLinkTargets [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f511-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f511-105">DESCRIPTION</span></span>
<span data-ttu-id="8f511-106">Das Cmdlet " **Get-AzureRmOperationalInsightsLinkTargets** " listet vorhandene Konten auf, die keinem Azure-Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8f511-106">The **Get-AzureRmOperationalInsightsLinkTargets** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="8f511-107">Wenn Sie einen neuen Arbeitsbereich mit einem vorhandenen Konto verknüpfen möchten, verwenden Sie eine Kunden-ID, die von diesem Vorgang in der Eigenschaft Kunden-ID eines neuen Arbeitsbereichs zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f511-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="8f511-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f511-108">EXAMPLES</span></span>

### <span data-ttu-id="8f511-109">Beispiel 1: Abrufen von unverknüpften Konten</span><span class="sxs-lookup"><span data-stu-id="8f511-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsLinkTargets
```

<span data-ttu-id="8f511-110">Dieser Befehl ruft Konten mit unverknüpften Konten ab, die der ID des Anrufers gehören.</span><span class="sxs-lookup"><span data-stu-id="8f511-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="8f511-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f511-111">PARAMETERS</span></span>

### <span data-ttu-id="8f511-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f511-112">-DefaultProfile</span></span>
<span data-ttu-id="8f511-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f511-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f511-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f511-114">CommonParameters</span></span>
<span data-ttu-id="8f511-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f511-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f511-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f511-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f511-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f511-117">INPUTS</span></span>

### <span data-ttu-id="8f511-118">Keine</span><span class="sxs-lookup"><span data-stu-id="8f511-118">None</span></span>
<span data-ttu-id="8f511-119">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8f511-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f511-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f511-120">OUTPUTS</span></span>

### <span data-ttu-id="8f511-121">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount]</span><span class="sxs-lookup"><span data-stu-id="8f511-121">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount]</span></span>

## <span data-ttu-id="8f511-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f511-122">NOTES</span></span>

## <span data-ttu-id="8f511-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f511-123">RELATED LINKS</span></span>

[<span data-ttu-id="8f511-124">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="8f511-124">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


