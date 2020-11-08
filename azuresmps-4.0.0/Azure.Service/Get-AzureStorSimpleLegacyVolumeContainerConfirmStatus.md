---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006759"
---
# <span data-ttu-id="8f8ea-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="8f8ea-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="8f8ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8ea-103">Ruft den Status eines Commit-oder Rollback-Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="8f8ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f8ea-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8f8ea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f8ea-105">DESCRIPTION</span></span>
<span data-ttu-id="8f8ea-106">Das Cmdlet " **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** " Ruft den Status des Commit-oder Rollback-Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="8f8ea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f8ea-107">EXAMPLES</span></span>

### <span data-ttu-id="8f8ea-108">Beispiel 1: Abrufen des Status eines abgeschlossenen Commit-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="8f8ea-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="8f8ea-109">Dieser Befehl ruft den Status eines Commit-Vorgangs für den benannten Container ab.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="8f8ea-110">Dieser Vorgang hat den Status "abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="8f8ea-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="8f8ea-111">Beispiel 2: Abrufen des Status eines abgeschlossenen Rollback-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="8f8ea-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="8f8ea-112">Dieser Befehl ruft den Status eines Rollback-Vorgangs für den benannten Container ab.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="8f8ea-113">Dieser Vorgang hat den Status "abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="8f8ea-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="8f8ea-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f8ea-114">PARAMETERS</span></span>

### <span data-ttu-id="8f8ea-115">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="8f8ea-115">-LegacyConfigId</span></span>
<span data-ttu-id="8f8ea-116">Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="8f8ea-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="8f8ea-117">-LegacyContainerNames</span></span>
<span data-ttu-id="8f8ea-118">Gibt ein Array von Volumen Containernamen an, für die der Migrationsplan gilt.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="8f8ea-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="8f8ea-119">-Profile</span></span>
<span data-ttu-id="8f8ea-120">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8f8ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8ea-121">CommonParameters</span></span>
<span data-ttu-id="8f8ea-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8ea-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f8ea-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8ea-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f8ea-124">INPUTS</span></span>

### <span data-ttu-id="8f8ea-125">Keine</span><span class="sxs-lookup"><span data-stu-id="8f8ea-125">None</span></span>

## <span data-ttu-id="8f8ea-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f8ea-126">OUTPUTS</span></span>

### <span data-ttu-id="8f8ea-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="8f8ea-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="8f8ea-128">Dieses Cmdlet gibt den Status des ausgeführten Confirm-Migrationsvorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="8f8ea-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="8f8ea-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f8ea-129">NOTES</span></span>

## <span data-ttu-id="8f8ea-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f8ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="8f8ea-131">Bestätigen-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="8f8ea-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="8f8ea-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="8f8ea-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)


