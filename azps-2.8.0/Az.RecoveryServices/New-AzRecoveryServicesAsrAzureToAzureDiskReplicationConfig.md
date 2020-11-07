---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824288"
---
# <span data-ttu-id="d0423-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="d0423-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="d0423-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0423-102">SYNOPSIS</span></span>
<span data-ttu-id="d0423-103">Erstellt ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0423-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="d0423-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0423-104">SYNTAX</span></span>

### <span data-ttu-id="d0423-105">AzureToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0423-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0423-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d0423-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0423-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0423-107">DESCRIPTION</span></span>
<span data-ttu-id="d0423-108">Erstellt ein Datenträger Zuordnungsobjekt, das einen Azure Virtual Machine-Datenträger dem Cachespeicher Konto und dem Zielspeicher Konto (Wiederherstellungsbereich) zuordnet, das zum Replizieren des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0423-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="d0423-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0423-109">EXAMPLES</span></span>

### <span data-ttu-id="d0423-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0423-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="d0423-111">Erstellen Sie ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen. Wird während Azure zu Azure enabledr verwendet, und der Vorgang wird erneut geschützt.</span><span class="sxs-lookup"><span data-stu-id="d0423-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="d0423-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0423-112">PARAMETERS</span></span>

### <span data-ttu-id="d0423-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0423-113">-DefaultProfile</span></span>
<span data-ttu-id="d0423-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0423-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0423-115">-Datenträger-Nr</span><span class="sxs-lookup"><span data-stu-id="d0423-115">-DiskId</span></span>
<span data-ttu-id="d0423-116">Gibt die Datenträger-ID des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d0423-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="d0423-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d0423-117">-LogStorageAccountId</span></span>
<span data-ttu-id="d0423-118">Gibt die Protokoll-oder Cache-Speicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0423-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="d0423-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d0423-119">-ManagedDisk</span></span>
<span data-ttu-id="d0423-120">Gibt an, dass die Eingabe für verwalteten Datenträger festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d0423-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="d0423-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d0423-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d0423-122">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0423-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="d0423-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="d0423-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="d0423-124">Gibt den Kontotyp des replizierten verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d0423-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0423-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d0423-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="d0423-126">Gibt die ID der Wiederherstellungsressourcen Gruppe für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="d0423-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="d0423-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="d0423-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="d0423-128">Gibt den Wiederherstellungsziel Datenträger für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="d0423-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0423-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="d0423-129">-VhdUri</span></span>
<span data-ttu-id="d0423-130">Geben Sie den VHD-URI des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="d0423-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="d0423-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0423-131">-Confirm</span></span>
<span data-ttu-id="d0423-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0423-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0423-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0423-133">-WhatIf</span></span>
<span data-ttu-id="d0423-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0423-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0423-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0423-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0423-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0423-136">CommonParameters</span></span>
<span data-ttu-id="d0423-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0423-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0423-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0423-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0423-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0423-139">INPUTS</span></span>

### <span data-ttu-id="d0423-140">Keine</span><span class="sxs-lookup"><span data-stu-id="d0423-140">None</span></span>

## <span data-ttu-id="d0423-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0423-141">OUTPUTS</span></span>

### <span data-ttu-id="d0423-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="d0423-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="d0423-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0423-143">NOTES</span></span>

## <span data-ttu-id="d0423-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0423-144">RELATED LINKS</span></span>
