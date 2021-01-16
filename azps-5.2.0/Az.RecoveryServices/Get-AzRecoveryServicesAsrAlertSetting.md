---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301195"
---
# <span data-ttu-id="076ff-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="076ff-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="076ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076ff-102">SYNOPSIS</span></span>
<span data-ttu-id="076ff-103">Ruft die konfigurierten Benachrichtigungseinstellungen für die Azure-Websitewiederherstellung für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="076ff-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="076ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="076ff-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="076ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="076ff-105">DESCRIPTION</span></span>
<span data-ttu-id="076ff-106">Das **Cmdlet "Get-AzRecoveryServicesAsrAlertSetting"** ruft die konfigurierten Benachrichtigungseinstellungen für die Azure-Websitewiederherstellung für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="076ff-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="076ff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="076ff-107">EXAMPLES</span></span>

### <span data-ttu-id="076ff-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="076ff-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="076ff-109">Benachrichtigungs-/Benachrichtigungseinstellung für die Azure-Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="076ff-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="076ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="076ff-110">PARAMETERS</span></span>

### <span data-ttu-id="076ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076ff-111">-DefaultProfile</span></span>
<span data-ttu-id="076ff-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="076ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="076ff-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076ff-113">CommonParameters</span></span>
<span data-ttu-id="076ff-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="076ff-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076ff-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="076ff-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076ff-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="076ff-116">INPUTS</span></span>

### <span data-ttu-id="076ff-117">Keine</span><span class="sxs-lookup"><span data-stu-id="076ff-117">None</span></span>

## <span data-ttu-id="076ff-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="076ff-118">OUTPUTS</span></span>

### <span data-ttu-id="076ff-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="076ff-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="076ff-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="076ff-120">NOTES</span></span>

## <span data-ttu-id="076ff-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="076ff-121">RELATED LINKS</span></span>
