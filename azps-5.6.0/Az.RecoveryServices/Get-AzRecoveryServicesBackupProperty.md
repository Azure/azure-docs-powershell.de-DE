---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 2cabaaedbd384237cd8be1469ea5f28cbc1e951f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934720"
---
# <span data-ttu-id="a7e10-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="a7e10-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="a7e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e10-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e10-103">Ruft Sicherungseigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="a7e10-103">Gets Backup properties.</span></span>

## <span data-ttu-id="a7e10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7e10-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e10-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7e10-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e10-106">Das **Get-AzRecoveryServicesBackupProperty-Cmdlet** ruft Sicherungseigenschaften für einen Recovery Services-Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="a7e10-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="a7e10-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7e10-107">EXAMPLES</span></span>

### <span data-ttu-id="a7e10-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a7e10-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="a7e10-109">Holen Sie sich die Sicherungstresoreigenschaft für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="a7e10-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="a7e10-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7e10-110">PARAMETERS</span></span>

### <span data-ttu-id="a7e10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e10-111">-DefaultProfile</span></span>
<span data-ttu-id="a7e10-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7e10-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e10-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="a7e10-113">-Vault</span></span>
<span data-ttu-id="a7e10-114">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="a7e10-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="a7e10-115">Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.</span><span class="sxs-lookup"><span data-stu-id="a7e10-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="a7e10-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e10-116">CommonParameters</span></span>
<span data-ttu-id="a7e10-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7e10-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e10-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7e10-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e10-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7e10-119">INPUTS</span></span>

### <span data-ttu-id="a7e10-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a7e10-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a7e10-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7e10-121">OUTPUTS</span></span>

### <span data-ttu-id="a7e10-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="a7e10-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="a7e10-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7e10-123">NOTES</span></span>

## <span data-ttu-id="a7e10-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7e10-124">RELATED LINKS</span></span>
