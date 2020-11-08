---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006464"
---
# <span data-ttu-id="2f227-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="2f227-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="2f227-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f227-102">SYNOPSIS</span></span>
<span data-ttu-id="2f227-103">Startet die Migration von Volumen Containern.</span><span class="sxs-lookup"><span data-stu-id="2f227-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="2f227-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f227-104">SYNTAX</span></span>

### <span data-ttu-id="2f227-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="2f227-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2f227-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="2f227-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f227-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f227-107">DESCRIPTION</span></span>
<span data-ttu-id="2f227-108">Mit dem Cmdlet " **Import-AzureStorSimpleLegacyVolumeContainer** " wird die Migration von Volumen Containern von einer Legacy-Appliance zur Ziel-Appliance gestartet.</span><span class="sxs-lookup"><span data-stu-id="2f227-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="2f227-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f227-109">EXAMPLES</span></span>

### <span data-ttu-id="2f227-110">Beispiel 1: Importieren eines Legacy-Volumen Containers</span><span class="sxs-lookup"><span data-stu-id="2f227-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="2f227-111">Mit diesem Befehl wird ein Legacy-Volumen Container für den benannten Container importiert.</span><span class="sxs-lookup"><span data-stu-id="2f227-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="2f227-112">Das Cmdlet startet den Import und gibt dann eine Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="2f227-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="2f227-113">Beispiel 2: Importieren aller Legacy-Volumen Container</span><span class="sxs-lookup"><span data-stu-id="2f227-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="2f227-114">Mit diesem Befehl werden alle Legacy-Volumen Container aus der importierten Konfigurationsdatei importiert.</span><span class="sxs-lookup"><span data-stu-id="2f227-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="2f227-115">Das Cmdlet startet den Import und gibt dann eine Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="2f227-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="2f227-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f227-116">PARAMETERS</span></span>

### <span data-ttu-id="2f227-117">– Alle</span><span class="sxs-lookup"><span data-stu-id="2f227-117">-All</span></span>
<span data-ttu-id="2f227-118">Gibt an, dass dieses Cmdlet alle Volumen Container in der importierten Konfigurationsdatei auf das Zielgerät importiert.</span><span class="sxs-lookup"><span data-stu-id="2f227-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="2f227-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2f227-119">-Force</span></span>
<span data-ttu-id="2f227-120">Gibt an, dass dieses Cmdlet den Volumen Container auf einem anderen Gerät importiert, auch wenn der Volumen Container auf einem anderen Gerät importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f227-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f227-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="2f227-121">-LegacyConfigId</span></span>
<span data-ttu-id="2f227-122">Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.</span><span class="sxs-lookup"><span data-stu-id="2f227-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="2f227-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="2f227-123">-LegacyContainerNames</span></span>
<span data-ttu-id="2f227-124">Gibt ein Array von Volumen Containernamen an, für die der Migrationsplan gilt.</span><span class="sxs-lookup"><span data-stu-id="2f227-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="2f227-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="2f227-125">-Profile</span></span>
<span data-ttu-id="2f227-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2f227-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f227-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2f227-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f227-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="2f227-128">-SkipACRs</span></span>
<span data-ttu-id="2f227-129">Gibt an, dass der Importvorgang die Zugriffssteuerungseinträge für die Migration überspringt.</span><span class="sxs-lookup"><span data-stu-id="2f227-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f227-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f227-130">CommonParameters</span></span>
<span data-ttu-id="2f227-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f227-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f227-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f227-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f227-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f227-133">INPUTS</span></span>

## <span data-ttu-id="2f227-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f227-134">OUTPUTS</span></span>

### <span data-ttu-id="2f227-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f227-135">String</span></span>
<span data-ttu-id="2f227-136">Dieser Befehl gibt den Status des Container Auftrags für den Migrationsimport Volumen zurück, wenn er erfolgreich in der Appliance gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="2f227-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="2f227-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f227-137">NOTES</span></span>

## <span data-ttu-id="2f227-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f227-138">RELATED LINKS</span></span>

[<span data-ttu-id="2f227-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="2f227-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="2f227-140">Importieren-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="2f227-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


