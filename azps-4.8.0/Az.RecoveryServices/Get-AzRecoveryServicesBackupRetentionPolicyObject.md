---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173567"
---
# <span data-ttu-id="df544-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="df544-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="df544-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df544-102">SYNOPSIS</span></span>
<span data-ttu-id="df544-103">Ruft ein Basis Aufbewahrungsrichtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="df544-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="df544-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df544-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df544-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df544-105">DESCRIPTION</span></span>
<span data-ttu-id="df544-106">Das Cmdlet " **Get-AzRecoveryServicesBackupRetentionPolicyObject** " Ruft eine Basis- **AzureRMRecoveryServicesRetentionPolicyObject** ab.</span><span class="sxs-lookup"><span data-stu-id="df544-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="df544-107">Dieses Objekt wird im System nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="df544-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="df544-108">Es handelt sich um ein temporäres Objekt, das Sie mit dem New-AzRecoveryServicesBackupProtectionPolicy-Cmdlet bearbeiten und verwenden können, um eine neue Sicherungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df544-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="df544-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df544-109">EXAMPLES</span></span>

### <span data-ttu-id="df544-110">Beispiel 1: Erstellen einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="df544-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="df544-111">Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="df544-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="df544-112">Der zweite Befehl legt die Dauer für das Aufbewahrungsrichtlinienobjekt auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="df544-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="df544-113">Der dritte Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="df544-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="df544-114">Mit dem letzten Befehl wird eine Sicherungsschutz Richtlinie mithilfe der Aufbewahrungsrichtlinie und der mit den vorherigen Befehlen erstellten Zeitplan-Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="df544-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="df544-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="df544-115">PARAMETERS</span></span>

### <span data-ttu-id="df544-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="df544-116">-BackupManagementType</span></span>
<span data-ttu-id="df544-117">Die Klasse der Ressourcen, die geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="df544-117">The class of resources being protected.</span></span> <span data-ttu-id="df544-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="df544-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df544-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="df544-119">AzureVM</span></span> 
- <span data-ttu-id="df544-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="df544-120">AzureWorkload</span></span>
- <span data-ttu-id="df544-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="df544-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df544-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df544-122">-DefaultProfile</span></span>
<span data-ttu-id="df544-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df544-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df544-124">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="df544-124">-WorkloadType</span></span>
<span data-ttu-id="df544-125">Arbeits Auslastungs der Ressource.</span><span class="sxs-lookup"><span data-stu-id="df544-125">Workload type of the resource.</span></span> <span data-ttu-id="df544-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="df544-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df544-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="df544-127">AzureVM</span></span> 
- <span data-ttu-id="df544-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="df544-128">AzureFiles</span></span>
- <span data-ttu-id="df544-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="df544-129">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df544-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df544-130">CommonParameters</span></span>
<span data-ttu-id="df544-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df544-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df544-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df544-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df544-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df544-133">INPUTS</span></span>

### <span data-ttu-id="df544-134">Keine</span><span class="sxs-lookup"><span data-stu-id="df544-134">None</span></span>

## <span data-ttu-id="df544-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df544-135">OUTPUTS</span></span>

### <span data-ttu-id="df544-136">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="df544-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="df544-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="df544-137">NOTES</span></span>

## <span data-ttu-id="df544-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df544-138">RELATED LINKS</span></span>

[<span data-ttu-id="df544-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="df544-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="df544-140">Neu – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="df544-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


