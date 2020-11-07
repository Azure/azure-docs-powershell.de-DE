---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663848"
---
# <span data-ttu-id="93ef0-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="93ef0-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="93ef0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="93ef0-103">Ruft Sicherungseigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="93ef0-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ef0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93ef0-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93ef0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="93ef0-106">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupProperty** " ruft Sicherungseigenschaften für einen Vault für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="93ef0-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="93ef0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93ef0-107">EXAMPLES</span></span>

## <span data-ttu-id="93ef0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="93ef0-108">PARAMETERS</span></span>

### <span data-ttu-id="93ef0-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="93ef0-109">-Vault</span></span>
<span data-ttu-id="93ef0-110">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="93ef0-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="93ef0-111">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="93ef0-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93ef0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ef0-112">-DefaultProfile</span></span>
<span data-ttu-id="93ef0-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93ef0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ef0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ef0-114">CommonParameters</span></span>
<span data-ttu-id="93ef0-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ef0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ef0-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ef0-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ef0-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93ef0-117">INPUTS</span></span>

### <span data-ttu-id="93ef0-118">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="93ef0-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="93ef0-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93ef0-119">OUTPUTS</span></span>

### <span data-ttu-id="93ef0-120">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="93ef0-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="93ef0-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="93ef0-121">NOTES</span></span>

## <span data-ttu-id="93ef0-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93ef0-122">RELATED LINKS</span></span>

