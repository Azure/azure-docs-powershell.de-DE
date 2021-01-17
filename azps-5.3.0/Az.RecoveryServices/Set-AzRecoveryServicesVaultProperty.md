---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468739"
---
# <span data-ttu-id="013d6-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="013d6-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="013d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="013d6-102">SYNOPSIS</span></span>
<span data-ttu-id="013d6-103">Aktualisiert die Eigenschaften eines Tresors.</span><span class="sxs-lookup"><span data-stu-id="013d6-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="013d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="013d6-104">SYNTAX</span></span>

### <span data-ttu-id="013d6-105">AzureRSVaultSoftDelteParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="013d6-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="013d6-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="013d6-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="013d6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="013d6-107">DESCRIPTION</span></span>
<span data-ttu-id="013d6-108">Das **Cmdlet "Set-AzRecoveryServicesVaultProperty"** aktualisiert die Eigenschaften eines Wiederherstellungsdiensttresors.</span><span class="sxs-lookup"><span data-stu-id="013d6-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="013d6-109">Mit diesem Cmdlet können Sie die soft delete-Funktion aktivieren/deaktivieren oder die CMK-Verschlüsselung für einen Tresor mit zwei verschiedenen Parametersätzen festlegen.</span><span class="sxs-lookup"><span data-stu-id="013d6-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="013d6-110">**Die Eigenschaft "SoftDeleteFeatureState"** eines Tresors kann nur deaktiviert werden, wenn im Tresor keine registrierten Container enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="013d6-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="013d6-111">Die InfrastructurEncryption kann nur festgelegt werden, wenn ein Benutzer den CMK-Tresor zum ersten Mal aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="013d6-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="013d6-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="013d6-112">EXAMPLES</span></span>

### <span data-ttu-id="013d6-113">Beispiel 1: Aktualisieren von SoftDeleteFeatureState eines Tresors</span><span class="sxs-lookup"><span data-stu-id="013d6-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="013d6-114">Der erste Befehl ruft ein Tresorobjekt ab und speichert es dann in der $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="013d6-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="013d6-115">Der zweite Befehl aktualisiert die SoftDeleteFeatureState-Eigenschaft des Tresors auf den Zustand "Enabled".</span><span class="sxs-lookup"><span data-stu-id="013d6-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="013d6-116">Beispiel 2: Aktualisieren der CMK-Verschlüsselung eines Tresors</span><span class="sxs-lookup"><span data-stu-id="013d6-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="013d6-117">Das erste Cmdlet ruft "RSVault" zum Aktualisieren der Verschlüsselungseigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="013d6-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="013d6-118">Das zweite Cmdlet ruft den Azure Key Vault ab.</span><span class="sxs-lookup"><span data-stu-id="013d6-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="013d6-119">Das dritte Cmdlet bekommt den Schlüssel aus dem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="013d6-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="013d6-120">Das vierte Cmdlet aktualisiert den vom Kunden verwalteten Verschlüsselungsschlüssel in RSVault.</span><span class="sxs-lookup"><span data-stu-id="013d6-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="013d6-121">Verwenden Sie den Parameter "-InfrastructureEncryption", um die Infrastrukturverschlüsselung zum ersten Update zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="013d6-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="013d6-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="013d6-122">PARAMETERS</span></span>

### <span data-ttu-id="013d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="013d6-123">-DefaultProfile</span></span>
<span data-ttu-id="013d6-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="013d6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="013d6-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="013d6-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="013d6-126">SoftDeleteFeatureState des Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="013d6-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="013d6-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="013d6-127">-EncryptionKeyId</span></span>
<span data-ttu-id="013d6-128">Die Schlüssel-ID des Verschlüsselungsschlüssels, der für CMK verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="013d6-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="013d6-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="013d6-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="013d6-130">Abonnement-ID des Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="013d6-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="013d6-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="013d6-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="013d6-132">Ermöglicht die Infrastrukturverschlüsselung für diesen Tresor.</span><span class="sxs-lookup"><span data-stu-id="013d6-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="013d6-133">Die Infrastrukturverschlüsselung muss beim Konfigurieren der Verschlüsselung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="013d6-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="013d6-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="013d6-134">-VaultId</span></span>
<span data-ttu-id="013d6-135">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="013d6-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="013d6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="013d6-136">-Confirm</span></span>
<span data-ttu-id="013d6-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="013d6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="013d6-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="013d6-138">-WhatIf</span></span>
<span data-ttu-id="013d6-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="013d6-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="013d6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="013d6-140">CommonParameters</span></span>
<span data-ttu-id="013d6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="013d6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="013d6-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="013d6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="013d6-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="013d6-143">INPUTS</span></span>

### <span data-ttu-id="013d6-144">System.String</span><span class="sxs-lookup"><span data-stu-id="013d6-144">System.String</span></span>

### <span data-ttu-id="013d6-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="013d6-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="013d6-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="013d6-146">OUTPUTS</span></span>

### <span data-ttu-id="013d6-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="013d6-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="013d6-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="013d6-148">NOTES</span></span>

## <span data-ttu-id="013d6-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="013d6-149">RELATED LINKS</span></span>

[<span data-ttu-id="013d6-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="013d6-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="013d6-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="013d6-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
