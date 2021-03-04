---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 6863c1c8b486784339cf0e1a52cc0793c0cc31f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944765"
---
# <span data-ttu-id="98663-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="98663-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="98663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98663-102">SYNOPSIS</span></span>
<span data-ttu-id="98663-103">Erstellt ein Datenträgerzuordnungsobjekt für virtuelle Azure-Computerlaufwerke, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98663-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="98663-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98663-104">SYNTAX</span></span>

### <span data-ttu-id="98663-105">AzureToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="98663-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98663-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="98663-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98663-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98663-107">DESCRIPTION</span></span>
<span data-ttu-id="98663-108">Erstellt ein Datenträgerzuordnungsobjekt, mit dem ein virtueller Azure-Computerdatenträger dem Cachespeicherkonto und dem Zielspeicherkonto (Wiederherstellungsregion) zugeordnet wird, das zum Replizieren des Datenträgers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98663-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="98663-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98663-109">EXAMPLES</span></span>

### <span data-ttu-id="98663-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98663-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="98663-111">Erstellen Sie ein Datenträgerzuordnungsobjekt für virtuelle Azure-Computerlaufwerke, die repliziert werden sollen. Wird während des Azure-EnableDr-Vorgangs und des erneuten Schutzvorgangs verwendet.</span><span class="sxs-lookup"><span data-stu-id="98663-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="98663-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="98663-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="98663-113">Erstellen Sie ein verwaltetes Datenträgerzuordnungsobjekt für virtuelle Azure-Computerlaufwerke, die repliziert werden sollen. Wird während des Azure-EnableDr-Vorgangs und des erneuten Schutzvorgangs verwendet.</span><span class="sxs-lookup"><span data-stu-id="98663-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="98663-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="98663-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="98663-115">Erstellen Sie ein verwaltetes Datenträgerzuordnungsobjekt mit Einstellungen für die One-Pass-Verschlüsselung für virtuelle Azure-Computerlaufwerke, die repliziert werden sollen. Wird während des Azure-EnableDr-Vorgangs und des erneuten Schutzvorgangs verwendet.</span><span class="sxs-lookup"><span data-stu-id="98663-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="98663-116">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="98663-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="98663-117">Erstellen Sie ein verwaltetes Datenträgerzuordnungsobjekt mit der Zieldatenträgerverschlüsselungssatz-ID, damit virtuelle Azure-Computerlaufwerke repliziert werden. Wird während des Azure-EnableDr-Vorgangs und des erneuten Schutzvorgangs verwendet.</span><span class="sxs-lookup"><span data-stu-id="98663-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="98663-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98663-118">PARAMETERS</span></span>

### <span data-ttu-id="98663-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98663-119">-DefaultProfile</span></span>
<span data-ttu-id="98663-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98663-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98663-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="98663-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="98663-122">Gibt die geheime Url der Datenträgerverschlüsselung an.</span><span class="sxs-lookup"><span data-stu-id="98663-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="98663-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="98663-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="98663-124">Gibt den Datenträgerverschlüsselungsschlüsseltresor ARM id an.</span><span class="sxs-lookup"><span data-stu-id="98663-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="98663-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="98663-125">-DiskId</span></span>
<span data-ttu-id="98663-126">Gibt die Datenträger-ID des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="98663-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="98663-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="98663-127">-FailoverDiskName</span></span>
<span data-ttu-id="98663-128">Gibt den Namen des Datenträgers an, der während des Failovers erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="98663-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="98663-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="98663-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="98663-130">Gibt die Schlüsselverschlüsselungs-URL an.</span><span class="sxs-lookup"><span data-stu-id="98663-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="98663-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="98663-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="98663-132">Gibt den Schlüsselverschlüsselungsschlüsseltresor ARM id an.</span><span class="sxs-lookup"><span data-stu-id="98663-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="98663-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="98663-133">-LogStorageAccountId</span></span>
<span data-ttu-id="98663-134">Gibt die Log- oder Cachespeicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98663-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="98663-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="98663-135">-ManagedDisk</span></span>
<span data-ttu-id="98663-136">Gibt an, dass die Eingabe für verwalteten Datenträger bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="98663-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="98663-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="98663-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="98663-138">Gibt die ID des Azure-Speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="98663-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="98663-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="98663-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="98663-140">Gibt die ID der Azure-Datenträgerverschlüsselung an, die für Wiederherstellungslaufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98663-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="98663-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="98663-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="98663-142">Gibt den Kontotyp des replizierten verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="98663-142">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="98663-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="98663-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="98663-144">Gibt die Wiederherstellungsressourcengruppen-ID für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="98663-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="98663-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="98663-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="98663-146">Gibt den Wiederherstellungszieldatenträger für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="98663-146">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="98663-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="98663-147">-TfoDiskName</span></span>
<span data-ttu-id="98663-148">Gibt den Namen des Datenträgers an, der während des Test failover erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="98663-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="98663-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="98663-149">-VhdUri</span></span>
<span data-ttu-id="98663-150">Geben Sie den VHD-URI des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="98663-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="98663-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98663-151">-Confirm</span></span>
<span data-ttu-id="98663-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98663-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98663-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98663-153">-WhatIf</span></span>
<span data-ttu-id="98663-154">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98663-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98663-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98663-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98663-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98663-156">CommonParameters</span></span>
<span data-ttu-id="98663-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98663-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98663-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98663-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98663-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98663-159">INPUTS</span></span>

### <span data-ttu-id="98663-160">Keine</span><span class="sxs-lookup"><span data-stu-id="98663-160">None</span></span>

## <span data-ttu-id="98663-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98663-161">OUTPUTS</span></span>

### <span data-ttu-id="98663-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="98663-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="98663-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="98663-163">NOTES</span></span>

## <span data-ttu-id="98663-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="98663-164">RELATED LINKS</span></span>
