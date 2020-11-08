---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 35C6E85B-E5E1-44E8-86E8-F18E197F69DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinktarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkTarget.md
ms.openlocfilehash: 72841dc8ecc90c14bb41ae8f0f207d990afec9a8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007477"
---
# <span data-ttu-id="d483b-101">Get-AzOperationalInsightsLinkTarget</span><span class="sxs-lookup"><span data-stu-id="d483b-101">Get-AzOperationalInsightsLinkTarget</span></span>

## <span data-ttu-id="d483b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d483b-102">SYNOPSIS</span></span>
<span data-ttu-id="d483b-103">Ruft Konten ab, die keinem Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d483b-103">Gets accounts that are not associated with a subscription.</span></span>

## <span data-ttu-id="d483b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d483b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkTarget [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d483b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d483b-105">DESCRIPTION</span></span>
<span data-ttu-id="d483b-106">Das Cmdlet " **Get-AzOperationalInsightsLinkTarget** " listet vorhandene Konten auf, die keinem Azure-Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d483b-106">The **Get-AzOperationalInsightsLinkTarget** cmdlet lists existing accounts that are not associated with an Azure subscription.</span></span>
<span data-ttu-id="d483b-107">Wenn Sie einen neuen Arbeitsbereich mit einem vorhandenen Konto verknüpfen möchten, verwenden Sie eine Kunden-ID, die von diesem Vorgang in der Eigenschaft Kunden-ID eines neuen Arbeitsbereichs zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d483b-107">To link a new workspace to an existing account, use a customer ID returned by this operation in the customer ID property of a new workspace.</span></span>

## <span data-ttu-id="d483b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d483b-108">EXAMPLES</span></span>

### <span data-ttu-id="d483b-109">Beispiel 1: Abrufen von unverknüpften Konten</span><span class="sxs-lookup"><span data-stu-id="d483b-109">Example 1: Get unlinked accounts</span></span>
```
PS C:\>Get-AzOperationalInsightsLinkTarget
```

<span data-ttu-id="d483b-110">Dieser Befehl ruft Konten mit unverknüpften Konten ab, die der ID des Anrufers gehören.</span><span class="sxs-lookup"><span data-stu-id="d483b-110">This command gets unlinked accounts that are owned by the caller's ID.</span></span>

## <span data-ttu-id="d483b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d483b-111">PARAMETERS</span></span>

### <span data-ttu-id="d483b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d483b-112">-DefaultProfile</span></span>
<span data-ttu-id="d483b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d483b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d483b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d483b-114">CommonParameters</span></span>
<span data-ttu-id="d483b-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d483b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d483b-116">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d483b-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d483b-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d483b-117">INPUTS</span></span>

### <span data-ttu-id="d483b-118">Keine</span><span class="sxs-lookup"><span data-stu-id="d483b-118">None</span></span>

## <span data-ttu-id="d483b-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d483b-119">OUTPUTS</span></span>

### <span data-ttu-id="d483b-120">Microsoft. Azure. Commands. OperationalInsights. Models. PSAccount</span><span class="sxs-lookup"><span data-stu-id="d483b-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSAccount</span></span>

## <span data-ttu-id="d483b-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="d483b-121">NOTES</span></span>

## <span data-ttu-id="d483b-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d483b-122">RELATED LINKS</span></span>

[<span data-ttu-id="d483b-123">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="d483b-123">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


