---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1b29bcc12c92b08e1c21dff4bb8b239fcc8f2bf6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004938"
---
# <span data-ttu-id="e8292-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8292-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="e8292-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8292-102">SYNOPSIS</span></span>
<span data-ttu-id="e8292-103">Ruft Sicherungsschutz Richtlinien für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="e8292-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="e8292-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8292-104">SYNTAX</span></span>

### <span data-ttu-id="e8292-105">Noparamet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8292-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8292-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="e8292-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8292-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="e8292-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8292-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="e8292-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8292-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8292-109">DESCRIPTION</span></span>
<span data-ttu-id="e8292-110">Das Cmdlet " **Get-AzRecoveryServicesBackupProtectionPolicy** " ruft Azure-Sicherungsschutz Richtlinien für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="e8292-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="e8292-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8292-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e8292-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8292-112">EXAMPLES</span></span>

### <span data-ttu-id="e8292-113">Beispiel 1: Abrufen aller Richtlinien im Tresor</span><span class="sxs-lookup"><span data-stu-id="e8292-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="e8292-114">Dieser Befehl ruft alle im Tresor erstellten Schutzrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="e8292-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="e8292-115">Beispiel 2: Abrufen einer bestimmten Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e8292-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="e8292-116">Dieser Befehl ruft die Schutzrichtlinie mit dem Namen DefaultPolicy ab und speichert Sie dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e8292-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="e8292-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8292-117">PARAMETERS</span></span>

### <span data-ttu-id="e8292-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e8292-118">-BackupManagementType</span></span>
<span data-ttu-id="e8292-119">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="e8292-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="e8292-120">Derzeit wird nur AzureVM, AzureStorage unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e8292-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8292-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8292-121">-DefaultProfile</span></span>
<span data-ttu-id="e8292-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8292-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8292-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e8292-123">-Name</span></span>
<span data-ttu-id="e8292-124">Gibt den Namen der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="e8292-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="e8292-125">-Tresor</span><span class="sxs-lookup"><span data-stu-id="e8292-125">-VaultId</span></span>
<span data-ttu-id="e8292-126">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="e8292-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e8292-127">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="e8292-127">-WorkloadType</span></span>
<span data-ttu-id="e8292-128">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="e8292-128">Specifies the workload type.</span></span>
<span data-ttu-id="e8292-129">Derzeit wird nur AzureVM, AzureFiles unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e8292-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

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

### <span data-ttu-id="e8292-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8292-130">CommonParameters</span></span>
<span data-ttu-id="e8292-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8292-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8292-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8292-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8292-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8292-133">INPUTS</span></span>

### <span data-ttu-id="e8292-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e8292-134">System.String</span></span>

## <span data-ttu-id="e8292-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8292-135">OUTPUTS</span></span>

### <span data-ttu-id="e8292-136">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="e8292-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="e8292-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8292-137">NOTES</span></span>

## <span data-ttu-id="e8292-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8292-138">RELATED LINKS</span></span>

[<span data-ttu-id="e8292-139">Neu – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8292-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e8292-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8292-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e8292-141">Satz-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8292-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


