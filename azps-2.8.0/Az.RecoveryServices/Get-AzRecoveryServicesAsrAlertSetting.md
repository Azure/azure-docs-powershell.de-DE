---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: e7ce712102ffbb74fd8f19eed544642af5a6ebce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824439"
---
# <span data-ttu-id="f1c3a-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="f1c3a-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="f1c3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c3a-103">Ruft die konfigurierten Einstellungen für die Azure Site Recovery-Benachrichtigung für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="f1c3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1c3a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c3a-106">Das Cmdlet " **Get-AzRecoveryServicesAsrAlertSetting** " Ruft die konfigurierten Azure Site Recovery-Benachrichtigungseinstellungen für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="f1c3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1c3a-107">EXAMPLES</span></span>

### <span data-ttu-id="f1c3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1c3a-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="f1c3a-109">Benachrichtigungs-und Benachrichtigungseinstellung für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="f1c3a-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="f1c3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1c3a-110">PARAMETERS</span></span>

### <span data-ttu-id="f1c3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c3a-111">-DefaultProfile</span></span>
<span data-ttu-id="f1c3a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c3a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c3a-113">CommonParameters</span></span>
<span data-ttu-id="f1c3a-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c3a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c3a-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c3a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c3a-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1c3a-116">INPUTS</span></span>

### <span data-ttu-id="f1c3a-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f1c3a-117">None</span></span>

## <span data-ttu-id="f1c3a-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1c3a-118">OUTPUTS</span></span>

### <span data-ttu-id="f1c3a-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="f1c3a-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="f1c3a-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1c3a-120">NOTES</span></span>

## <span data-ttu-id="f1c3a-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1c3a-121">RELATED LINKS</span></span>
