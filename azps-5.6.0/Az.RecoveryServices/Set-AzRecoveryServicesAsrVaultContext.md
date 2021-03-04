---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: ad4fe186a07adb2b9f90222d3caf8def1ecbefdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942267"
---
# <span data-ttu-id="72188-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="72188-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="72188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72188-102">SYNOPSIS</span></span>
<span data-ttu-id="72188-103">Legt den Recovery Services-Tresorkontext fest, der für nachfolgende Azure-Websitewiederherstellungsvorgänge in der aktuellen PowerShell-Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72188-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="72188-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72188-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72188-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72188-105">DESCRIPTION</span></span>
<span data-ttu-id="72188-106">Das **Cmdlet Set-AzRecoveryServicesAsrVaultContext** legt den Azure Site Recovery-Tresorkontext für weitere Vorgänge fest.</span><span class="sxs-lookup"><span data-stu-id="72188-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="72188-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72188-107">EXAMPLES</span></span>

### <span data-ttu-id="72188-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72188-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="72188-109">Legt den Tresorkontext auf den angegebenen Recovery Services-Tresor für nachfolgende Azure-Websitewiederherstellungsvorgänge in der aktuellen PowerShell-Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="72188-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="72188-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72188-110">PARAMETERS</span></span>

### <span data-ttu-id="72188-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72188-111">-DefaultProfile</span></span>
<span data-ttu-id="72188-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72188-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72188-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="72188-113">-Vault</span></span>
<span data-ttu-id="72188-114">Das Recovery Services-Tresorobjekt, das dem Recovery Services-Tresor entspricht.</span><span class="sxs-lookup"><span data-stu-id="72188-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="72188-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72188-115">-Confirm</span></span>
<span data-ttu-id="72188-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72188-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72188-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72188-117">-WhatIf</span></span>
<span data-ttu-id="72188-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72188-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72188-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72188-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72188-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72188-120">CommonParameters</span></span>
<span data-ttu-id="72188-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72188-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72188-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72188-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72188-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72188-123">INPUTS</span></span>

### <span data-ttu-id="72188-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="72188-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="72188-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72188-125">OUTPUTS</span></span>

### <span data-ttu-id="72188-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="72188-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="72188-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="72188-127">NOTES</span></span>

## <span data-ttu-id="72188-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="72188-128">RELATED LINKS</span></span>
