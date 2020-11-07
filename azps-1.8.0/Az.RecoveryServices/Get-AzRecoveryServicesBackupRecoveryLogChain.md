---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: d06cae4fc13151d8b1c5c2b0fb4dd7803606fe49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659902"
---
# <span data-ttu-id="f368e-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="f368e-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="f368e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f368e-102">SYNOPSIS</span></span>
<span data-ttu-id="f368e-103">Dieser Befehl listet die Anfangs-und Endpunkte der unbeschädigten Protokollkette des angegebenen sicherungselements auf.</span><span class="sxs-lookup"><span data-stu-id="f368e-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="f368e-104">Verwenden Sie diese Option, um zu ermitteln, ob der Zeitpunkt, zu dem der Benutzer die Datenbank wiederherstellen möchte, gültig ist.</span><span class="sxs-lookup"><span data-stu-id="f368e-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="f368e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f368e-105">SYNTAX</span></span>

### <span data-ttu-id="f368e-106">Nofilterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="f368e-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f368e-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="f368e-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f368e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f368e-108">DESCRIPTION</span></span>
<span data-ttu-id="f368e-109">Mit dem Cmdlet **Get-AzRecoveryServicesBackupRecoveryLogChain werden** die Zeitbereich-Wiederherstellungspunkte rechtzeitig für ein gesichertes Azure-Sicherungselement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f368e-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f368e-110">Nachdem ein Element gesichert wurde, verfügt ein **AzRecoveryServicesBackupRecoveryLogChain** -Objekt über einen oder mehrere Wiederherstellungszeit Bereiche.</span><span class="sxs-lookup"><span data-stu-id="f368e-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="f368e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f368e-111">EXAMPLES</span></span>

### <span data-ttu-id="f368e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f368e-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="f368e-113">Der erste Befehl ruft das Datum vor sieben Tagen ab und speichert es dann in der $StartDate-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f368e-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f368e-114">Der zweite Befehl ruft das heutige Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f368e-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f368e-115">Der dritte Befehl ruft AzureWorkload-Sicherungs Container ab und speichert Sie in der $Containers-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f368e-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="f368e-116">Der vierte Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="f368e-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f368e-117">Der letzte Befehl ruft ein Array von Wiederherstellungspunkt-Zeitbereichen für das Element in $BackupItem ab und speichert Sie dann in der $RP-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f368e-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="f368e-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f368e-118">PARAMETERS</span></span>

### <span data-ttu-id="f368e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f368e-119">-DefaultProfile</span></span>
<span data-ttu-id="f368e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f368e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f368e-121">-Enddate</span><span class="sxs-lookup"><span data-stu-id="f368e-121">-EndDate</span></span>
<span data-ttu-id="f368e-122">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="f368e-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="f368e-123">-Item</span><span class="sxs-lookup"><span data-stu-id="f368e-123">-Item</span></span>
<span data-ttu-id="f368e-124">Geschütztes Element Objekt, für das der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="f368e-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="f368e-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f368e-125">-StartDate</span></span>
<span data-ttu-id="f368e-126">Startzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="f368e-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="f368e-127">-Tresor</span><span class="sxs-lookup"><span data-stu-id="f368e-127">-VaultId</span></span>
<span data-ttu-id="f368e-128">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="f368e-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f368e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f368e-129">CommonParameters</span></span>
<span data-ttu-id="f368e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f368e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f368e-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f368e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f368e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f368e-132">INPUTS</span></span>

### <span data-ttu-id="f368e-133">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="f368e-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="f368e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f368e-134">System.String</span></span>

## <span data-ttu-id="f368e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f368e-135">OUTPUTS</span></span>

### <span data-ttu-id="f368e-136">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f368e-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="f368e-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f368e-137">NOTES</span></span>

## <span data-ttu-id="f368e-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f368e-138">RELATED LINKS</span></span>