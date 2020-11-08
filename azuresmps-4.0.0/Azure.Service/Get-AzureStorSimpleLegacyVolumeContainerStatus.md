---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006756"
---
# <span data-ttu-id="62ad7-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="62ad7-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="62ad7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="62ad7-103">Ruft den Migrationsstatus der Volumen Container ab.</span><span class="sxs-lookup"><span data-stu-id="62ad7-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="62ad7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ad7-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="62ad7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="62ad7-106">Das Cmdlet " **Get-AzureStorSimpleLegacyVolumeContainerStatus** " Ruft den Migrationsstatus der Volumen Container ab.</span><span class="sxs-lookup"><span data-stu-id="62ad7-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="62ad7-107">Dieses Cmdlet gibt Statusinformationen zurück, die beinhalten, ob die Volume-Container Migration noch ausgeführt, abgeschlossen oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="62ad7-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="62ad7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62ad7-108">EXAMPLES</span></span>

### <span data-ttu-id="62ad7-109">Beispiel 1: Abrufen des Status für eine fehlgeschlagene Migration</span><span class="sxs-lookup"><span data-stu-id="62ad7-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="62ad7-110">Dieser Befehl ruft den Migrationsstatus für den benannten Legacy Container ab.</span><span class="sxs-lookup"><span data-stu-id="62ad7-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="62ad7-111">Die Ergebnisse zeigen, dass die Migration fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="62ad7-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="62ad7-112">Beispiel 2: Abrufen des Status für eine in Bearbeitung befindliche Migration</span><span class="sxs-lookup"><span data-stu-id="62ad7-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="62ad7-113">Dieser Befehl ruft den Migrationsstatus für den benannten Legacy Container ab.</span><span class="sxs-lookup"><span data-stu-id="62ad7-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="62ad7-114">Die Ergebnisse zeigen, dass die Migration gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62ad7-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="62ad7-115">Beispiel 3: Abrufen des Status für eine abgeschlossene Migration</span><span class="sxs-lookup"><span data-stu-id="62ad7-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="62ad7-116">Dieser Befehl ruft den Migrationsstatus für den benannten Legacy Container ab.</span><span class="sxs-lookup"><span data-stu-id="62ad7-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="62ad7-117">Die Ergebnisse zeigen, dass die Migration abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="62ad7-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="62ad7-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="62ad7-118">PARAMETERS</span></span>

### <span data-ttu-id="62ad7-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="62ad7-119">-LegacyConfigId</span></span>
<span data-ttu-id="62ad7-120">Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.</span><span class="sxs-lookup"><span data-stu-id="62ad7-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ad7-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="62ad7-121">-LegacyContainerNames</span></span>
<span data-ttu-id="62ad7-122">Gibt ein Array von Volumen Containernamen an, für die der Migrationsplan gilt.</span><span class="sxs-lookup"><span data-stu-id="62ad7-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ad7-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="62ad7-123">-Profile</span></span>
<span data-ttu-id="62ad7-124">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="62ad7-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ad7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ad7-125">CommonParameters</span></span>
<span data-ttu-id="62ad7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ad7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ad7-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ad7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ad7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62ad7-128">INPUTS</span></span>

## <span data-ttu-id="62ad7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62ad7-129">OUTPUTS</span></span>

## <span data-ttu-id="62ad7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="62ad7-130">NOTES</span></span>

## <span data-ttu-id="62ad7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62ad7-131">RELATED LINKS</span></span>

[<span data-ttu-id="62ad7-132">Bestätigen-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="62ad7-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="62ad7-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="62ad7-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


