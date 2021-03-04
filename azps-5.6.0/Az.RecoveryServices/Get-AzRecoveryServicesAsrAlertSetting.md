---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: cadde5ec773452897aa9c6915a5f3e16f00cfef5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946468"
---
# <span data-ttu-id="b31d4-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b31d4-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="b31d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b31d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b31d4-103">Ruft die konfigurierten Azure Site Recovery-Benachrichtigungseinstellungen für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="b31d4-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b31d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b31d4-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b31d4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b31d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b31d4-106">Das **Get-AzRecoveryServicesAsrAlertSetting-Cmdlet** ruft die konfigurierten Azure Site Recovery-Benachrichtigungseinstellungen für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="b31d4-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b31d4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b31d4-107">EXAMPLES</span></span>

### <span data-ttu-id="b31d4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b31d4-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="b31d4-109">Benachrichtigungs-/Benachrichtigungseinstellung für die Azure-Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="b31d4-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="b31d4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b31d4-110">PARAMETERS</span></span>

### <span data-ttu-id="b31d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31d4-111">-DefaultProfile</span></span>
<span data-ttu-id="b31d4-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b31d4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b31d4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31d4-113">CommonParameters</span></span>
<span data-ttu-id="b31d4-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b31d4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31d4-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b31d4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31d4-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b31d4-116">INPUTS</span></span>

### <span data-ttu-id="b31d4-117">Keine</span><span class="sxs-lookup"><span data-stu-id="b31d4-117">None</span></span>

## <span data-ttu-id="b31d4-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b31d4-118">OUTPUTS</span></span>

### <span data-ttu-id="b31d4-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b31d4-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="b31d4-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b31d4-120">NOTES</span></span>

## <span data-ttu-id="b31d4-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b31d4-121">RELATED LINKS</span></span>
