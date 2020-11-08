---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003729"
---
# <span data-ttu-id="92be3-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="92be3-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="92be3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92be3-102">SYNOPSIS</span></span>

<span data-ttu-id="92be3-103">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="92be3-103">Sets vault context.</span></span>

## <span data-ttu-id="92be3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92be3-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92be3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92be3-105">DESCRIPTION</span></span>

<span data-ttu-id="92be3-106">Das Cmdlet " **Set-AzRecoveryServicesVaultContext** " legt den Vault-Kontext für Azure Site Recovery Services fest.</span><span class="sxs-lookup"><span data-stu-id="92be3-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="92be3-107">Warnung: Dieses Cmdlet wird in einer zukünftigen Version von Breaking Change veraltet.</span><span class="sxs-lookup"><span data-stu-id="92be3-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="92be3-108">Dafür wird es keinen Ersatz geben.</span><span class="sxs-lookup"><span data-stu-id="92be3-108">There will be no replacement for it.</span></span> <span data-ttu-id="92be3-109">Verwenden Sie den-Vault-Parameter in allen Befehlen für Wiederherstellungsdienste, die weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="92be3-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="92be3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92be3-110">EXAMPLES</span></span>

### <span data-ttu-id="92be3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92be3-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="92be3-112">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="92be3-112">Sets vault context.</span></span>

## <span data-ttu-id="92be3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="92be3-113">PARAMETERS</span></span>

### <span data-ttu-id="92be3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92be3-114">-DefaultProfile</span></span>

<span data-ttu-id="92be3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92be3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92be3-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="92be3-116">-Vault</span></span>

<span data-ttu-id="92be3-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="92be3-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="92be3-118">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="92be3-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="92be3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92be3-119">CommonParameters</span></span>
<span data-ttu-id="92be3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92be3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92be3-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92be3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92be3-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92be3-122">INPUTS</span></span>

### <span data-ttu-id="92be3-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="92be3-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="92be3-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92be3-124">OUTPUTS</span></span>

### <span data-ttu-id="92be3-125">System. void</span><span class="sxs-lookup"><span data-stu-id="92be3-125">System.Void</span></span>

## <span data-ttu-id="92be3-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="92be3-126">NOTES</span></span>

## <span data-ttu-id="92be3-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92be3-127">RELATED LINKS</span></span>
