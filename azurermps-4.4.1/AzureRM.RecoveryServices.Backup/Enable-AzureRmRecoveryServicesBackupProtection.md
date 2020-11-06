---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 76238516065dffc7a8a38ee6ad025f67d54b47c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481713"
---
# <span data-ttu-id="93af2-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="93af2-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="93af2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93af2-102">SYNOPSIS</span></span>
<span data-ttu-id="93af2-103">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="93af2-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93af2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93af2-104">SYNTAX</span></span>

### <span data-ttu-id="93af2-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="93af2-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93af2-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="93af2-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93af2-107">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="93af2-107">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93af2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93af2-108">DESCRIPTION</span></span>
<span data-ttu-id="93af2-109">Das Cmdlet **enable-AzureRmRecoveryServicesBackupProtection** legt die Azure-Sicherungsschutz Richtlinie für ein Element fest.</span><span class="sxs-lookup"><span data-stu-id="93af2-109">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>

<span data-ttu-id="93af2-110">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="93af2-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="93af2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93af2-111">EXAMPLES</span></span>

### <span data-ttu-id="93af2-112">Beispiel 1: Aktivieren des Sicherungs Schutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="93af2-112">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="93af2-113">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="93af2-113">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="93af2-114">Das zweite Cmdlet legt die Sicherungsschutz Richtlinie für den virtuellen Arm-Computer mit dem Namen V2VM mithilfe der Richtlinie in $Pol fest.</span><span class="sxs-lookup"><span data-stu-id="93af2-114">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="93af2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="93af2-115">PARAMETERS</span></span>

### <span data-ttu-id="93af2-116">-Item</span><span class="sxs-lookup"><span data-stu-id="93af2-116">-Item</span></span>
<span data-ttu-id="93af2-117">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="93af2-117">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="93af2-118">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzureRmRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93af2-118">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93af2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="93af2-119">-Name</span></span>
<span data-ttu-id="93af2-120">Gibt den Namen des sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="93af2-120">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93af2-121">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="93af2-121">-Policy</span></span>
<span data-ttu-id="93af2-122">Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93af2-122">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="93af2-123">Verwenden Sie das Get-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **AzureRmRecoveryServicesBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93af2-123">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93af2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93af2-124">-ResourceGroupName</span></span>
<span data-ttu-id="93af2-125">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="93af2-125">Specifies the name of the resource group.</span></span>
<span data-ttu-id="93af2-126">Geben Sie diesen Parameter nur für virtuelle Arm-Computer an.</span><span class="sxs-lookup"><span data-stu-id="93af2-126">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93af2-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="93af2-127">-ServiceName</span></span>
<span data-ttu-id="93af2-128">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="93af2-128">Specifies the service name.</span></span>
<span data-ttu-id="93af2-129">Geben Sie diesen Parameter nur für ASM Virtual Machines an.</span><span class="sxs-lookup"><span data-stu-id="93af2-129">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93af2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93af2-130">-DefaultProfile</span></span>
<span data-ttu-id="93af2-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93af2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93af2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93af2-132">CommonParameters</span></span>
<span data-ttu-id="93af2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93af2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93af2-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93af2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93af2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93af2-135">INPUTS</span></span>

### <span data-ttu-id="93af2-136">ItemBase</span><span class="sxs-lookup"><span data-stu-id="93af2-136">ItemBase</span></span>
<span data-ttu-id="93af2-137">Der Parameter "Item" akzeptiert den Wert vom Typ "ItemBase" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="93af2-137">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="93af2-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93af2-138">OUTPUTS</span></span>

### <span data-ttu-id="93af2-139">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="93af2-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="93af2-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="93af2-140">NOTES</span></span>

## <span data-ttu-id="93af2-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93af2-141">RELATED LINKS</span></span>

[<span data-ttu-id="93af2-142">Deaktivieren-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="93af2-142">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="93af2-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="93af2-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


