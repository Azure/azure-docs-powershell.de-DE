---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008989"
---
# <span data-ttu-id="f4700-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="f4700-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="f4700-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4700-102">SYNOPSIS</span></span>
<span data-ttu-id="f4700-103">Erstellt ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f4700-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="f4700-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4700-104">SYNTAX</span></span>

### <span data-ttu-id="f4700-105">AzureToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4700-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4700-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f4700-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4700-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4700-107">DESCRIPTION</span></span>
<span data-ttu-id="f4700-108">Erstellt ein Datenträger Zuordnungsobjekt, das einen Azure Virtual Machine-Datenträger dem Cachespeicher Konto und dem Zielspeicher Konto (Wiederherstellungsbereich) zuordnet, das zum Replizieren des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4700-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="f4700-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4700-109">EXAMPLES</span></span>

### <span data-ttu-id="f4700-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4700-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="f4700-111">Erstellen Sie ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen. Wird während Azure zu Azure enabledr verwendet, und der Vorgang wird erneut geschützt.</span><span class="sxs-lookup"><span data-stu-id="f4700-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="f4700-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f4700-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="f4700-113">Erstellen Sie ein verwaltetes Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen. Wird während Azure zu Azure enabledr verwendet, und der Vorgang wird erneut geschützt.</span><span class="sxs-lookup"><span data-stu-id="f4700-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="f4700-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f4700-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="f4700-115">Erstellen Sie ein verwaltetes Datenträger Zuordnungsobjekt mit einem Pass-Verschlüsselungseinstellungen für Azure Virtual Machine-Datenträger, die repliziert werden sollen. Wird während Azure zu Azure enabledr verwendet, und der Vorgang wird erneut geschützt.</span><span class="sxs-lookup"><span data-stu-id="f4700-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="f4700-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f4700-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="f4700-117">Erstellen Sie ein verwaltetes Datenträger Zuordnungsobjekt mit der Zielfestplatten Verschlüsselungs Satz-ID, damit Azure Virtual Machine-Datenträger repliziert werden. Wird während Azure zu Azure enabledr verwendet, und der Vorgang wird erneut geschützt.</span><span class="sxs-lookup"><span data-stu-id="f4700-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="f4700-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4700-118">PARAMETERS</span></span>

### <span data-ttu-id="f4700-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4700-119">-DefaultProfile</span></span>
<span data-ttu-id="f4700-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4700-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4700-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="f4700-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="f4700-122">Gibt die geheim-URL für die Datenträgerverschlüsselung an.</span><span class="sxs-lookup"><span data-stu-id="f4700-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f4700-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="f4700-124">Gibt die Vault Arm-ID des Datenträger Verschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="f4700-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-125">-Datenträger-Nr</span><span class="sxs-lookup"><span data-stu-id="f4700-125">-DiskId</span></span>
<span data-ttu-id="f4700-126">Gibt die Datenträger-ID des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f4700-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="f4700-127">-FailoverDiskName</span></span>
<span data-ttu-id="f4700-128">Gibt den Namen des Datenträgers an, der während des Failovers erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f4700-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="f4700-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="f4700-130">Gibt die Schlüssel Verschlüsselungs-URL an.</span><span class="sxs-lookup"><span data-stu-id="f4700-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="f4700-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="f4700-132">Gibt die Schlüssel-Verschlüsselungsschlüssel-ID an.</span><span class="sxs-lookup"><span data-stu-id="f4700-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f4700-133">-LogStorageAccountId</span></span>
<span data-ttu-id="f4700-134">Gibt die Protokoll-oder Cache-Speicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4700-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f4700-135">-ManagedDisk</span></span>
<span data-ttu-id="f4700-136">Gibt an, dass die Eingabe für verwalteten Datenträger festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f4700-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f4700-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f4700-138">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4700-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="f4700-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="f4700-140">Gibt die ID des Azure Disk Encryption-Satzes an, der für Wiederherstellungsdatenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4700-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="f4700-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="f4700-142">Gibt den Kontotyp des replizierten verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f4700-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="f4700-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="f4700-144">Gibt die ID der Wiederherstellungsressourcen Gruppe für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="f4700-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="f4700-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="f4700-146">Gibt den Wiederherstellungsziel Datenträger für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="f4700-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="f4700-147">-TfoDiskName</span></span>
<span data-ttu-id="f4700-148">Gibt den Namen des Datenträgers an, der während des Test Failovers erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f4700-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="f4700-149">-VhdUri</span></span>
<span data-ttu-id="f4700-150">Geben Sie den VHD-URI des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="f4700-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4700-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4700-151">-Confirm</span></span>
<span data-ttu-id="f4700-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4700-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4700-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4700-153">-WhatIf</span></span>
<span data-ttu-id="f4700-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4700-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4700-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4700-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4700-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4700-156">CommonParameters</span></span>
<span data-ttu-id="f4700-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4700-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4700-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4700-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4700-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4700-159">INPUTS</span></span>

### <span data-ttu-id="f4700-160">Keine</span><span class="sxs-lookup"><span data-stu-id="f4700-160">None</span></span>

## <span data-ttu-id="f4700-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4700-161">OUTPUTS</span></span>

### <span data-ttu-id="f4700-162">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="f4700-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="f4700-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4700-163">NOTES</span></span>

## <span data-ttu-id="f4700-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4700-164">RELATED LINKS</span></span>
