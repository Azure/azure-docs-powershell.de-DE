---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 19ba256176c47b5841b9d124d186f376f0ecce7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662311"
---
# <span data-ttu-id="9b32d-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="9b32d-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="9b32d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b32d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b32d-103">Erstellt ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b32d-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b32d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b32d-104">SYNTAX</span></span>

### <span data-ttu-id="9b32d-105">AzureToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b32d-105">AzureToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b32d-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9b32d-106">AzureToAzureManagedDisk</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b32d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b32d-107">DESCRIPTION</span></span>
<span data-ttu-id="9b32d-108">Erstellt ein Datenträger Zuordnungsobjekt, das einen Azure Virtual Machine-Datenträger dem Cachespeicher Konto und dem Zielspeicher Konto (Wiederherstellungsbereich) zuordnet, das zum Replizieren des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b32d-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="9b32d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b32d-109">EXAMPLES</span></span>

### <span data-ttu-id="9b32d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b32d-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="9b32d-111">Erstellen Sie ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen. Wird während Azure zu Azure enabledr verwendet, und der Vorgang wird erneut geschützt.</span><span class="sxs-lookup"><span data-stu-id="9b32d-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="9b32d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b32d-112">PARAMETERS</span></span>

### <span data-ttu-id="9b32d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b32d-113">-DefaultProfile</span></span>
<span data-ttu-id="9b32d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b32d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b32d-115">-Datenträger-Nr</span><span class="sxs-lookup"><span data-stu-id="9b32d-115">-DiskId</span></span>
<span data-ttu-id="9b32d-116">Gibt die Datenträger-ID des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="9b32d-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="9b32d-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9b32d-117">-LogStorageAccountId</span></span>
<span data-ttu-id="9b32d-118">Gibt die Protokoll-oder Cache-Speicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b32d-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="9b32d-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9b32d-119">-ManagedDisk</span></span>
<span data-ttu-id="9b32d-120">Gibt an, dass die Eingabe für verwalteten Datenträger festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9b32d-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="9b32d-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9b32d-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="9b32d-122">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b32d-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="9b32d-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="9b32d-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="9b32d-124">Gibt den Kontotyp des replizierten verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="9b32d-124">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="9b32d-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="9b32d-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="9b32d-126">Gibt die ID der Wiederherstellungsressourcen Gruppe für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="9b32d-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="9b32d-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="9b32d-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="9b32d-128">Gibt den Wiederherstellungsziel Datenträger für replizierten verwalteten Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="9b32d-128">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="9b32d-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="9b32d-129">-VhdUri</span></span>
<span data-ttu-id="9b32d-130">Geben Sie den VHD-URI des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="9b32d-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="9b32d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b32d-131">-Confirm</span></span>
<span data-ttu-id="9b32d-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b32d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b32d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b32d-133">-WhatIf</span></span>
<span data-ttu-id="9b32d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b32d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b32d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b32d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b32d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b32d-136">CommonParameters</span></span>
<span data-ttu-id="9b32d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b32d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b32d-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b32d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b32d-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b32d-139">INPUTS</span></span>

### <span data-ttu-id="9b32d-140">Keine</span><span class="sxs-lookup"><span data-stu-id="9b32d-140">None</span></span>

## <span data-ttu-id="9b32d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b32d-141">OUTPUTS</span></span>

### <span data-ttu-id="9b32d-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="9b32d-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="9b32d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b32d-143">NOTES</span></span>

## <span data-ttu-id="9b32d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b32d-144">RELATED LINKS</span></span>
