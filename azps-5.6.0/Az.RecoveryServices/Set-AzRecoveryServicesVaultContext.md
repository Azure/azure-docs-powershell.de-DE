---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 04fa3c9a7024b8a9e1f525a4ef131ae151f25804
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942243"
---
# <span data-ttu-id="be161-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="be161-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="be161-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be161-102">SYNOPSIS</span></span>

<span data-ttu-id="be161-103">Legt den Tresorkontext fest.</span><span class="sxs-lookup"><span data-stu-id="be161-103">Sets vault context.</span></span>

## <span data-ttu-id="be161-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be161-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be161-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be161-105">DESCRIPTION</span></span>

<span data-ttu-id="be161-106">Das **Cmdlet Set-AzRecoveryServicesVaultContext** legt den Tresorkontext für Azure Websitewiederherstellungsdienste fest.</span><span class="sxs-lookup"><span data-stu-id="be161-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="be161-107">Warnung: Dieses Cmdlet wird in einer zukünftigen Änderungsversion nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="be161-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="be161-108">Es gibt keinen Ersatz dafür.</span><span class="sxs-lookup"><span data-stu-id="be161-108">There will be no replacement for it.</span></span> <span data-ttu-id="be161-109">Verwenden Sie den Parameter -VaultId in allen Wiederherstellungsdiensten-Befehlen, die in Zukunft ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="be161-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="be161-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be161-110">EXAMPLES</span></span>

### <span data-ttu-id="be161-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be161-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="be161-112">Legt den Tresorkontext fest.</span><span class="sxs-lookup"><span data-stu-id="be161-112">Sets vault context.</span></span>

## <span data-ttu-id="be161-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="be161-113">PARAMETERS</span></span>

### <span data-ttu-id="be161-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be161-114">-DefaultProfile</span></span>

<span data-ttu-id="be161-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be161-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be161-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="be161-116">-Vault</span></span>

<span data-ttu-id="be161-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="be161-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="be161-118">Der Tresor muss ein **AzureRmRecoveryServicesVault-Objekt** sein.</span><span class="sxs-lookup"><span data-stu-id="be161-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="be161-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be161-119">CommonParameters</span></span>
<span data-ttu-id="be161-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be161-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be161-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be161-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be161-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be161-122">INPUTS</span></span>

### <span data-ttu-id="be161-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="be161-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="be161-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be161-124">OUTPUTS</span></span>

### <span data-ttu-id="be161-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="be161-125">System.Void</span></span>

## <span data-ttu-id="be161-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="be161-126">NOTES</span></span>

## <span data-ttu-id="be161-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="be161-127">RELATED LINKS</span></span>
