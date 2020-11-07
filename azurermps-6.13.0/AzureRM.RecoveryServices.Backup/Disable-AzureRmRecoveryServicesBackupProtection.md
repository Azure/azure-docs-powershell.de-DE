---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 07406378df0439171c5be2e7558e8ac33cb32687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662666"
---
# <span data-ttu-id="42d9d-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="42d9d-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="42d9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="42d9d-103">Deaktiviert den Schutz für ein Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="42d9d-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42d9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42d9d-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d9d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="42d9d-106">Das Cmdlet **Disable-AzureRmRecoveryServicesBackupProtection** deaktiviert den Schutz für ein Azure-Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="42d9d-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="42d9d-107">Dieses Cmdlet beendet die reguläre geplante Sicherung eines Elements.</span><span class="sxs-lookup"><span data-stu-id="42d9d-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="42d9d-108">Mit diesem Cmdlet können auch vorhandene Wiederherstellungspunkte für das Sicherungselement gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="42d9d-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="42d9d-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="42d9d-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="42d9d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42d9d-110">EXAMPLES</span></span>

### <span data-ttu-id="42d9d-111">Beispiel 1: Deaktivieren des Sicherungs Schutzes</span><span class="sxs-lookup"><span data-stu-id="42d9d-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="42d9d-112">Der erste Befehl ruft ein Array von Sicherungs Containern ab und speichert es dann im $CONT-Array.</span><span class="sxs-lookup"><span data-stu-id="42d9d-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="42d9d-113">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in der $Pi Variablen.</span><span class="sxs-lookup"><span data-stu-id="42d9d-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="42d9d-114">Der letzte Befehl deaktiviert den Sicherungsschutz für das Element in $Pi \[ 0 \] , behält aber die Daten bei.</span><span class="sxs-lookup"><span data-stu-id="42d9d-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="42d9d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d9d-115">PARAMETERS</span></span>

### <span data-ttu-id="42d9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d9d-116">-DefaultProfile</span></span>
<span data-ttu-id="42d9d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42d9d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d9d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="42d9d-118">-Force</span></span>
<span data-ttu-id="42d9d-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="42d9d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42d9d-120">-Item</span><span class="sxs-lookup"><span data-stu-id="42d9d-120">-Item</span></span>
<span data-ttu-id="42d9d-121">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="42d9d-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="42d9d-122">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzureRmRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42d9d-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="42d9d-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="42d9d-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="42d9d-124">Gibt an, dass dieses Cmdlet vorhandene Wiederherstellungspunkte löscht.</span><span class="sxs-lookup"><span data-stu-id="42d9d-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="42d9d-125">Um gespeicherte Wiederherstellungspunkte zu einem späteren Zeitpunkt zu löschen, führen Sie dieses Cmdlet erneut aus, und geben Sie diesen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="42d9d-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="42d9d-126">-Tresor</span><span class="sxs-lookup"><span data-stu-id="42d9d-126">-VaultId</span></span>
<span data-ttu-id="42d9d-127">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="42d9d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="42d9d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42d9d-128">-Confirm</span></span>
<span data-ttu-id="42d9d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42d9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d9d-130">-WhatIf</span></span>
<span data-ttu-id="42d9d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42d9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d9d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42d9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d9d-133">CommonParameters</span></span>
<span data-ttu-id="42d9d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d9d-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d9d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d9d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42d9d-136">INPUTS</span></span>

### <span data-ttu-id="42d9d-137">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="42d9d-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="42d9d-138">Parameter: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42d9d-138">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="42d9d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="42d9d-139">System.String</span></span>
<span data-ttu-id="42d9d-140">Parameter: Vault-ByValue</span><span class="sxs-lookup"><span data-stu-id="42d9d-140">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="42d9d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42d9d-141">OUTPUTS</span></span>

### <span data-ttu-id="42d9d-142">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="42d9d-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="42d9d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="42d9d-143">NOTES</span></span>

## <span data-ttu-id="42d9d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42d9d-144">RELATED LINKS</span></span>

[<span data-ttu-id="42d9d-145">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="42d9d-145">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="42d9d-146">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="42d9d-146">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="42d9d-147">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="42d9d-147">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


