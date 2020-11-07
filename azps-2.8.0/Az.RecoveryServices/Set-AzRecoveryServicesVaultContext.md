---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 6a611017b2effa4733b75f56e6799f6857dcdfa8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825231"
---
# <span data-ttu-id="1d918-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="1d918-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="1d918-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d918-102">SYNOPSIS</span></span>

<span data-ttu-id="1d918-103">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="1d918-103">Sets vault context.</span></span>

## <span data-ttu-id="1d918-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d918-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d918-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d918-105">DESCRIPTION</span></span>

<span data-ttu-id="1d918-106">Das Cmdlet " **Set-AzRecoveryServicesVaultContext** " legt den Vault-Kontext für Azure Site Recovery Services fest.</span><span class="sxs-lookup"><span data-stu-id="1d918-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="1d918-107">Warnung: Dieses Cmdlet wird in einer zukünftigen Version von Breaking Change veraltet.</span><span class="sxs-lookup"><span data-stu-id="1d918-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="1d918-108">Dafür wird es keinen Ersatz geben.</span><span class="sxs-lookup"><span data-stu-id="1d918-108">There will be no replacement for it.</span></span> <span data-ttu-id="1d918-109">Verwenden Sie den-Vault-Parameter in allen Befehlen für Wiederherstellungsdienste, die weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="1d918-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="1d918-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d918-110">EXAMPLES</span></span>

### <span data-ttu-id="1d918-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1d918-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="1d918-112">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="1d918-112">Sets vault context.</span></span>

## <span data-ttu-id="1d918-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d918-113">PARAMETERS</span></span>

### <span data-ttu-id="1d918-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d918-114">-DefaultProfile</span></span>

<span data-ttu-id="1d918-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d918-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d918-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="1d918-116">-Vault</span></span>

<span data-ttu-id="1d918-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="1d918-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="1d918-118">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="1d918-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="1d918-119">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d918-119">-CommonParameters</span></span>

<span data-ttu-id="1d918-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d918-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d918-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d918-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d918-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d918-122">INPUTS</span></span>

### <span data-ttu-id="1d918-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="1d918-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="1d918-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d918-124">OUTPUTS</span></span>

### <span data-ttu-id="1d918-125">System. void</span><span class="sxs-lookup"><span data-stu-id="1d918-125">System.Void</span></span>

## <span data-ttu-id="1d918-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d918-126">NOTES</span></span>

## <span data-ttu-id="1d918-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d918-127">RELATED LINKS</span></span>
