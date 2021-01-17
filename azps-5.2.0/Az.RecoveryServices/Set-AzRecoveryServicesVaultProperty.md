---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371284"
---
# <span data-ttu-id="59735-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="59735-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="59735-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59735-102">SYNOPSIS</span></span>
<span data-ttu-id="59735-103">Aktualisiert die Eigenschaften eines Tresors.</span><span class="sxs-lookup"><span data-stu-id="59735-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="59735-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59735-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59735-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59735-105">DESCRIPTION</span></span>
<span data-ttu-id="59735-106">Das **Cmdlet "Set-AzRecoveryServicesVaultProperty"** aktualisiert die Eigenschaften eines Wiederherstellungsdiensttresors.</span><span class="sxs-lookup"><span data-stu-id="59735-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="59735-107">Dieses Cmdlet gibt die aktualisierten Tresoreigenschaften nach dem aktuellen Set-Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="59735-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="59735-108">Die Verwendung dieser Cmdlet-Eigenschaften des Tresors, z. B. soft-delete, kann jederzeit aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="59735-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="59735-109">**Die Eigenschaft "SoftDeleteFeatureState"** eines Tresors kann nur deaktiviert werden, wenn sich im Tresor keine registrierten Container befinden.</span><span class="sxs-lookup"><span data-stu-id="59735-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="59735-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59735-110">EXAMPLES</span></span>

### <span data-ttu-id="59735-111">Beispiel 1: Aktualisieren von SoftDeleteFeatureState eines Tresors</span><span class="sxs-lookup"><span data-stu-id="59735-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="59735-112">Der erste Befehl ruft ein Tresorobjekt ab und speichert es dann in der $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="59735-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="59735-113">Mit dem zweiten Befehl wird die Eigenschaft "SoftDeleteFeatureState" des Tresors auf den Zustand "Enabled" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="59735-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="59735-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59735-114">PARAMETERS</span></span>

### <span data-ttu-id="59735-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59735-115">-DefaultProfile</span></span>
<span data-ttu-id="59735-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59735-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59735-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="59735-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="59735-118">SoftDeleteFeatureState des Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="59735-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59735-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="59735-119">-VaultId</span></span>
<span data-ttu-id="59735-120">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="59735-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59735-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59735-121">-Confirm</span></span>
<span data-ttu-id="59735-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59735-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59735-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="59735-123">-WhatIf</span></span>
<span data-ttu-id="59735-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59735-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="59735-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59735-125">CommonParameters</span></span>
<span data-ttu-id="59735-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59735-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59735-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59735-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59735-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59735-128">INPUTS</span></span>

### <span data-ttu-id="59735-129">System.String</span><span class="sxs-lookup"><span data-stu-id="59735-129">System.String</span></span>

### <span data-ttu-id="59735-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="59735-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="59735-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59735-131">OUTPUTS</span></span>

### <span data-ttu-id="59735-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="59735-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="59735-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59735-133">NOTES</span></span>

## <span data-ttu-id="59735-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59735-134">RELATED LINKS</span></span>

[<span data-ttu-id="59735-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="59735-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="59735-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="59735-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


