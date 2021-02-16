---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146225"
---
# <span data-ttu-id="0fc1d-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="0fc1d-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="0fc1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc1d-103">Dieser Befehl listet die Start- und Endpunkte der nicht aufgebrochenen Protokollkette des angegebenen Sicherungselements auf.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="0fc1d-104">Damit können Sie feststellen, ob der Zeitpunkt, zu dem der Benutzer die DB wiederherstellen möchte, gültig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="0fc1d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fc1d-105">SYNTAX</span></span>

### <span data-ttu-id="0fc1d-106">NoFilterParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0fc1d-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fc1d-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="0fc1d-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fc1d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fc1d-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc1d-109">Das **Cmdlet "Get-AzRecoveryServicesBackupRecoveryLogChain"** ruft die Wiederherstellungspunkte für den Zeitraum für ein gesichertes Azure Backup-Element ab.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="0fc1d-110">Nachdem ein Element gesichert wurde, hat ein **AzRecoveryServicesBackupRecoveryLogChain-Objekt** einen oder mehrere Wiederherstellungszeitbereiche.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="0fc1d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0fc1d-111">EXAMPLES</span></span>

### <span data-ttu-id="0fc1d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fc1d-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="0fc1d-113">Der erste Befehl ruft das Datum von vor sieben Tagen ab und speichert es dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="0fc1d-114">Der zweite Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="0fc1d-115">Der dritte Befehl ruft Sicherungscontainer für AzureWorkload ab und speichert sie in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="0fc1d-116">Der vierte Befehl ruft das Sicherungselement ab und gibt es dann über das Cmdlet "Pipedlet" als Sicherungselementobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="0fc1d-117">Der letzte Befehl ruft ein Array von Wiederherstellungspunktzeitbereichen für das Element in $BackupItem ab und speichert sie dann in der $RP Variable.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="0fc1d-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0fc1d-118">Example 2</span></span>

<span data-ttu-id="0fc1d-119">Dieser Befehl listet die Start- und Endpunkte der nicht aufgebrochenen Protokollkette des angegebenen Sicherungselements auf.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="0fc1d-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="0fc1d-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="0fc1d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fc1d-121">PARAMETERS</span></span>

### <span data-ttu-id="0fc1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc1d-122">-DefaultProfile</span></span>
<span data-ttu-id="0fc1d-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc1d-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0fc1d-124">-EndDate</span></span>
<span data-ttu-id="0fc1d-125">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="0fc1d-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="0fc1d-126">-Item</span><span class="sxs-lookup"><span data-stu-id="0fc1d-126">-Item</span></span>
<span data-ttu-id="0fc1d-127">Geschütztes Elementobjekt, für das ein Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="0fc1d-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="0fc1d-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0fc1d-128">-StartDate</span></span>
<span data-ttu-id="0fc1d-129">Startzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="0fc1d-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="0fc1d-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0fc1d-130">-VaultId</span></span>
<span data-ttu-id="0fc1d-131">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0fc1d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc1d-132">CommonParameters</span></span>
<span data-ttu-id="0fc1d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc1d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc1d-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fc1d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc1d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0fc1d-135">INPUTS</span></span>

### <span data-ttu-id="0fc1d-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="0fc1d-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="0fc1d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0fc1d-137">System.String</span></span>

## <span data-ttu-id="0fc1d-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0fc1d-138">OUTPUTS</span></span>

### <span data-ttu-id="0fc1d-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="0fc1d-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="0fc1d-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0fc1d-140">NOTES</span></span>

## <span data-ttu-id="0fc1d-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0fc1d-141">RELATED LINKS</span></span>
