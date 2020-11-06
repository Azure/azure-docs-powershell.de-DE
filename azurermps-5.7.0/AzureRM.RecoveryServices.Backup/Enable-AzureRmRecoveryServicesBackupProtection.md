---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: efe4392fd57c5cb0beb6731fefb83878001b489b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478382"
---
# <span data-ttu-id="1130b-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1130b-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="1130b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1130b-102">SYNOPSIS</span></span>
<span data-ttu-id="1130b-103">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="1130b-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1130b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1130b-104">SYNTAX</span></span>

### <span data-ttu-id="1130b-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="1130b-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1130b-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="1130b-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1130b-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="1130b-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1130b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1130b-108">DESCRIPTION</span></span>
<span data-ttu-id="1130b-109">Das Cmdlet **enable-AzureRmRecoveryServicesBackupProtection** legt die Azure-Sicherungsschutz Richtlinie für ein Element fest.</span><span class="sxs-lookup"><span data-stu-id="1130b-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="1130b-110">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="1130b-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1130b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1130b-111">EXAMPLES</span></span>

### <span data-ttu-id="1130b-112">Beispiel 1: Aktivieren des Sicherungs Schutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="1130b-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="1130b-113">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1130b-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="1130b-114">Das zweite Cmdlet legt die Sicherungsschutz Richtlinie für den virtuellen Arm-Computer mit dem Namen V2VM mithilfe der Richtlinie in $Pol fest.</span><span class="sxs-lookup"><span data-stu-id="1130b-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="1130b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1130b-115">PARAMETERS</span></span>

### <span data-ttu-id="1130b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1130b-116">-DefaultProfile</span></span>
<span data-ttu-id="1130b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1130b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1130b-118">-Item</span><span class="sxs-lookup"><span data-stu-id="1130b-118">-Item</span></span>
<span data-ttu-id="1130b-119">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1130b-119">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="1130b-120">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzureRmRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1130b-120">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1130b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1130b-121">-Name</span></span>
<span data-ttu-id="1130b-122">Gibt den Namen des sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="1130b-122">Specifies the name of the Backup item.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1130b-123">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1130b-123">-Policy</span></span>
<span data-ttu-id="1130b-124">Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1130b-124">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="1130b-125">Verwenden Sie das Get-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **AzureRmRecoveryServicesBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1130b-125">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1130b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1130b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1130b-127">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1130b-127">Specifies the name of the resource group.</span></span>
<span data-ttu-id="1130b-128">Geben Sie diesen Parameter nur für virtuelle Arm-Computer an.</span><span class="sxs-lookup"><span data-stu-id="1130b-128">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1130b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1130b-129">-ServiceName</span></span>
<span data-ttu-id="1130b-130">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="1130b-130">Specifies the service name.</span></span>
<span data-ttu-id="1130b-131">Geben Sie diesen Parameter nur für ASM Virtual Machines an.</span><span class="sxs-lookup"><span data-stu-id="1130b-131">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1130b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1130b-132">-Confirm</span></span>
<span data-ttu-id="1130b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1130b-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1130b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1130b-134">-WhatIf</span></span>
<span data-ttu-id="1130b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1130b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1130b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1130b-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1130b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1130b-137">CommonParameters</span></span>
<span data-ttu-id="1130b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1130b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1130b-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1130b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1130b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1130b-140">INPUTS</span></span>

### <span data-ttu-id="1130b-141">ItemBase</span><span class="sxs-lookup"><span data-stu-id="1130b-141">ItemBase</span></span>
<span data-ttu-id="1130b-142">Der Parameter "Item" akzeptiert den Wert vom Typ "ItemBase" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1130b-142">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="1130b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1130b-143">OUTPUTS</span></span>

### <span data-ttu-id="1130b-144">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="1130b-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1130b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="1130b-145">NOTES</span></span>

## <span data-ttu-id="1130b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1130b-146">RELATED LINKS</span></span>

[<span data-ttu-id="1130b-147">Deaktivieren-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1130b-147">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="1130b-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1130b-148">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


