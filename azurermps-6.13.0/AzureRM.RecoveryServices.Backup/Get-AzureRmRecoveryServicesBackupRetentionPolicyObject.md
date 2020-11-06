---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83eeeec861452407dae1a9d92e5bc900b98d6512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498197"
---
# <span data-ttu-id="95f86-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="95f86-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="95f86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95f86-102">SYNOPSIS</span></span>
<span data-ttu-id="95f86-103">Ruft ein Basis Aufbewahrungsrichtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="95f86-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f86-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95f86-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95f86-105">DESCRIPTION</span></span>
<span data-ttu-id="95f86-106">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** " Ruft eine Basis- **AzureRMRecoveryServicesRetentionPolicyObject** ab.</span><span class="sxs-lookup"><span data-stu-id="95f86-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="95f86-107">Dieses Objekt wird im System nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="95f86-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="95f86-108">Es handelt sich um ein temporäres Objekt, das Sie mit dem New-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet bearbeiten und verwenden können, um eine neue Sicherungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="95f86-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="95f86-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95f86-109">EXAMPLES</span></span>

### <span data-ttu-id="95f86-110">Beispiel 1: Erstellen einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="95f86-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="95f86-111">Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="95f86-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="95f86-112">Der zweite Befehl legt die Dauer für das Aufbewahrungsrichtlinienobjekt auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="95f86-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="95f86-113">Der dritte Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="95f86-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="95f86-114">Mit dem letzten Befehl wird eine Sicherungsschutz Richtlinie mithilfe der Aufbewahrungsrichtlinie und der mit den vorherigen Befehlen erstellten Zeitplan-Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="95f86-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="95f86-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="95f86-115">PARAMETERS</span></span>

### <span data-ttu-id="95f86-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="95f86-116">-BackupManagementType</span></span>
<span data-ttu-id="95f86-117">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="95f86-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="95f86-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="95f86-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95f86-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="95f86-119">AzureVM</span></span> 
- <span data-ttu-id="95f86-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="95f86-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="95f86-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="95f86-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f86-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f86-122">-DefaultProfile</span></span>
<span data-ttu-id="95f86-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95f86-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f86-124">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="95f86-124">-WorkloadType</span></span>
<span data-ttu-id="95f86-125">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="95f86-125">Specifies the workload type.</span></span>
<span data-ttu-id="95f86-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="95f86-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95f86-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="95f86-127">AzureVM</span></span> 
- <span data-ttu-id="95f86-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="95f86-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="95f86-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="95f86-129">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f86-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f86-130">CommonParameters</span></span>
<span data-ttu-id="95f86-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f86-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f86-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f86-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f86-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95f86-133">INPUTS</span></span>

### <span data-ttu-id="95f86-134">Keine</span><span class="sxs-lookup"><span data-stu-id="95f86-134">None</span></span>

## <span data-ttu-id="95f86-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95f86-135">OUTPUTS</span></span>

### <span data-ttu-id="95f86-136">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="95f86-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="95f86-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="95f86-137">NOTES</span></span>

## <span data-ttu-id="95f86-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95f86-138">RELATED LINKS</span></span>

[<span data-ttu-id="95f86-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="95f86-139">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="95f86-140">Neu – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="95f86-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


