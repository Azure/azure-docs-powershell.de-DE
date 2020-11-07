---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846979"
---
# <span data-ttu-id="9327d-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9327d-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="9327d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9327d-102">SYNOPSIS</span></span>
<span data-ttu-id="9327d-103">Ruft die konfigurierten Einstellungen für die Azure Site Recovery-Benachrichtigung für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="9327d-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="9327d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9327d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9327d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9327d-105">DESCRIPTION</span></span>
<span data-ttu-id="9327d-106">Das Cmdlet " **Get-AzRecoveryServicesAsrAlertSetting** " Ruft die konfigurierten Azure Site Recovery-Benachrichtigungseinstellungen für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="9327d-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="9327d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9327d-107">EXAMPLES</span></span>

### <span data-ttu-id="9327d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9327d-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="9327d-109">Benachrichtigungs-und Benachrichtigungseinstellung für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="9327d-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="9327d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9327d-110">PARAMETERS</span></span>

### <span data-ttu-id="9327d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9327d-111">-DefaultProfile</span></span>
<span data-ttu-id="9327d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9327d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9327d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9327d-113">CommonParameters</span></span>
<span data-ttu-id="9327d-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9327d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9327d-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9327d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9327d-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9327d-116">INPUTS</span></span>

### <span data-ttu-id="9327d-117">Keine</span><span class="sxs-lookup"><span data-stu-id="9327d-117">None</span></span>

## <span data-ttu-id="9327d-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9327d-118">OUTPUTS</span></span>

### <span data-ttu-id="9327d-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9327d-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="9327d-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="9327d-120">NOTES</span></span>

## <span data-ttu-id="9327d-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9327d-121">RELATED LINKS</span></span>
