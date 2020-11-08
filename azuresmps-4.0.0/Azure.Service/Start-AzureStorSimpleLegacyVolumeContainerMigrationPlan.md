---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005979"
---
# <span data-ttu-id="d8e5d-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="d8e5d-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="d8e5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e5d-103">Startet die Erstellung eines Migrationsplans.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="d8e5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8e5d-104">SYNTAX</span></span>

### <span data-ttu-id="d8e5d-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="d8e5d-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d8e5d-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="d8e5d-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8e5d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8e5d-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e5d-108">Mit dem **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan-** Cmdlet wird die Erstellung eines Migrationsplans gestartet.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="d8e5d-109">Die Erstellung eines Migrationsplans ist asynchron.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="d8e5d-110">Wenn Sie den Status des Migrationsplans anzeigen möchten, verwenden Sie das Cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .</span><span class="sxs-lookup"><span data-stu-id="d8e5d-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="d8e5d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8e5d-111">EXAMPLES</span></span>

### <span data-ttu-id="d8e5d-112">Beispiel 1: Starten eines Migrationsplans</span><span class="sxs-lookup"><span data-stu-id="d8e5d-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="d8e5d-113">Mit diesem Befehl wird die Erstellung eines Migrationsplans für den Legacy Container mit dem Namen OneSDKAzureCloud gestartet.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="d8e5d-114">Der Befehl gibt eine Meldung zum Status des Plans zurück und verwendet das Cmdlet " **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** " für aktuelle Informationen.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="d8e5d-115">Beispiel 2: Starten des Migrationsplans für alle Volumen Container</span><span class="sxs-lookup"><span data-stu-id="d8e5d-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="d8e5d-116">Mit diesem Befehl wird die Erstellung des Migrationsplans für alle Legacy-Volumen Container in der importierten Konfigurationsdatei gestartet.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="d8e5d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8e5d-117">PARAMETERS</span></span>

### <span data-ttu-id="d8e5d-118">– Alle</span><span class="sxs-lookup"><span data-stu-id="d8e5d-118">-All</span></span>
<span data-ttu-id="d8e5d-119">Gibt an, dass dieses Cmdlet Migrationszeit Schätzungen für alle Volumen Container in der importierten Konfigurationsdatei startet.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="d8e5d-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="d8e5d-120">-LegacyConfigId</span></span>
<span data-ttu-id="d8e5d-121">Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="d8e5d-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="d8e5d-122">-LegacyContainerNames</span></span>
<span data-ttu-id="d8e5d-123">Gibt ein Array von Volumen Containernamen an, für die ein Migrationsplan erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

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

### <span data-ttu-id="d8e5d-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8e5d-124">-Profile</span></span>
<span data-ttu-id="d8e5d-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8e5d-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8e5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e5d-127">CommonParameters</span></span>
<span data-ttu-id="d8e5d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e5d-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e5d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e5d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8e5d-130">INPUTS</span></span>

### <span data-ttu-id="d8e5d-131">Keine</span><span class="sxs-lookup"><span data-stu-id="d8e5d-131">None</span></span>

## <span data-ttu-id="d8e5d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8e5d-132">OUTPUTS</span></span>

### <span data-ttu-id="d8e5d-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d8e5d-133">String</span></span>
<span data-ttu-id="d8e5d-134">Dieses Cmdlet gibt den Status des Migrationsplan Auftrags zurück, wenn er erfolgreich in der Appliance gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d8e5d-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="d8e5d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8e5d-135">NOTES</span></span>

## <span data-ttu-id="d8e5d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8e5d-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8e5d-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="d8e5d-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


