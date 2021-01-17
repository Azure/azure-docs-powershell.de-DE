---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470392"
---
# <span data-ttu-id="7277b-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="7277b-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="7277b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7277b-102">SYNOPSIS</span></span>
<span data-ttu-id="7277b-103">Das **Cmdlet "Enable-AzRecoveryServicesBackupAutoProtection"** richtet den automatischen Schutz von aktuellen und zukünftigen SQL-DBs innerhalb der angegebenen Instanz mit der angegebenen Richtlinie ein.</span><span class="sxs-lookup"><span data-stu-id="7277b-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="7277b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7277b-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7277b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7277b-105">DESCRIPTION</span></span>
<span data-ttu-id="7277b-106">Mit diesem Befehl können Benutzer automatisch alle vorhandenen ungeschützten SQL DBs und db-Dateien schützen, die später mit der angegebenen Richtlinie hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7277b-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="7277b-107">Da die Anweisung zum Sichern aller zukünftigen Psps ist, erfolgt der Vorgang auf SQLInstance-Ebene. Der Azure-Sicherungsdienst überprüft dann automatisch geschützte Container regelmäßig nach neuen PSP-Dateien und schützt sie automatisch.</span><span class="sxs-lookup"><span data-stu-id="7277b-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="7277b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7277b-108">EXAMPLES</span></span>

### <span data-ttu-id="7277b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7277b-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="7277b-110">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol Variable.</span><span class="sxs-lookup"><span data-stu-id="7277b-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="7277b-111">Das zweite Cmdlet ruft die relevante SQLInstance ab, bei der es sich um ein beschutzbares Element handelt.</span><span class="sxs-lookup"><span data-stu-id="7277b-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="7277b-112">Der dritte Befehl richtet dann den automatischen Schutz für diese Instanz mithilfe der Richtlinie in der $Pol.</span><span class="sxs-lookup"><span data-stu-id="7277b-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="7277b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7277b-113">Example 2</span></span>

<span data-ttu-id="7277b-114">Mit diesen Befehlen können Benutzer automatisch alle vorhandenen nicht geschützten DB-Dateien und db-Dateien schützen, die später mit der angegebenen Richtlinie hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7277b-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="7277b-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="7277b-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="7277b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7277b-116">PARAMETERS</span></span>

### <span data-ttu-id="7277b-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7277b-117">-BackupManagementType</span></span>
<span data-ttu-id="7277b-118">Die Klasse der geschützten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7277b-118">The class of resources being protected.</span></span> <span data-ttu-id="7277b-119">Derzeit werden für dieses Cmdlet MAB, AzureWorkload, AzureVM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7277b-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7277b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7277b-120">-DefaultProfile</span></span>
<span data-ttu-id="7277b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7277b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7277b-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="7277b-122">-InputItem</span></span>
<span data-ttu-id="7277b-123">Gibt das schützende Elementobjekt an, das als Eingabe übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="7277b-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="7277b-124">Der aktuell unterstützte Wert ist ein protectableItem-Objekt vom Typ "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="7277b-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7277b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7277b-125">-PassThru</span></span>
<span data-ttu-id="7277b-126">Gibt das Ergebnis für den automatischen Schutz zurück.</span><span class="sxs-lookup"><span data-stu-id="7277b-126">Return the result for auto protection.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7277b-127">-Policy</span><span class="sxs-lookup"><span data-stu-id="7277b-127">-Policy</span></span>
<span data-ttu-id="7277b-128">Schutzrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="7277b-128">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7277b-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7277b-129">-VaultId</span></span>
<span data-ttu-id="7277b-130">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="7277b-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7277b-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7277b-131">-WorkloadType</span></span>
<span data-ttu-id="7277b-132">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="7277b-132">Workload type of the resource.</span></span> <span data-ttu-id="7277b-133">Die aktuell unterstützten Werte sind AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="7277b-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7277b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7277b-134">-Confirm</span></span>
<span data-ttu-id="7277b-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7277b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7277b-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7277b-136">-WhatIf</span></span>
<span data-ttu-id="7277b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7277b-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="7277b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7277b-138">CommonParameters</span></span>
<span data-ttu-id="7277b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7277b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7277b-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7277b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7277b-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7277b-141">INPUTS</span></span>

### <span data-ttu-id="7277b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7277b-142">System.String</span></span>

## <span data-ttu-id="7277b-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7277b-143">OUTPUTS</span></span>

### <span data-ttu-id="7277b-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="7277b-144">System.Object</span></span>

## <span data-ttu-id="7277b-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7277b-145">NOTES</span></span>

## <span data-ttu-id="7277b-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7277b-146">RELATED LINKS</span></span>
