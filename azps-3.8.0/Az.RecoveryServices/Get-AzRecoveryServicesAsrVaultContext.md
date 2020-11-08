---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995601"
---
# <span data-ttu-id="2db8d-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="2db8d-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="2db8d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2db8d-102">SYNOPSIS</span></span>
<span data-ttu-id="2db8d-103">Ruft Informationen zu ASR Vault-Einstellungen für den Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="2db8d-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="2db8d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2db8d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2db8d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2db8d-105">DESCRIPTION</span></span>
<span data-ttu-id="2db8d-106">Das Cmdlet " **Get-AzRecoveryServicesAsrVaultContext** " Ruft Informationen zum ASR-Tresor ab, die sich auf den Vault für Wiederherstellungsdienste beziehen.</span><span class="sxs-lookup"><span data-stu-id="2db8d-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="2db8d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2db8d-107">EXAMPLES</span></span>

### <span data-ttu-id="2db8d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2db8d-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="2db8d-109">Ruft die Einstellungen für ASR-Tresor für den aktuell aktiven (im PowerShell-Sitzungs-) Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="2db8d-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="2db8d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2db8d-110">PARAMETERS</span></span>

### <span data-ttu-id="2db8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db8d-111">-DefaultProfile</span></span>
<span data-ttu-id="2db8d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2db8d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2db8d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db8d-113">CommonParameters</span></span>
<span data-ttu-id="2db8d-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2db8d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db8d-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2db8d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db8d-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2db8d-116">INPUTS</span></span>

### <span data-ttu-id="2db8d-117">Keine</span><span class="sxs-lookup"><span data-stu-id="2db8d-117">None</span></span>

## <span data-ttu-id="2db8d-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2db8d-118">OUTPUTS</span></span>

### <span data-ttu-id="2db8d-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2db8d-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="2db8d-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="2db8d-120">NOTES</span></span>

## <span data-ttu-id="2db8d-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2db8d-121">RELATED LINKS</span></span>
