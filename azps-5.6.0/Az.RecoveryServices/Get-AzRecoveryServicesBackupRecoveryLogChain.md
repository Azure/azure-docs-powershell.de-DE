---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: c0080985637e58232e2f7eea37344ab291d5d594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931723"
---
# <span data-ttu-id="cbb62-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="cbb62-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="cbb62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbb62-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb62-103">Mit diesem Befehl werden die Start- und Endpunkte der ungebrochenen Protokollkette des angegebenen Sicherungselements aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbb62-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="cbb62-104">Verwenden Sie ihn, um zu ermitteln, ob der Zeitpunkt, für den der Benutzer die DB wiederherstellen möchte, gültig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="cbb62-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="cbb62-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbb62-105">SYNTAX</span></span>

### <span data-ttu-id="cbb62-106">NoFilterParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cbb62-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbb62-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="cbb62-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbb62-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbb62-108">DESCRIPTION</span></span>
<span data-ttu-id="cbb62-109">Das **Get-AzRecoveryServicesBackupRecoveryLogChain-Cmdlet** ruft die Wiederherstellungspunkte für den Zeitraum für ein gesichertes Azure Backup-Element ab.</span><span class="sxs-lookup"><span data-stu-id="cbb62-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="cbb62-110">Nachdem ein Element gesichert wurde, verfügt ein **AzRecoveryServicesBackupRecoveryLogChain-Objekt** über einen oder mehrere Wiederherstellungszeitbereiche.</span><span class="sxs-lookup"><span data-stu-id="cbb62-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="cbb62-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cbb62-111">EXAMPLES</span></span>

### <span data-ttu-id="cbb62-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cbb62-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="cbb62-113">Der erste Befehl ruft das Datum von vor sieben Tagen ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="cbb62-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="cbb62-114">Der zweite Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="cbb62-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="cbb62-115">Der dritte Befehl ruft AzureWorkload-Sicherungscontainer ab und speichert sie in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="cbb62-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="cbb62-116">Der vierte Befehl ruft das Sicherungselement ab und gibt es dann im pipedierten Cmdlet als Sicherungselementobjekt wieder.</span><span class="sxs-lookup"><span data-stu-id="cbb62-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="cbb62-117">Der letzte Befehl ruft ein Array von Wiederherstellungspunktzeitbereichen für das Element in $BackupItem ab und speichert es dann in der $RP Variablen.</span><span class="sxs-lookup"><span data-stu-id="cbb62-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="cbb62-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cbb62-118">Example 2</span></span>

<span data-ttu-id="cbb62-119">Mit diesem Befehl werden die Start- und Endpunkte der ungebrochenen Protokollkette des angegebenen Sicherungselements aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbb62-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="cbb62-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="cbb62-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="cbb62-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cbb62-121">PARAMETERS</span></span>

### <span data-ttu-id="cbb62-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb62-122">-DefaultProfile</span></span>
<span data-ttu-id="cbb62-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cbb62-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbb62-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="cbb62-124">-EndDate</span></span>
<span data-ttu-id="cbb62-125">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="cbb62-125">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbb62-126">-Item</span><span class="sxs-lookup"><span data-stu-id="cbb62-126">-Item</span></span>
<span data-ttu-id="cbb62-127">Geschütztes Elementobjekt, für das ein Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="cbb62-127">Protected Item object for which recovery point need to be fetched</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbb62-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="cbb62-128">-StartDate</span></span>
<span data-ttu-id="cbb62-129">Startzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="cbb62-129">Start time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbb62-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cbb62-130">-VaultId</span></span>
<span data-ttu-id="cbb62-131">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="cbb62-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cbb62-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb62-132">CommonParameters</span></span>
<span data-ttu-id="cbb62-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbb62-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb62-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbb62-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb62-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cbb62-135">INPUTS</span></span>

### <span data-ttu-id="cbb62-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="cbb62-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="cbb62-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cbb62-137">System.String</span></span>

## <span data-ttu-id="cbb62-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cbb62-138">OUTPUTS</span></span>

### <span data-ttu-id="cbb62-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="cbb62-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="cbb62-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cbb62-140">NOTES</span></span>

## <span data-ttu-id="cbb62-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cbb62-141">RELATED LINKS</span></span>
