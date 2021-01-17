---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471615"
---
# <span data-ttu-id="85666-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="85666-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="85666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85666-102">SYNOPSIS</span></span>

<span data-ttu-id="85666-103">Legt den Tresorkontext fest.</span><span class="sxs-lookup"><span data-stu-id="85666-103">Sets vault context.</span></span>

## <span data-ttu-id="85666-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85666-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85666-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85666-105">DESCRIPTION</span></span>

<span data-ttu-id="85666-106">Das **Cmdlet "Set-AzRecoveryServicesVaultContext"** legt den Tresorkontext für Azure Site Recovery Services fest.</span><span class="sxs-lookup"><span data-stu-id="85666-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="85666-107">Warnung: Dieses Cmdlet wird in einer zukünftigen Version der änderungsveränderung nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="85666-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="85666-108">Es wird kein Ersatz dafür verwendet.</span><span class="sxs-lookup"><span data-stu-id="85666-108">There will be no replacement for it.</span></span> <span data-ttu-id="85666-109">Verwenden Sie in Zukunft den Parameter "-VaultId" in allen Wiederherstellungsdienste-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="85666-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="85666-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85666-110">EXAMPLES</span></span>

### <span data-ttu-id="85666-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85666-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="85666-112">Legt den Tresorkontext fest.</span><span class="sxs-lookup"><span data-stu-id="85666-112">Sets vault context.</span></span>

## <span data-ttu-id="85666-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85666-113">PARAMETERS</span></span>

### <span data-ttu-id="85666-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85666-114">-DefaultProfile</span></span>

<span data-ttu-id="85666-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85666-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85666-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="85666-116">-Vault</span></span>

<span data-ttu-id="85666-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="85666-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="85666-118">Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.</span><span class="sxs-lookup"><span data-stu-id="85666-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="85666-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85666-119">CommonParameters</span></span>
<span data-ttu-id="85666-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85666-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85666-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85666-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85666-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85666-122">INPUTS</span></span>

### <span data-ttu-id="85666-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="85666-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="85666-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85666-124">OUTPUTS</span></span>

### <span data-ttu-id="85666-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="85666-125">System.Void</span></span>

## <span data-ttu-id="85666-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85666-126">NOTES</span></span>

## <span data-ttu-id="85666-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85666-127">RELATED LINKS</span></span>
