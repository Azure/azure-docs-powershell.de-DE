---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479373"
---
# <span data-ttu-id="4ac24-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4ac24-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="4ac24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ac24-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac24-103">Ordnet einem Element eine Azure Backup Protection-Richtlinie zu.</span><span class="sxs-lookup"><span data-stu-id="4ac24-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ac24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ac24-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ac24-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ac24-105">DESCRIPTION</span></span>
<span data-ttu-id="4ac24-106">Das Cmdlet **enable-AzureRmBackupProtection** ordnet einem Element eine Azure Backup Protection-Richtlinie zu.</span><span class="sxs-lookup"><span data-stu-id="4ac24-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="4ac24-107">Um eine Schutzrichtlinie zu aktivieren, müssen Sie zunächst über ein vorhandenes Sicherungselement und eine vorhandene Richtlinie verfügen.</span><span class="sxs-lookup"><span data-stu-id="4ac24-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="4ac24-108">Beide müssen dem gleichen sicherungstresor angehören.</span><span class="sxs-lookup"><span data-stu-id="4ac24-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="4ac24-109">Der Sicherungszeitplan führt die vollständige anfangs Kopie für das Element und die inkrementelle Kopie für die nachfolgenden Sicherungen durch.</span><span class="sxs-lookup"><span data-stu-id="4ac24-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="4ac24-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ac24-110">EXAMPLES</span></span>

### <span data-ttu-id="4ac24-111">Beispiel 1: Aktivieren des Schutzes auf einem virtuellen Azure-Computer</span><span class="sxs-lookup"><span data-stu-id="4ac24-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="4ac24-112">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="4ac24-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4ac24-113">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="4ac24-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="4ac24-114">Der zweite Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen DefaultPolicy für den Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4ac24-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="4ac24-115">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="4ac24-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="4ac24-116">Der endgültige Befehl verwendet den Pipelineoperator, um Werte von einem Cmdlet an das nächste zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="4ac24-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="4ac24-117">Mithilfe des Get-AzureRmBackupContainer-Cmdlets wird ein Container abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4ac24-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="4ac24-118">Der Befehl ruft das Sicherungselement aus diesem Container mithilfe des Get-AzureRmBackupItem-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="4ac24-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="4ac24-119">Das aktuelle Cmdlet aktiviert die in $Policy gespeicherte Richtlinie für das Element, das der Befehl an dieses Cmdlet übergibt.</span><span class="sxs-lookup"><span data-stu-id="4ac24-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="4ac24-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ac24-120">PARAMETERS</span></span>

### <span data-ttu-id="4ac24-121">-Item</span><span class="sxs-lookup"><span data-stu-id="4ac24-121">-Item</span></span>
<span data-ttu-id="4ac24-122">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4ac24-122">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="4ac24-123">Verwenden Sie zum Abrufen eines **AzureRmBackupItem** das Get-AzureRmBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac24-123">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ac24-124">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="4ac24-124">-Policy</span></span>
<span data-ttu-id="4ac24-125">Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4ac24-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="4ac24-126">Verwenden Sie das Get-AzureRmBackupProtectionPolicy-Cmdlet, um ein **AzureRmBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ac24-126">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac24-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac24-127">-DefaultProfile</span></span>
<span data-ttu-id="4ac24-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ac24-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ac24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac24-129">CommonParameters</span></span>
<span data-ttu-id="4ac24-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac24-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac24-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac24-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ac24-132">INPUTS</span></span>

### <span data-ttu-id="4ac24-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="4ac24-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="4ac24-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ac24-134">OUTPUTS</span></span>

### <span data-ttu-id="4ac24-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4ac24-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="4ac24-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ac24-136">NOTES</span></span>

## <span data-ttu-id="4ac24-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ac24-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ac24-138">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="4ac24-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="4ac24-139">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="4ac24-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="4ac24-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4ac24-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


