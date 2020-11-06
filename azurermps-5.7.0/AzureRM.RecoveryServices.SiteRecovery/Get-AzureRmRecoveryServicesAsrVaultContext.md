---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 2be1ca7de1728d1aed7758cd170cb608c7645f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502506"
---
# <span data-ttu-id="b1d70-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="b1d70-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="b1d70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1d70-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d70-103">Ruft Informationen zu ASR Vault-Einstellungen für den Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="b1d70-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1d70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1d70-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1d70-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1d70-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d70-106">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrVaultContext** " Ruft Informationen zum ASR-Tresor ab, die sich auf den Vault für Wiederherstellungsdienste beziehen.</span><span class="sxs-lookup"><span data-stu-id="b1d70-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="b1d70-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1d70-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d70-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1d70-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="b1d70-109">Ruft die Einstellungen für ASR-Tresor für den aktuell aktiven (im PowerShell-Sitzungs-) Wiederherstellungsdienste-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="b1d70-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="b1d70-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1d70-110">PARAMETERS</span></span>

### <span data-ttu-id="b1d70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d70-111">-DefaultProfile</span></span>
<span data-ttu-id="b1d70-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1d70-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1d70-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d70-113">CommonParameters</span></span>
<span data-ttu-id="b1d70-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1d70-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d70-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d70-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d70-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1d70-116">INPUTS</span></span>

### <span data-ttu-id="b1d70-117">Keine</span><span class="sxs-lookup"><span data-stu-id="b1d70-117">None</span></span>

## <span data-ttu-id="b1d70-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1d70-118">OUTPUTS</span></span>

### <span data-ttu-id="b1d70-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b1d70-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b1d70-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1d70-120">NOTES</span></span>

## <span data-ttu-id="b1d70-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1d70-121">RELATED LINKS</span></span>
