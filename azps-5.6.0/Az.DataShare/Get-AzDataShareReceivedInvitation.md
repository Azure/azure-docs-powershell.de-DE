---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 563c97ec87a758668c737465ea50642324706a9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948723"
---
# <span data-ttu-id="03ece-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="03ece-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="03ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ece-102">SYNOPSIS</span></span>
<span data-ttu-id="03ece-103">Ruft Informationen zu Verbrauchereinladungen ab.</span><span class="sxs-lookup"><span data-stu-id="03ece-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="03ece-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03ece-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ece-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03ece-105">DESCRIPTION</span></span>
<span data-ttu-id="03ece-106">Das **Cmdlet Get-AzDataShareReceivedInvitation** enthält Informationen zu allen Einladungen, die der Verbraucher erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="03ece-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="03ece-107">Wenn Sie einen Ort oder eine Einladungs-ID bereitstellen, enthält dieses Cmdlet Informationen zur Einladung an einem bestimmten Ort oder zur Einladungs-ID. Andernfalls enthält es eine Liste der Einladungen, die an den Verbraucher gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="03ece-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="03ece-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03ece-108">EXAMPLES</span></span>

### <span data-ttu-id="03ece-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03ece-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="03ece-110">Dieser Commant enthält Informationen zu Verbrauchereinladungen.</span><span class="sxs-lookup"><span data-stu-id="03ece-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="03ece-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="03ece-111">PARAMETERS</span></span>

### <span data-ttu-id="03ece-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-112">-DefaultProfile</span></span>
<span data-ttu-id="03ece-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03ece-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03ece-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="03ece-114">-InvitationId</span></span>
<span data-ttu-id="03ece-115">Azure dataShare-Einladungs-ID.</span><span class="sxs-lookup"><span data-stu-id="03ece-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ece-116">-Location</span><span class="sxs-lookup"><span data-stu-id="03ece-116">-Location</span></span>
<span data-ttu-id="03ece-117">Azure Data Share Invitation Location.</span><span class="sxs-lookup"><span data-stu-id="03ece-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ece-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ece-118">CommonParameters</span></span>
<span data-ttu-id="03ece-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ece-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ece-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03ece-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ece-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03ece-121">INPUTS</span></span>

### <span data-ttu-id="03ece-122">Keine</span><span class="sxs-lookup"><span data-stu-id="03ece-122">None</span></span>

## <span data-ttu-id="03ece-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03ece-123">OUTPUTS</span></span>

### <span data-ttu-id="03ece-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="03ece-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="03ece-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="03ece-125">NOTES</span></span>

## <span data-ttu-id="03ece-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="03ece-126">RELATED LINKS</span></span>
