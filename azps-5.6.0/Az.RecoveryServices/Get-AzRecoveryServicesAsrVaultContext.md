---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921656"
---
# <span data-ttu-id="037b3-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="037b3-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="037b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="037b3-102">SYNOPSIS</span></span>
<span data-ttu-id="037b3-103">Ruft Informationen zu den Einstellungen des ASR-Tresors für den Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="037b3-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="037b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="037b3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="037b3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="037b3-105">DESCRIPTION</span></span>
<span data-ttu-id="037b3-106">Das **Get-AzRecoveryServicesAsrVaultContext-Cmdlet** ruft Informationen zu den ASR-Tresoreinstellungen im Zusammenhang mit dem Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="037b3-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="037b3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="037b3-107">EXAMPLES</span></span>

### <span data-ttu-id="037b3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="037b3-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="037b3-109">Ruft die EINSTELLUNGEN für den ASR-Tresor für den derzeit aktiven (in der PowerShell-Sitzung) Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="037b3-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="037b3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="037b3-110">PARAMETERS</span></span>

### <span data-ttu-id="037b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037b3-111">-DefaultProfile</span></span>
<span data-ttu-id="037b3-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="037b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="037b3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037b3-113">CommonParameters</span></span>
<span data-ttu-id="037b3-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037b3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037b3-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="037b3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037b3-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="037b3-116">INPUTS</span></span>

### <span data-ttu-id="037b3-117">Keine</span><span class="sxs-lookup"><span data-stu-id="037b3-117">None</span></span>

## <span data-ttu-id="037b3-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="037b3-118">OUTPUTS</span></span>

### <span data-ttu-id="037b3-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="037b3-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="037b3-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="037b3-120">NOTES</span></span>

## <span data-ttu-id="037b3-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="037b3-121">RELATED LINKS</span></span>
