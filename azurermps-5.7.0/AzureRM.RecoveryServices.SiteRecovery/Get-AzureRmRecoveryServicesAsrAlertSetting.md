---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663453"
---
# <span data-ttu-id="10908-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="10908-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="10908-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10908-102">SYNOPSIS</span></span>
<span data-ttu-id="10908-103">Ruft die konfigurierten Einstellungen für die Azure Site Recovery-Benachrichtigung für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="10908-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10908-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10908-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10908-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10908-105">DESCRIPTION</span></span>
<span data-ttu-id="10908-106">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrAlertSetting** " Ruft die konfigurierten Azure Site Recovery-Benachrichtigungseinstellungen für den Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="10908-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="10908-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10908-107">EXAMPLES</span></span>

### <span data-ttu-id="10908-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10908-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="10908-109">Benachrichtigungs-und Benachrichtigungseinstellung für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="10908-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="10908-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10908-110">PARAMETERS</span></span>

### <span data-ttu-id="10908-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10908-111">-DefaultProfile</span></span>
<span data-ttu-id="10908-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10908-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10908-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10908-113">CommonParameters</span></span>
<span data-ttu-id="10908-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10908-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10908-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10908-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10908-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10908-116">INPUTS</span></span>

### <span data-ttu-id="10908-117">Keine</span><span class="sxs-lookup"><span data-stu-id="10908-117">None</span></span>

## <span data-ttu-id="10908-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10908-118">OUTPUTS</span></span>

### <span data-ttu-id="10908-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="10908-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="10908-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="10908-120">NOTES</span></span>

## <span data-ttu-id="10908-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10908-121">RELATED LINKS</span></span>
