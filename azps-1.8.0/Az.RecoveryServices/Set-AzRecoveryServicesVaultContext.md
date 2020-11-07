---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659810"
---
# <span data-ttu-id="d9388-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="d9388-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="d9388-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9388-102">SYNOPSIS</span></span>
<span data-ttu-id="d9388-103">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="d9388-103">Sets vault context.</span></span>

## <span data-ttu-id="d9388-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9388-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9388-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9388-105">DESCRIPTION</span></span>
<span data-ttu-id="d9388-106">Das Cmdlet " **Set-AzRecoveryServicesVaultContext** " legt den Vault-Kontext für Azure Site Recovery Services fest.</span><span class="sxs-lookup"><span data-stu-id="d9388-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="d9388-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9388-107">EXAMPLES</span></span>

### <span data-ttu-id="d9388-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9388-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="d9388-109">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="d9388-109">Sets vault context.</span></span>

## <span data-ttu-id="d9388-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9388-110">PARAMETERS</span></span>

### <span data-ttu-id="d9388-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9388-111">-DefaultProfile</span></span>
<span data-ttu-id="d9388-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9388-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9388-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="d9388-113">-Vault</span></span>
<span data-ttu-id="d9388-114">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="d9388-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="d9388-115">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="d9388-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="d9388-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9388-116">CommonParameters</span></span>
<span data-ttu-id="d9388-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9388-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9388-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9388-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9388-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9388-119">INPUTS</span></span>

### <span data-ttu-id="d9388-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d9388-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d9388-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9388-121">OUTPUTS</span></span>

### <span data-ttu-id="d9388-122">System. void</span><span class="sxs-lookup"><span data-stu-id="d9388-122">System.Void</span></span>

## <span data-ttu-id="d9388-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9388-123">NOTES</span></span>

## <span data-ttu-id="d9388-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9388-124">RELATED LINKS</span></span>