---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479930"
---
# <span data-ttu-id="8ebd1-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="8ebd1-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="8ebd1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ebd1-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebd1-103">Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="8ebd1-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ebd1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ebd1-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ebd1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ebd1-105">DESCRIPTION</span></span>
<span data-ttu-id="8ebd1-106">Das Cmdlet **Restore-AzureRmBackupItem** stellt die Daten und die Konfiguration für ein Azure Backup-Element an einem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="8ebd1-107">Mit diesem Cmdlet wird die Wiederherstellung aus dem Sicherungs Depot in Ihrem Konto gestartet.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="8ebd1-108">Beim Wiederherstellungsvorgang wird der vollständige virtuelle Computer nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="8ebd1-109">Die Datenträgerdaten und Konfigurationsinformationen werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="8ebd1-110">Nach Abschluss des Wiederherstellungsvorgangs müssen Sie den virtuellen Computer erstellen und starten.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="8ebd1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ebd1-111">EXAMPLES</span></span>

### <span data-ttu-id="8ebd1-112">Beispiel 1: Wiederherstellen einer virtuellen Maschine auf einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="8ebd1-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="8ebd1-113">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="8ebd1-114">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="8ebd1-115">Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupContainer** einen Container mit dem angegebenen Namen im Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="8ebd1-116">Der Befehl speichert das Objekt in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="8ebd1-117">Der dritte Befehl ruft das Sicherungselement im Container in $Container mit dem Cmdlet **Get-AzureRmBackupItem** ab.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="8ebd1-118">Der Befehl speichert das Objekt in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="8ebd1-119">Der vierte Befehl ruft den Wiederherstellungspunkt für das Element in $BackupItem ab.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="8ebd1-120">Der Befehl speichert das Objekt in der $RecoveryPoint Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="8ebd1-121">Der endgültige Befehl stellt den Wiederherstellungspunkt in $RecoveryPoint für das Konto mit dem Namen DestinationAccount wieder her.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="8ebd1-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ebd1-122">PARAMETERS</span></span>

### <span data-ttu-id="8ebd1-123">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8ebd1-123">-RecoveryPoint</span></span>
<span data-ttu-id="8ebd1-124">Gibt den Wiederherstellungspunkt an, auf den der virtuelle Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-124">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="8ebd1-125">Verwenden Sie zum Abrufen eines **AzureRmBackupRecoveryPoint** das Get-AzureRmBackupRecoveryPoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-125">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebd1-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8ebd1-126">-StorageAccountName</span></span>
<span data-ttu-id="8ebd1-127">Gibt den Namen des Zielspeicher Kontos in Ihrem Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-127">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="8ebd1-128">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-128">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebd1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebd1-129">-DefaultProfile</span></span>
<span data-ttu-id="8ebd1-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ebd1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebd1-131">CommonParameters</span></span>
<span data-ttu-id="8ebd1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebd1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebd1-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebd1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebd1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ebd1-134">INPUTS</span></span>

### <span data-ttu-id="8ebd1-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8ebd1-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="8ebd1-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ebd1-136">OUTPUTS</span></span>

### <span data-ttu-id="8ebd1-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8ebd1-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="8ebd1-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ebd1-138">NOTES</span></span>

## <span data-ttu-id="8ebd1-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ebd1-139">RELATED LINKS</span></span>

[<span data-ttu-id="8ebd1-140">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="8ebd1-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="8ebd1-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="8ebd1-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="8ebd1-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8ebd1-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


