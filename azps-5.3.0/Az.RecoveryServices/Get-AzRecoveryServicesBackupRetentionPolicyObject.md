---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470071"
---
# <span data-ttu-id="55baa-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="55baa-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="55baa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55baa-102">SYNOPSIS</span></span>
<span data-ttu-id="55baa-103">Ruft ein Basisobjekt für die Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="55baa-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="55baa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55baa-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55baa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55baa-105">DESCRIPTION</span></span>
<span data-ttu-id="55baa-106">Das **Cmdlet "Get-AzRecoveryServicesBackupRetentionPolicyObject"** ruft eine **AzureRMRecoveryServicesRetentionPolicyObject-Basis ab.**</span><span class="sxs-lookup"><span data-stu-id="55baa-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="55baa-107">Dieses Objekt wird nicht im System beibehalten.</span><span class="sxs-lookup"><span data-stu-id="55baa-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="55baa-108">Es ist ein temporäres Objekt, das Sie bearbeiten und mit dem New-AzRecoveryServicesBackupProtectionPolicy verwenden können, um eine neue Sicherungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="55baa-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="55baa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55baa-109">EXAMPLES</span></span>

### <span data-ttu-id="55baa-110">Beispiel 1: Erstellen einer Sicherungsschutzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="55baa-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="55baa-111">Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variable.</span><span class="sxs-lookup"><span data-stu-id="55baa-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="55baa-112">Der zweite Befehl legt die Dauer für das Aufbewahrungsrichtlinienobjekt auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="55baa-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="55baa-113">Der dritte Befehl ruft das Zeitplanrichtlinienobjekt ab und speichert es dann in der $SchPol Variable.</span><span class="sxs-lookup"><span data-stu-id="55baa-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="55baa-114">Der letzte Befehl erstellt mithilfe der Aufbewahrungs- und Zeitplanrichtlinie, die mit den vorherigen Befehlen erstellt wurde, eine Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="55baa-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="55baa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55baa-115">PARAMETERS</span></span>

### <span data-ttu-id="55baa-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="55baa-116">-BackupManagementType</span></span>
<span data-ttu-id="55baa-117">Die Klasse der geschützten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="55baa-117">The class of resources being protected.</span></span> <span data-ttu-id="55baa-118">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="55baa-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55baa-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="55baa-119">AzureVM</span></span> 
- <span data-ttu-id="55baa-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="55baa-120">AzureWorkload</span></span>
- <span data-ttu-id="55baa-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="55baa-121">AzureStorage</span></span>

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

### <span data-ttu-id="55baa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55baa-122">-DefaultProfile</span></span>
<span data-ttu-id="55baa-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55baa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55baa-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="55baa-124">-WorkloadType</span></span>
<span data-ttu-id="55baa-125">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="55baa-125">Workload type of the resource.</span></span> <span data-ttu-id="55baa-126">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="55baa-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55baa-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="55baa-127">AzureVM</span></span> 
- <span data-ttu-id="55baa-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="55baa-128">AzureFiles</span></span>
- <span data-ttu-id="55baa-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="55baa-129">MSSQL</span></span>

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

### <span data-ttu-id="55baa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55baa-130">CommonParameters</span></span>
<span data-ttu-id="55baa-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55baa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55baa-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55baa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55baa-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55baa-133">INPUTS</span></span>

### <span data-ttu-id="55baa-134">Keine</span><span class="sxs-lookup"><span data-stu-id="55baa-134">None</span></span>

## <span data-ttu-id="55baa-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55baa-135">OUTPUTS</span></span>

### <span data-ttu-id="55baa-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="55baa-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="55baa-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55baa-137">NOTES</span></span>

## <span data-ttu-id="55baa-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55baa-138">RELATED LINKS</span></span>

[<span data-ttu-id="55baa-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="55baa-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="55baa-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="55baa-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)


