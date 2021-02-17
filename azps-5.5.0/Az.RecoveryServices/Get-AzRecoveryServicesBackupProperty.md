---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153860"
---
# <span data-ttu-id="cf3aa-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="cf3aa-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="cf3aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3aa-103">Ruft Sicherungseigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="cf3aa-103">Gets Backup properties.</span></span>

## <span data-ttu-id="cf3aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf3aa-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf3aa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf3aa-105">DESCRIPTION</span></span>
<span data-ttu-id="cf3aa-106">Das **Cmdlet "Get-AzRecoveryServicesBackupProperty"** ruft Sicherungseigenschaften für einen Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="cf3aa-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="cf3aa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf3aa-107">EXAMPLES</span></span>

### <span data-ttu-id="cf3aa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cf3aa-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="cf3aa-109">Holen Sie sich die Sicherungstresoreigenschaft für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="cf3aa-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="cf3aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf3aa-110">PARAMETERS</span></span>

### <span data-ttu-id="cf3aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3aa-111">-DefaultProfile</span></span>
<span data-ttu-id="cf3aa-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf3aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf3aa-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="cf3aa-113">-Vault</span></span>
<span data-ttu-id="cf3aa-114">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="cf3aa-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="cf3aa-115">Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.</span><span class="sxs-lookup"><span data-stu-id="cf3aa-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="cf3aa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3aa-116">CommonParameters</span></span>
<span data-ttu-id="cf3aa-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3aa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3aa-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf3aa-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3aa-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf3aa-119">INPUTS</span></span>

### <span data-ttu-id="cf3aa-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="cf3aa-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="cf3aa-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf3aa-121">OUTPUTS</span></span>

### <span data-ttu-id="cf3aa-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="cf3aa-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="cf3aa-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf3aa-123">NOTES</span></span>

## <span data-ttu-id="cf3aa-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf3aa-124">RELATED LINKS</span></span>
