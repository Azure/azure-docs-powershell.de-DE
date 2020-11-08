---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005906"
---
# <span data-ttu-id="d4a62-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="d4a62-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="d4a62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4a62-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a62-103">Initiiert das Commit oder Rollback der zu migrierenden Volumen Container.</span><span class="sxs-lookup"><span data-stu-id="d4a62-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="d4a62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a62-104">SYNTAX</span></span>

### <span data-ttu-id="d4a62-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="d4a62-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d4a62-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="d4a62-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d4a62-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4a62-107">DESCRIPTION</span></span>
<span data-ttu-id="d4a62-108">Das Cmdlet **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** initiiert das Commit oder Rollback der Volumen Container, die als Teil einer Legacy Migration migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d4a62-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="d4a62-109">Der Rollback stellt die Appliance wieder auf den ursprünglichen Besitz zurück.</span><span class="sxs-lookup"><span data-stu-id="d4a62-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="d4a62-110">Der Commit weist der Ziel Appliance den Besitz zu.</span><span class="sxs-lookup"><span data-stu-id="d4a62-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="d4a62-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4a62-111">EXAMPLES</span></span>

### <span data-ttu-id="d4a62-112">Beispiel 1: Initiieren eines Commit-Vorgangs für einen bestimmten Volumen Container</span><span class="sxs-lookup"><span data-stu-id="d4a62-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d4a62-113">Dieser Befehl initiiert einen Commit-Vorgang für den angegebenen Volumen Container für die angegebene Legacy-Konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="d4a62-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="d4a62-114">Um den Status des Vorgangs anzuzeigen, verwenden Sie das Cmdlet **Get-AzureStorSimpleLegacyVolumeContainerStatus** .</span><span class="sxs-lookup"><span data-stu-id="d4a62-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="d4a62-115">Beispiel 2: Initiieren eines Rollback-Vorgangs für einen bestimmten Volumen Container</span><span class="sxs-lookup"><span data-stu-id="d4a62-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d4a62-116">Mit diesem Befehl wird ein Rollback-Vorgang für den angegebenen Volumen Container für die angegebene Legacy-Konfigurations-ID initiiert.</span><span class="sxs-lookup"><span data-stu-id="d4a62-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="d4a62-117">Beispiel 3: Initiieren eines Commit-Vorgangs für alle Volumen Container</span><span class="sxs-lookup"><span data-stu-id="d4a62-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d4a62-118">Mit diesem Befehl wird ein Commit-Vorgang für den gesamten Volumen Container für die angegebene Legacy-Konfigurations-ID initiiert.</span><span class="sxs-lookup"><span data-stu-id="d4a62-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="d4a62-119">Beispiel 4: Initiieren eines Rollback-Vorgangs für alle Volumen Container</span><span class="sxs-lookup"><span data-stu-id="d4a62-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d4a62-120">Mit diesem Befehl wird ein Rollback-Vorgang für alle Volumen Container für die angegebene Legacy-Konfigurations-ID initiiert.</span><span class="sxs-lookup"><span data-stu-id="d4a62-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="d4a62-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a62-121">PARAMETERS</span></span>

### <span data-ttu-id="d4a62-122">– Alle</span><span class="sxs-lookup"><span data-stu-id="d4a62-122">-All</span></span>
<span data-ttu-id="d4a62-123">Gibt an, dass dieses Cmdlet einen Rollback-oder Commit-Vorgang für alle Volumen Container in der importierten Konfigurationsdatei initiiert.</span><span class="sxs-lookup"><span data-stu-id="d4a62-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a62-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="d4a62-124">-LegacyConfigId</span></span>
<span data-ttu-id="d4a62-125">Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.</span><span class="sxs-lookup"><span data-stu-id="d4a62-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="d4a62-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="d4a62-126">-LegacyContainerNames</span></span>
<span data-ttu-id="d4a62-127">Gibt ein Array von Volumen Containernamen an, für die der Migrationsplan gilt.</span><span class="sxs-lookup"><span data-stu-id="d4a62-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a62-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="d4a62-128">-MigrationOperation</span></span>
<span data-ttu-id="d4a62-129">Gibt an, ob dieses Cmdlet einen Commit oder Rollback ausführt.</span><span class="sxs-lookup"><span data-stu-id="d4a62-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="d4a62-130">Gültige Werte sind: Commit und Rollback.</span><span class="sxs-lookup"><span data-stu-id="d4a62-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="d4a62-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="d4a62-131">-Profile</span></span>
<span data-ttu-id="d4a62-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d4a62-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4a62-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d4a62-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4a62-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a62-134">CommonParameters</span></span>
<span data-ttu-id="d4a62-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a62-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a62-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a62-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a62-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4a62-137">INPUTS</span></span>

## <span data-ttu-id="d4a62-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4a62-138">OUTPUTS</span></span>

## <span data-ttu-id="d4a62-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4a62-139">NOTES</span></span>

## <span data-ttu-id="d4a62-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4a62-140">RELATED LINKS</span></span>

[<span data-ttu-id="d4a62-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="d4a62-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="d4a62-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="d4a62-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="d4a62-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="d4a62-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


