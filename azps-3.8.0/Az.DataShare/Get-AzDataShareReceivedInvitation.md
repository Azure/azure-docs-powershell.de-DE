---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 18cd37f1e24851720299a647a30323f9379bea6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995871"
---
# <span data-ttu-id="e5165-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="e5165-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="e5165-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5165-102">SYNOPSIS</span></span>
<span data-ttu-id="e5165-103">Ruft Informationen zu Verbraucher Einladungen ab.</span><span class="sxs-lookup"><span data-stu-id="e5165-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="e5165-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5165-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5165-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5165-105">DESCRIPTION</span></span>
<span data-ttu-id="e5165-106">Das Cmdlet " **Get-AzDataShareReceivedInvitation** " enthält Informationen zu allen Einladungen, die der Consumer receieved hat.</span><span class="sxs-lookup"><span data-stu-id="e5165-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="e5165-107">Wenn Sie eine Standort-oder Einladungs-ID angeben, gibt dieses Cmdlet Informationen zur Einladung an einem bestimmten Ort oder zur Einladungs-ID. Andernfalls wird eine Liste der Einladungen bereitgestellt, die an den Consumer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5165-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="e5165-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5165-108">EXAMPLES</span></span>

### <span data-ttu-id="e5165-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5165-109">Example 1</span></span>
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

<span data-ttu-id="e5165-110">Dieser Commee bietet Informationen zu Verbraucher Einladungen.</span><span class="sxs-lookup"><span data-stu-id="e5165-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="e5165-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5165-111">PARAMETERS</span></span>

### <span data-ttu-id="e5165-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5165-112">-DefaultProfile</span></span>
<span data-ttu-id="e5165-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5165-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5165-114">-Einladungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="e5165-114">-InvitationId</span></span>
<span data-ttu-id="e5165-115">Azure DataShare-Einladungs-ID.</span><span class="sxs-lookup"><span data-stu-id="e5165-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="e5165-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="e5165-116">-Location</span></span>
<span data-ttu-id="e5165-117">Speicherort der Einladung zu Azure Data Freigabe.</span><span class="sxs-lookup"><span data-stu-id="e5165-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="e5165-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5165-118">CommonParameters</span></span>
<span data-ttu-id="e5165-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5165-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5165-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5165-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5165-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5165-121">INPUTS</span></span>

### <span data-ttu-id="e5165-122">Keine</span><span class="sxs-lookup"><span data-stu-id="e5165-122">None</span></span>

## <span data-ttu-id="e5165-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5165-123">OUTPUTS</span></span>

### <span data-ttu-id="e5165-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="e5165-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="e5165-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5165-125">NOTES</span></span>

## <span data-ttu-id="e5165-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5165-126">RELATED LINKS</span></span>
