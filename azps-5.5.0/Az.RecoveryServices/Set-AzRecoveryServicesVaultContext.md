---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158524"
---
# <span data-ttu-id="9d6a4-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="9d6a4-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="9d6a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d6a4-102">SYNOPSIS</span></span>

<span data-ttu-id="9d6a4-103">Legt den Tresorkontext fest.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-103">Sets vault context.</span></span>

## <span data-ttu-id="9d6a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d6a4-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d6a4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d6a4-105">DESCRIPTION</span></span>

<span data-ttu-id="9d6a4-106">Das **Cmdlet "Set-AzRecoveryServicesVaultContext"** legt den Tresorkontext für Azure Site Recovery Services fest.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="9d6a4-107">Warnung: Dieses Cmdlet wird in einer zukünftigen Änderungsversion nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="9d6a4-108">Es wird kein Ersatz dafür verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-108">There will be no replacement for it.</span></span> <span data-ttu-id="9d6a4-109">Verwenden Sie in Zukunft den Parameter "-VaultId" in allen Wiederherstellungsdienste-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="9d6a4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d6a4-110">EXAMPLES</span></span>

### <span data-ttu-id="9d6a4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d6a4-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="9d6a4-112">Legt den Tresorkontext fest.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-112">Sets vault context.</span></span>

## <span data-ttu-id="9d6a4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d6a4-113">PARAMETERS</span></span>

### <span data-ttu-id="9d6a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d6a4-114">-DefaultProfile</span></span>

<span data-ttu-id="9d6a4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d6a4-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="9d6a4-116">-Vault</span></span>

<span data-ttu-id="9d6a4-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="9d6a4-118">Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9d6a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d6a4-119">CommonParameters</span></span>
<span data-ttu-id="9d6a4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d6a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d6a4-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d6a4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d6a4-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d6a4-122">INPUTS</span></span>

### <span data-ttu-id="9d6a4-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="9d6a4-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9d6a4-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d6a4-124">OUTPUTS</span></span>

### <span data-ttu-id="9d6a4-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="9d6a4-125">System.Void</span></span>

## <span data-ttu-id="9d6a4-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d6a4-126">NOTES</span></span>

## <span data-ttu-id="9d6a4-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d6a4-127">RELATED LINKS</span></span>
