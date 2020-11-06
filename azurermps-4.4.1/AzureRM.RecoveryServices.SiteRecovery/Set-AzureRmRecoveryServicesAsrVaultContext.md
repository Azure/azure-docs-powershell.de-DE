---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481670"
---
# <span data-ttu-id="a5760-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="a5760-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="a5760-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5760-102">SYNOPSIS</span></span>
<span data-ttu-id="a5760-103">Legt den Vault-Kontext für Wiederherstellungsdienste für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen PowerShell-Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="a5760-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5760-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5760-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5760-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5760-105">DESCRIPTION</span></span>
<span data-ttu-id="a5760-106">Das Cmdlet " **Set-AzureRmRecoveryServicesAsrVaultContext** " legt den Azure Site Recovery Vault-Kontext für weitere Vorgänge fest.</span><span class="sxs-lookup"><span data-stu-id="a5760-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="a5760-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5760-107">EXAMPLES</span></span>

### <span data-ttu-id="a5760-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5760-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="a5760-109">Legt den Vault-Kontext auf den angegebenen Recovery Services Vault für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen PowerShell-Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="a5760-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="a5760-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5760-110">PARAMETERS</span></span>

### <span data-ttu-id="a5760-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="a5760-111">-Vault</span></span>
<span data-ttu-id="a5760-112">Das Vault-Objekt für Wiederherstellungsdienste, das dem Speicher für Wiederherstellungsdienste entspricht.</span><span class="sxs-lookup"><span data-stu-id="a5760-112">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="a5760-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5760-113">-Confirm</span></span>
<span data-ttu-id="a5760-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5760-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5760-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5760-115">-WhatIf</span></span>
<span data-ttu-id="a5760-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5760-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5760-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5760-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5760-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5760-118">CommonParameters</span></span>
<span data-ttu-id="a5760-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5760-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5760-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5760-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5760-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5760-121">INPUTS</span></span>

### <span data-ttu-id="a5760-122">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a5760-122">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a5760-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5760-123">OUTPUTS</span></span>

### <span data-ttu-id="a5760-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="a5760-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="a5760-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5760-125">NOTES</span></span>

## <span data-ttu-id="a5760-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5760-126">RELATED LINKS</span></span>

