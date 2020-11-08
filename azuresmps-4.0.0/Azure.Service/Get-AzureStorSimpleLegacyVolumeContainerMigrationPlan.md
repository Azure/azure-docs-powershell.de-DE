---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005762"
---
# <span data-ttu-id="071a2-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="071a2-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="071a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="071a2-102">SYNOPSIS</span></span>
<span data-ttu-id="071a2-103">Ruft Migrationspläne für Legacy Container ab.</span><span class="sxs-lookup"><span data-stu-id="071a2-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="071a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="071a2-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="071a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="071a2-105">DESCRIPTION</span></span>
<span data-ttu-id="071a2-106">Das Cmdlet " **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** " ruft Migrationspläne für Legacy Container ab.</span><span class="sxs-lookup"><span data-stu-id="071a2-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="071a2-107">Geben Sie einen Migrationsplan anhand seiner Legacy-Konfigurations-ID an.</span><span class="sxs-lookup"><span data-stu-id="071a2-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="071a2-108">Wenn die Erstellung des Migrationsplans noch nicht abgeschlossen ist, ruft dieses Cmdlet den Status des Migrationsplans ab.</span><span class="sxs-lookup"><span data-stu-id="071a2-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="071a2-109">Wenn der Migrationsplan abgeschlossen ist, gibt dieses Cmdlet den tatsächlichen Migrationsplan für den Satz von Legacy Containern zurück.</span><span class="sxs-lookup"><span data-stu-id="071a2-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="071a2-110">Wenn Sie den *LegacyConfigId* -Parameter nicht angeben, gibt dieses Cmdlet eine Liste mit Konfigurations-IDs zurück.</span><span class="sxs-lookup"><span data-stu-id="071a2-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="071a2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="071a2-111">EXAMPLES</span></span>

### <span data-ttu-id="071a2-112">Beispiel 1: Abrufen des Status eines Plans</span><span class="sxs-lookup"><span data-stu-id="071a2-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="071a2-113">Mit diesem Befehl wird der Status des Migrationsplans abgerufen.</span><span class="sxs-lookup"><span data-stu-id="071a2-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="071a2-114">Der Status umfasst angenommene Bandbreite, geschätzte Zeit und verwandte Informationen.</span><span class="sxs-lookup"><span data-stu-id="071a2-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="071a2-115">Beispiel 2: Abrufen der IDs vorhandener Pläne</span><span class="sxs-lookup"><span data-stu-id="071a2-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="071a2-116">Dieser Befehl ruft alle Konfigurations-IDs von Migrationsplänen ab.</span><span class="sxs-lookup"><span data-stu-id="071a2-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="071a2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="071a2-117">PARAMETERS</span></span>

### <span data-ttu-id="071a2-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="071a2-118">-LegacyConfigId</span></span>
<span data-ttu-id="071a2-119">Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.</span><span class="sxs-lookup"><span data-stu-id="071a2-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="071a2-120">-LegacyContainerNames</span></span>
<span data-ttu-id="071a2-121">Gibt ein Array von Volumen Containernamen an, für die dieses Cmdlet einen Migrationsplan erhält.</span><span class="sxs-lookup"><span data-stu-id="071a2-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="071a2-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="071a2-122">-Profile</span></span>
<span data-ttu-id="071a2-123">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="071a2-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="071a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071a2-124">CommonParameters</span></span>
<span data-ttu-id="071a2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="071a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071a2-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="071a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071a2-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="071a2-127">INPUTS</span></span>

### <span data-ttu-id="071a2-128">Keine</span><span class="sxs-lookup"><span data-stu-id="071a2-128">None</span></span>

## <span data-ttu-id="071a2-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="071a2-129">OUTPUTS</span></span>

### <span data-ttu-id="071a2-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="071a2-130">MigrationPlanMsg</span></span>
<span data-ttu-id="071a2-131">Dieses Cmdlet gibt ein **MigrationPlanMsg** -Objekt zurück, das den Status des Migrationsplan Auftrags enthält, die Bandbreite in Megabit pro Sekunde und die geschätzte Zeit in Minuten angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="071a2-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="071a2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="071a2-132">NOTES</span></span>

## <span data-ttu-id="071a2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="071a2-133">RELATED LINKS</span></span>

[<span data-ttu-id="071a2-134">Anfang-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="071a2-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


