---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470370"
---
# <span data-ttu-id="27b99-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="27b99-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="27b99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b99-102">SYNOPSIS</span></span>
<span data-ttu-id="27b99-103">Ruft Informationen zu den Einstellungen des ASR-Tresors für den Wiederherstellungsdienst ab.</span><span class="sxs-lookup"><span data-stu-id="27b99-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="27b99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27b99-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27b99-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27b99-105">DESCRIPTION</span></span>
<span data-ttu-id="27b99-106">Das **Cmdlet "Get-AzRecoveryServicesAsrVaultContext"** ruft Informationen zu den Einstellungen des ASR-Tresors ab, die mit dem Wiederherstellungsdiensttresor in Zusammenhang stehen.</span><span class="sxs-lookup"><span data-stu-id="27b99-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="27b99-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27b99-107">EXAMPLES</span></span>

### <span data-ttu-id="27b99-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27b99-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="27b99-109">Ruft die Einstellungen des ASR-Tresors für den derzeit aktiven (in der PowerShell-Sitzung) Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="27b99-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="27b99-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b99-110">PARAMETERS</span></span>

### <span data-ttu-id="27b99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b99-111">-DefaultProfile</span></span>
<span data-ttu-id="27b99-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27b99-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b99-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b99-113">CommonParameters</span></span>
<span data-ttu-id="27b99-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b99-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b99-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27b99-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b99-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27b99-116">INPUTS</span></span>

### <span data-ttu-id="27b99-117">Keine</span><span class="sxs-lookup"><span data-stu-id="27b99-117">None</span></span>

## <span data-ttu-id="27b99-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27b99-118">OUTPUTS</span></span>

### <span data-ttu-id="27b99-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="27b99-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="27b99-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27b99-120">NOTES</span></span>

## <span data-ttu-id="27b99-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27b99-121">RELATED LINKS</span></span>
