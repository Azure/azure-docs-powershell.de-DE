---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 4c023de04cb431e18dc027c0ca3563aa6a2410e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824452"
---
# <span data-ttu-id="55762-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="55762-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="55762-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55762-102">SYNOPSIS</span></span>
<span data-ttu-id="55762-103">Deaktiviert den Schutz für ein Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="55762-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="55762-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55762-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55762-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55762-105">DESCRIPTION</span></span>
<span data-ttu-id="55762-106">Das Cmdlet **Disable-AzRecoveryServicesBackupProtection** deaktiviert den Schutz für ein Azure-Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="55762-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="55762-107">Dieses Cmdlet beendet die reguläre geplante Sicherung eines Elements.</span><span class="sxs-lookup"><span data-stu-id="55762-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="55762-108">Mit diesem Cmdlet können auch vorhandene Wiederherstellungspunkte für das Sicherungselement gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="55762-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="55762-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="55762-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="55762-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55762-110">EXAMPLES</span></span>

### <span data-ttu-id="55762-111">Beispiel 1: Deaktivieren des Sicherungs Schutzes</span><span class="sxs-lookup"><span data-stu-id="55762-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="55762-112">Der erste Befehl ruft ein Array von Sicherungs Containern ab und speichert es dann im $CONT-Array.</span><span class="sxs-lookup"><span data-stu-id="55762-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="55762-113">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in der $Pi Variablen.</span><span class="sxs-lookup"><span data-stu-id="55762-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="55762-114">Der letzte Befehl deaktiviert den Sicherungsschutz für das Element in $Pi \[ 0 \] , behält aber die Daten bei.</span><span class="sxs-lookup"><span data-stu-id="55762-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="55762-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="55762-115">PARAMETERS</span></span>

### <span data-ttu-id="55762-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55762-116">-DefaultProfile</span></span>
<span data-ttu-id="55762-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55762-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55762-118">-Force</span><span class="sxs-lookup"><span data-stu-id="55762-118">-Force</span></span>
<span data-ttu-id="55762-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="55762-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="55762-120">-Item</span><span class="sxs-lookup"><span data-stu-id="55762-120">-Item</span></span>
<span data-ttu-id="55762-121">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="55762-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="55762-122">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55762-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="55762-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="55762-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="55762-124">Gibt an, dass dieses Cmdlet vorhandene Wiederherstellungspunkte löscht.</span><span class="sxs-lookup"><span data-stu-id="55762-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="55762-125">Um gespeicherte Wiederherstellungspunkte zu einem späteren Zeitpunkt zu löschen, führen Sie dieses Cmdlet erneut aus, und geben Sie diesen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="55762-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="55762-126">-Tresor</span><span class="sxs-lookup"><span data-stu-id="55762-126">-VaultId</span></span>
<span data-ttu-id="55762-127">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="55762-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="55762-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55762-128">-Confirm</span></span>
<span data-ttu-id="55762-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55762-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55762-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55762-130">-WhatIf</span></span>
<span data-ttu-id="55762-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55762-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55762-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55762-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55762-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55762-133">CommonParameters</span></span>
<span data-ttu-id="55762-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55762-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55762-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55762-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55762-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55762-136">INPUTS</span></span>

### <span data-ttu-id="55762-137">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="55762-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="55762-138">System. String</span><span class="sxs-lookup"><span data-stu-id="55762-138">System.String</span></span>

## <span data-ttu-id="55762-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55762-139">OUTPUTS</span></span>

### <span data-ttu-id="55762-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="55762-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="55762-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="55762-141">NOTES</span></span>

## <span data-ttu-id="55762-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55762-142">RELATED LINKS</span></span>

[<span data-ttu-id="55762-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="55762-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="55762-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="55762-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="55762-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="55762-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


