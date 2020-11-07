---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 0a809f9ef3d3c89edc7571b9bb7b7cc2f03e043b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664997"
---
# <span data-ttu-id="9c592-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="9c592-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="9c592-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c592-102">SYNOPSIS</span></span>
<span data-ttu-id="9c592-103">Ruft Informationen zu ASR Vault-Einstellungen für den Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="9c592-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c592-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c592-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [<CommonParameters>]
```

## <span data-ttu-id="9c592-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c592-105">DESCRIPTION</span></span>
<span data-ttu-id="9c592-106">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrVaultContext** " Ruft Informationen zum ASR-Tresor ab, die sich auf den Vault für Wiederherstellungsdienste beziehen.</span><span class="sxs-lookup"><span data-stu-id="9c592-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="9c592-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c592-107">EXAMPLES</span></span>

### <span data-ttu-id="9c592-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9c592-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="9c592-109">Ruft die Einstellungen für ASR-Tresor für den aktuell aktiven (im PowerShell-Sitzungs-) Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="9c592-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="9c592-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c592-110">PARAMETERS</span></span>

### <span data-ttu-id="9c592-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c592-111">CommonParameters</span></span>
<span data-ttu-id="9c592-112">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c592-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c592-113">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c592-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c592-114">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c592-114">INPUTS</span></span>

### <span data-ttu-id="9c592-115">Keine</span><span class="sxs-lookup"><span data-stu-id="9c592-115">None</span></span>

## <span data-ttu-id="9c592-116">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c592-116">OUTPUTS</span></span>

### <span data-ttu-id="9c592-117">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="9c592-117">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="9c592-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c592-118">NOTES</span></span>

## <span data-ttu-id="9c592-119">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c592-119">RELATED LINKS</span></span>

