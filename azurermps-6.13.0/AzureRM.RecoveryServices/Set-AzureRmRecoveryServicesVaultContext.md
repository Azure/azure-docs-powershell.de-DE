---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 0989bdcc14a9f7e3cbd65af11aea843cdd0ec6e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477750"
---
# <span data-ttu-id="d1384-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="d1384-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="d1384-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1384-102">SYNOPSIS</span></span>
<span data-ttu-id="d1384-103">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="d1384-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1384-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1384-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1384-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1384-105">DESCRIPTION</span></span>
<span data-ttu-id="d1384-106">Das Cmdlet " **Set-AzureRmRecoveryServicesVaultContext** " legt den Vault-Kontext für Azure Site Recovery Services fest.</span><span class="sxs-lookup"><span data-stu-id="d1384-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="d1384-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1384-107">EXAMPLES</span></span>

### <span data-ttu-id="d1384-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1384-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="d1384-109">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="d1384-109">Sets vault context.</span></span>

## <span data-ttu-id="d1384-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1384-110">PARAMETERS</span></span>

### <span data-ttu-id="d1384-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="d1384-111">-Vault</span></span>
<span data-ttu-id="d1384-112">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="d1384-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="d1384-113">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="d1384-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1384-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1384-114">-DefaultProfile</span></span>
<span data-ttu-id="d1384-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1384-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1384-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1384-116">CommonParameters</span></span>
<span data-ttu-id="d1384-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1384-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1384-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1384-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1384-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1384-119">INPUTS</span></span>

### <span data-ttu-id="d1384-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d1384-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="d1384-121">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1384-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="d1384-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1384-122">OUTPUTS</span></span>

### <span data-ttu-id="d1384-123">System. void</span><span class="sxs-lookup"><span data-stu-id="d1384-123">System.Void</span></span>

## <span data-ttu-id="d1384-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1384-124">NOTES</span></span>

## <span data-ttu-id="d1384-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1384-125">RELATED LINKS</span></span>
