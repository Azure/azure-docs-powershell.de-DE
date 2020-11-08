---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 9dc42a137d3abcd23a64e096117be8d287571ecf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165036"
---
# <span data-ttu-id="f37dd-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f37dd-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="f37dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f37dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f37dd-103">Deaktiviert den Schutz für ein Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="f37dd-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="f37dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f37dd-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f37dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f37dd-105">DESCRIPTION</span></span>
<span data-ttu-id="f37dd-106">Das Cmdlet **Disable-AzRecoveryServicesBackupProtection** deaktiviert den Schutz für ein Azure-Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="f37dd-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="f37dd-107">Dieses Cmdlet beendet die reguläre geplante Sicherung eines Elements.</span><span class="sxs-lookup"><span data-stu-id="f37dd-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="f37dd-108">Mit diesem Cmdlet können auch vorhandene Wiederherstellungspunkte für das Sicherungselement gelöscht werden, wenn Sie mit dem RemoveRecoveryPoints-Parameter ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f37dd-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="f37dd-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="f37dd-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f37dd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f37dd-110">EXAMPLES</span></span>

### <span data-ttu-id="f37dd-111">Beispiel 1: Deaktivieren des Sicherungs Schutzes</span><span class="sxs-lookup"><span data-stu-id="f37dd-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="f37dd-112">Der erste Befehl ruft ein Array von Sicherungs Containern ab und speichert es dann im $CONT-Array.</span><span class="sxs-lookup"><span data-stu-id="f37dd-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="f37dd-113">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in der $Pi Variablen.</span><span class="sxs-lookup"><span data-stu-id="f37dd-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="f37dd-114">Der letzte Befehl deaktiviert den Sicherungsschutz für das Element in $Pi \[ 0 \] , behält aber die Daten bei.</span><span class="sxs-lookup"><span data-stu-id="f37dd-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="f37dd-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f37dd-115">Example 2</span></span>

<span data-ttu-id="f37dd-116">Deaktiviert den Schutz für ein Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="f37dd-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="f37dd-117">automatisch</span><span class="sxs-lookup"><span data-stu-id="f37dd-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="f37dd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f37dd-118">PARAMETERS</span></span>

### <span data-ttu-id="f37dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37dd-119">-DefaultProfile</span></span>
<span data-ttu-id="f37dd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f37dd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f37dd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f37dd-121">-Force</span></span>
<span data-ttu-id="f37dd-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f37dd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f37dd-123">-Item</span><span class="sxs-lookup"><span data-stu-id="f37dd-123">-Item</span></span>
<span data-ttu-id="f37dd-124">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f37dd-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="f37dd-125">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f37dd-125">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f37dd-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="f37dd-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="f37dd-127">Gibt an, dass dieses Cmdlet vorhandene Wiederherstellungspunkte löscht.</span><span class="sxs-lookup"><span data-stu-id="f37dd-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37dd-128">-Tresor</span><span class="sxs-lookup"><span data-stu-id="f37dd-128">-VaultId</span></span>
<span data-ttu-id="f37dd-129">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="f37dd-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f37dd-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f37dd-130">-Confirm</span></span>
<span data-ttu-id="f37dd-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f37dd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f37dd-132">-WhatIf</span></span>
<span data-ttu-id="f37dd-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f37dd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f37dd-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f37dd-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37dd-135">CommonParameters</span></span>
<span data-ttu-id="f37dd-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f37dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37dd-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f37dd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37dd-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f37dd-138">INPUTS</span></span>

### <span data-ttu-id="f37dd-139">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="f37dd-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="f37dd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f37dd-140">System.String</span></span>

## <span data-ttu-id="f37dd-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f37dd-141">OUTPUTS</span></span>

### <span data-ttu-id="f37dd-142">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f37dd-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f37dd-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="f37dd-143">NOTES</span></span>

## <span data-ttu-id="f37dd-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f37dd-144">RELATED LINKS</span></span>

[<span data-ttu-id="f37dd-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f37dd-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f37dd-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f37dd-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f37dd-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f37dd-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


