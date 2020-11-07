---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: a0f21fc8cde4c64eaf1e8ea27bf05eff8d664c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659828"
---
# <span data-ttu-id="d82aa-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d82aa-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="d82aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d82aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d82aa-103">Löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="d82aa-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="d82aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d82aa-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d82aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d82aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d82aa-106">Das Cmdlet **Remove-AzRecoveryServicesVault** löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="d82aa-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="d82aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d82aa-107">EXAMPLES</span></span>

### <span data-ttu-id="d82aa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d82aa-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="d82aa-109">Löscht einen Vault für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="d82aa-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="d82aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d82aa-110">PARAMETERS</span></span>

### <span data-ttu-id="d82aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d82aa-111">-DefaultProfile</span></span>
<span data-ttu-id="d82aa-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d82aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d82aa-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="d82aa-113">-Vault</span></span>
<span data-ttu-id="d82aa-114">Gibt ein Azure Site Recovery Vault-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d82aa-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="d82aa-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d82aa-115">-Confirm</span></span>
<span data-ttu-id="d82aa-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d82aa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d82aa-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d82aa-117">-WhatIf</span></span>
<span data-ttu-id="d82aa-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d82aa-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d82aa-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d82aa-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d82aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d82aa-120">CommonParameters</span></span>
<span data-ttu-id="d82aa-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d82aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d82aa-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d82aa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d82aa-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d82aa-123">INPUTS</span></span>

### <span data-ttu-id="d82aa-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d82aa-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d82aa-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d82aa-125">OUTPUTS</span></span>

### <span data-ttu-id="d82aa-126">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="d82aa-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="d82aa-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d82aa-127">NOTES</span></span>

## <span data-ttu-id="d82aa-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d82aa-128">RELATED LINKS</span></span>

[<span data-ttu-id="d82aa-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d82aa-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="d82aa-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d82aa-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="d82aa-131">Neu – AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d82aa-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


