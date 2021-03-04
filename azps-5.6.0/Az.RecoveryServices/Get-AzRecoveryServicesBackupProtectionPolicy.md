---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c29ff9d1fbe4a34f17a491dd1cb3c86c16f3ce75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921648"
---
# <span data-ttu-id="c59e2-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c59e2-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="c59e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c59e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c59e2-103">Ruft Sicherungsschutzrichtlinien für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="c59e2-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="c59e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c59e2-104">SYNTAX</span></span>

### <span data-ttu-id="c59e2-105">NoParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c59e2-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c59e2-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="c59e2-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c59e2-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="c59e2-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c59e2-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="c59e2-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c59e2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c59e2-109">DESCRIPTION</span></span>
<span data-ttu-id="c59e2-110">Das **Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet** ruft Azure-Sicherungsschutzrichtlinien für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="c59e2-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="c59e2-111">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="c59e2-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c59e2-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c59e2-112">EXAMPLES</span></span>

### <span data-ttu-id="c59e2-113">Beispiel 1: Alle Richtlinien im Tresor erhalten</span><span class="sxs-lookup"><span data-stu-id="c59e2-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="c59e2-114">Dieser Befehl ruft alle im Tresor erstellten Schutzrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="c59e2-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="c59e2-115">Beispiel 2: Erhalten einer bestimmten Richtlinie</span><span class="sxs-lookup"><span data-stu-id="c59e2-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="c59e2-116">Dieser Befehl ruft die Schutzrichtlinie "DefaultPolicy" ab und speichert sie dann in der $Pol-Variable.</span><span class="sxs-lookup"><span data-stu-id="c59e2-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="c59e2-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c59e2-117">PARAMETERS</span></span>

### <span data-ttu-id="c59e2-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="c59e2-118">-BackupManagementType</span></span>
<span data-ttu-id="c59e2-119">Die Klasse der zu schützenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c59e2-119">The class of resources being protected.</span></span> <span data-ttu-id="c59e2-120">Derzeit werden für dieses Cmdlet AzureVM, AzureStorage, AzureWorkload unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c59e2-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59e2-121">-DefaultProfile</span></span>
<span data-ttu-id="c59e2-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c59e2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c59e2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c59e2-123">-Name</span></span>
<span data-ttu-id="c59e2-124">Gibt den Namen der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="c59e2-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59e2-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c59e2-125">-VaultId</span></span>
<span data-ttu-id="c59e2-126">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="c59e2-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c59e2-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c59e2-127">-WorkloadType</span></span>
<span data-ttu-id="c59e2-128">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c59e2-128">Workload type of the resource.</span></span> <span data-ttu-id="c59e2-129">Die aktuellen unterstützten Werte sind AzureVM, AzureFiles, MSSQL.</span><span class="sxs-lookup"><span data-stu-id="c59e2-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59e2-130">CommonParameters</span></span>
<span data-ttu-id="c59e2-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59e2-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c59e2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59e2-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c59e2-133">INPUTS</span></span>

### <span data-ttu-id="c59e2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c59e2-134">System.String</span></span>

## <span data-ttu-id="c59e2-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c59e2-135">OUTPUTS</span></span>

### <span data-ttu-id="c59e2-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="c59e2-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="c59e2-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c59e2-137">NOTES</span></span>

## <span data-ttu-id="c59e2-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c59e2-138">RELATED LINKS</span></span>

[<span data-ttu-id="c59e2-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c59e2-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="c59e2-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c59e2-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="c59e2-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c59e2-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


