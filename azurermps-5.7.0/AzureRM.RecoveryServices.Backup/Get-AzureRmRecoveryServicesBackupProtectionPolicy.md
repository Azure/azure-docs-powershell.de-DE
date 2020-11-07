---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662354"
---
# <span data-ttu-id="be6fa-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be6fa-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="be6fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="be6fa-103">Ruft Sicherungsschutz Richtlinien für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="be6fa-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be6fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be6fa-104">SYNTAX</span></span>

### <span data-ttu-id="be6fa-105">Noparamet (Standard)</span><span class="sxs-lookup"><span data-stu-id="be6fa-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be6fa-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="be6fa-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be6fa-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="be6fa-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be6fa-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="be6fa-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be6fa-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be6fa-109">DESCRIPTION</span></span>
<span data-ttu-id="be6fa-110">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupProtectionPolicy** " ruft Azure-Sicherungsschutz Richtlinien für einen Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="be6fa-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="be6fa-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="be6fa-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="be6fa-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be6fa-112">EXAMPLES</span></span>

### <span data-ttu-id="be6fa-113">Beispiel 1: Abrufen aller Richtlinien im Tresor</span><span class="sxs-lookup"><span data-stu-id="be6fa-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="be6fa-114">Dieser Befehl ruft alle im Tresor erstellten Schutzrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="be6fa-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="be6fa-115">Beispiel 2: Abrufen einer bestimmten Richtlinie</span><span class="sxs-lookup"><span data-stu-id="be6fa-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="be6fa-116">Dieser Befehl ruft die Schutzrichtlinie mit dem Namen DefaultPolicy ab und speichert Sie dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="be6fa-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="be6fa-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="be6fa-117">PARAMETERS</span></span>

### <span data-ttu-id="be6fa-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="be6fa-118">-BackupManagementType</span></span>
<span data-ttu-id="be6fa-119">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="be6fa-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="be6fa-120">Derzeit wird nur AzureVM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be6fa-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be6fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be6fa-121">-DefaultProfile</span></span>
<span data-ttu-id="be6fa-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="be6fa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be6fa-123">-Name</span><span class="sxs-lookup"><span data-stu-id="be6fa-123">-Name</span></span>
<span data-ttu-id="be6fa-124">Gibt den Namen der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="be6fa-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be6fa-125">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="be6fa-125">-WorkloadType</span></span>
<span data-ttu-id="be6fa-126">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="be6fa-126">Specifies the workload type.</span></span>
<span data-ttu-id="be6fa-127">Derzeit wird nur AzureVM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be6fa-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be6fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be6fa-128">CommonParameters</span></span>
<span data-ttu-id="be6fa-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be6fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be6fa-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be6fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be6fa-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be6fa-131">INPUTS</span></span>

### <span data-ttu-id="be6fa-132">Keine</span><span class="sxs-lookup"><span data-stu-id="be6fa-132">None</span></span>
<span data-ttu-id="be6fa-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="be6fa-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be6fa-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be6fa-134">OUTPUTS</span></span>

### <span data-ttu-id="be6fa-135">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="be6fa-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="be6fa-136">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase]</span><span class="sxs-lookup"><span data-stu-id="be6fa-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="be6fa-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="be6fa-137">NOTES</span></span>

## <span data-ttu-id="be6fa-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be6fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="be6fa-139">Neu – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be6fa-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="be6fa-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be6fa-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="be6fa-141">Satz-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="be6fa-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


