---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166163"
---
# <span data-ttu-id="966f0-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="966f0-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="966f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="966f0-102">SYNOPSIS</span></span>
<span data-ttu-id="966f0-103">Legt den Vault-Kontext für Wiederherstellungsdienste für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen PowerShell-Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="966f0-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="966f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="966f0-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="966f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="966f0-105">DESCRIPTION</span></span>
<span data-ttu-id="966f0-106">Das Cmdlet " **Set-AzRecoveryServicesAsrVaultContext** " legt den Azure Site Recovery Vault-Kontext für weitere Vorgänge fest.</span><span class="sxs-lookup"><span data-stu-id="966f0-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="966f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="966f0-107">EXAMPLES</span></span>

### <span data-ttu-id="966f0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="966f0-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="966f0-109">Legt den Vault-Kontext auf den angegebenen Recovery Services Vault für nachfolgende Azure Site Recovery-Vorgänge in der aktuellen PowerShell-Sitzung fest.</span><span class="sxs-lookup"><span data-stu-id="966f0-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="966f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="966f0-110">PARAMETERS</span></span>

### <span data-ttu-id="966f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966f0-111">-DefaultProfile</span></span>
<span data-ttu-id="966f0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="966f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="966f0-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="966f0-113">-Vault</span></span>
<span data-ttu-id="966f0-114">Das Vault-Objekt für Wiederherstellungsdienste, das dem Speicher für Wiederherstellungsdienste entspricht.</span><span class="sxs-lookup"><span data-stu-id="966f0-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="966f0-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="966f0-115">-Confirm</span></span>
<span data-ttu-id="966f0-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="966f0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="966f0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="966f0-117">-WhatIf</span></span>
<span data-ttu-id="966f0-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="966f0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="966f0-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="966f0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="966f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966f0-120">CommonParameters</span></span>
<span data-ttu-id="966f0-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966f0-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="966f0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966f0-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="966f0-123">INPUTS</span></span>

### <span data-ttu-id="966f0-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="966f0-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="966f0-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="966f0-125">OUTPUTS</span></span>

### <span data-ttu-id="966f0-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="966f0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="966f0-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="966f0-127">NOTES</span></span>

## <span data-ttu-id="966f0-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="966f0-128">RELATED LINKS</span></span>
