---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 81fa8a4ada2f2479d9aa2ecceb1de3c05c3f34c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945779"
---
# <span data-ttu-id="6ef76-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="6ef76-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="6ef76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef76-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef76-103">Das **Cmdlet Enable-AzRecoveryServicesBackupAutoProtection** richtet den automatischen Schutz aktueller und zukünftiger SQL-DBs innerhalb der angegebenen Instanz mit der angegebenen Richtlinie ein.</span><span class="sxs-lookup"><span data-stu-id="6ef76-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="6ef76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ef76-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ef76-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ef76-105">DESCRIPTION</span></span>
<span data-ttu-id="6ef76-106">Mit diesem Befehl können Benutzer automatisch alle vorhandenen nicht geschützten SQL DBs und db schützen, die später mit der angegebenen Richtlinie hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6ef76-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="6ef76-107">Da die Anweisung zum Sichern aller zukünftigen DBs besteht, erfolgt der Vorgang auf SQLInstance-Ebene, und der Azure-Sicherungsdienst überprüft dann regelmäßig automatisch geschützte Container auf neue DBs und schützt diese automatisch.</span><span class="sxs-lookup"><span data-stu-id="6ef76-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="6ef76-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ef76-108">EXAMPLES</span></span>

### <span data-ttu-id="6ef76-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ef76-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="6ef76-110">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol Variablen.</span><span class="sxs-lookup"><span data-stu-id="6ef76-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="6ef76-111">Das zweite Cmdlet ruft die relevante SQLInstance ab, bei der es sich um ein schützenbares Element handelt.</span><span class="sxs-lookup"><span data-stu-id="6ef76-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="6ef76-112">Der dritte Befehl richtet dann den automatischen Schutz für diese Instanz mithilfe der Richtlinie in $Pol.</span><span class="sxs-lookup"><span data-stu-id="6ef76-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="6ef76-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6ef76-113">Example 2</span></span>

<span data-ttu-id="6ef76-114">Mit diesen Befehlen können Benutzer automatisch alle vorhandenen nicht geschützten DBs und db schützen, die später mit der angegebenen Richtlinie hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6ef76-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="6ef76-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="6ef76-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="6ef76-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ef76-116">PARAMETERS</span></span>

### <span data-ttu-id="6ef76-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6ef76-117">-BackupManagementType</span></span>
<span data-ttu-id="6ef76-118">Die Klasse der zu schützenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ef76-118">The class of resources being protected.</span></span> <span data-ttu-id="6ef76-119">Derzeit werden die für dieses Cmdlet unterstützten Werte MAB, AzureWorkload, AzureVM unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ef76-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

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

### <span data-ttu-id="6ef76-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef76-120">-DefaultProfile</span></span>
<span data-ttu-id="6ef76-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ef76-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ef76-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="6ef76-122">-InputItem</span></span>
<span data-ttu-id="6ef76-123">Gibt das schützende Elementobjekt an, das als Eingabe übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ef76-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="6ef76-124">Der aktuelle unterstützte Wert ist ein protectableItem-Objekt vom Typ "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="6ef76-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

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

### <span data-ttu-id="6ef76-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ef76-125">-PassThru</span></span>
<span data-ttu-id="6ef76-126">Geben Sie das Ergebnis für den automatischen Schutz zurück.</span><span class="sxs-lookup"><span data-stu-id="6ef76-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="6ef76-127">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6ef76-127">-Policy</span></span>
<span data-ttu-id="6ef76-128">Schutzrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="6ef76-128">Protection policy object.</span></span>

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

### <span data-ttu-id="6ef76-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6ef76-129">-VaultId</span></span>
<span data-ttu-id="6ef76-130">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="6ef76-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6ef76-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6ef76-131">-WorkloadType</span></span>
<span data-ttu-id="6ef76-132">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="6ef76-132">Workload type of the resource.</span></span> <span data-ttu-id="6ef76-133">Die aktuellen unterstützten Werte sind AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="6ef76-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

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

### <span data-ttu-id="6ef76-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ef76-134">-Confirm</span></span>
<span data-ttu-id="6ef76-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ef76-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef76-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef76-136">-WhatIf</span></span>
<span data-ttu-id="6ef76-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ef76-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="6ef76-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef76-138">CommonParameters</span></span>
<span data-ttu-id="6ef76-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ef76-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef76-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ef76-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef76-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ef76-141">INPUTS</span></span>

### <span data-ttu-id="6ef76-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6ef76-142">System.String</span></span>

## <span data-ttu-id="6ef76-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ef76-143">OUTPUTS</span></span>

### <span data-ttu-id="6ef76-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="6ef76-144">System.Object</span></span>

## <span data-ttu-id="6ef76-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6ef76-145">NOTES</span></span>

## <span data-ttu-id="6ef76-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6ef76-146">RELATED LINKS</span></span>
