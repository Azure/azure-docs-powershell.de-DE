---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376647"
---
# <span data-ttu-id="1f621-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f621-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1f621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f621-102">SYNOPSIS</span></span>
<span data-ttu-id="1f621-103">Ruft Sicherungsschutzrichtlinien für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="1f621-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="1f621-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f621-104">SYNTAX</span></span>

### <span data-ttu-id="1f621-105">NoParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f621-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f621-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="1f621-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f621-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="1f621-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f621-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="1f621-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f621-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f621-109">DESCRIPTION</span></span>
<span data-ttu-id="1f621-110">Das **Cmdlet "Get-AzRecoveryServicesBackupProtectionPolicy"** ruft Azure Backup Protection Policies für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="1f621-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="1f621-111">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f621-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1f621-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1f621-112">EXAMPLES</span></span>

### <span data-ttu-id="1f621-113">Beispiel 1: Alle Richtlinien im Tresor erhalten</span><span class="sxs-lookup"><span data-stu-id="1f621-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="1f621-114">Dieser Befehl ruft alle im Tresor erstellten Schutzrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="1f621-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="1f621-115">Beispiel 2: Erhalten einer bestimmten Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1f621-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="1f621-116">Dieser Befehl ruft die Schutzrichtlinie mit dem Namen "DefaultPolicy" ab und speichert sie dann in $Pol Variable.</span><span class="sxs-lookup"><span data-stu-id="1f621-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="1f621-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f621-117">PARAMETERS</span></span>

### <span data-ttu-id="1f621-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1f621-118">-BackupManagementType</span></span>
<span data-ttu-id="1f621-119">Die Klasse der geschützten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1f621-119">The class of resources being protected.</span></span> <span data-ttu-id="1f621-120">Derzeit werden für dieses Cmdlet AzureVM, AzureStorage, AzureWorkload unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f621-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

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

### <span data-ttu-id="1f621-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f621-121">-DefaultProfile</span></span>
<span data-ttu-id="1f621-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f621-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f621-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1f621-123">-Name</span></span>
<span data-ttu-id="1f621-124">Gibt den Namen der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="1f621-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="1f621-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1f621-125">-VaultId</span></span>
<span data-ttu-id="1f621-126">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="1f621-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1f621-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1f621-127">-WorkloadType</span></span>
<span data-ttu-id="1f621-128">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="1f621-128">Workload type of the resource.</span></span> <span data-ttu-id="1f621-129">Die aktuell unterstützten Werte sind AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1f621-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="1f621-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f621-130">CommonParameters</span></span>
<span data-ttu-id="1f621-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f621-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f621-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f621-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f621-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1f621-133">INPUTS</span></span>

### <span data-ttu-id="1f621-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1f621-134">System.String</span></span>

## <span data-ttu-id="1f621-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1f621-135">OUTPUTS</span></span>

### <span data-ttu-id="1f621-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1f621-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="1f621-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1f621-137">NOTES</span></span>

## <span data-ttu-id="1f621-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1f621-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f621-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f621-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1f621-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f621-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1f621-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1f621-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


