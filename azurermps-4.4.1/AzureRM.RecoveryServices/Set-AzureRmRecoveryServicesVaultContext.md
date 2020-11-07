---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664456"
---
# <span data-ttu-id="41ec8-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="41ec8-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="41ec8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="41ec8-103">Legt den Vault-Kontext fest.</span><span class="sxs-lookup"><span data-stu-id="41ec8-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41ec8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41ec8-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41ec8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41ec8-105">DESCRIPTION</span></span>
<span data-ttu-id="41ec8-106">Das Cmdlet " **Set-AzureRmRecoveryServicesVaultContext** " legt den Vault-Kontext für Azure Site Recovery Services fest.</span><span class="sxs-lookup"><span data-stu-id="41ec8-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="41ec8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41ec8-107">EXAMPLES</span></span>

## <span data-ttu-id="41ec8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="41ec8-108">PARAMETERS</span></span>

### <span data-ttu-id="41ec8-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="41ec8-109">-Vault</span></span>
<span data-ttu-id="41ec8-110">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="41ec8-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="41ec8-111">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="41ec8-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="41ec8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ec8-112">-DefaultProfile</span></span>
<span data-ttu-id="41ec8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41ec8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41ec8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ec8-114">CommonParameters</span></span>
<span data-ttu-id="41ec8-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ec8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ec8-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41ec8-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ec8-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41ec8-117">INPUTS</span></span>

### <span data-ttu-id="41ec8-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="41ec8-118">ARSVault</span></span>
<span data-ttu-id="41ec8-119">Der Parameter "Vault" akzeptiert den Wert vom Typ "ARSVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="41ec8-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="41ec8-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41ec8-120">OUTPUTS</span></span>

## <span data-ttu-id="41ec8-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="41ec8-121">NOTES</span></span>

## <span data-ttu-id="41ec8-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41ec8-122">RELATED LINKS</span></span>

