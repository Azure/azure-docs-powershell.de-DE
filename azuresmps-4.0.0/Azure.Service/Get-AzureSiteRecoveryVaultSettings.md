---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006772"
---
# <span data-ttu-id="511b1-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="511b1-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="511b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="511b1-102">SYNOPSIS</span></span>
<span data-ttu-id="511b1-103">Ruft die Einstellungen für ein Website Wiederherstellungs Depot ab.</span><span class="sxs-lookup"><span data-stu-id="511b1-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="511b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="511b1-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="511b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="511b1-105">DESCRIPTION</span></span>
<span data-ttu-id="511b1-106">Das Cmdlet " **Get-AzureSiteRecoveryVaultSettings** " Ruft Einstellungen ab, die sich auf das aktuelle Azure Site Recovery Vault beziehen.</span><span class="sxs-lookup"><span data-stu-id="511b1-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="511b1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="511b1-107">EXAMPLES</span></span>

### <span data-ttu-id="511b1-108">Beispiel 1: Abrufen von Einstellungsinformationen</span><span class="sxs-lookup"><span data-stu-id="511b1-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="511b1-109">Dieser Befehl ruft Einstellungsinformationen für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="511b1-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="511b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="511b1-110">PARAMETERS</span></span>

### <span data-ttu-id="511b1-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="511b1-111">-Profile</span></span>
<span data-ttu-id="511b1-112">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="511b1-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="511b1-113">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="511b1-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511b1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511b1-114">CommonParameters</span></span>
<span data-ttu-id="511b1-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511b1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511b1-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="511b1-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511b1-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="511b1-117">INPUTS</span></span>

## <span data-ttu-id="511b1-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="511b1-118">OUTPUTS</span></span>

## <span data-ttu-id="511b1-119">Notizen</span><span class="sxs-lookup"><span data-stu-id="511b1-119">NOTES</span></span>

## <span data-ttu-id="511b1-120">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="511b1-120">RELATED LINKS</span></span>

[<span data-ttu-id="511b1-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="511b1-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="511b1-122">Importieren-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="511b1-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


