---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478361"
---
# <span data-ttu-id="6fa02-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="6fa02-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="6fa02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fa02-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa02-103">Lädt ein Skript herunter, um alle Dateien des Wiederherstellungspunkts bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6fa02-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fa02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fa02-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fa02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fa02-105">DESCRIPTION</span></span>
<span data-ttu-id="6fa02-106">Das Get-AzureRmRecoveryServicesBackupRPMountScript-Cmdlet lädt ein Skript herunter, das die Volumes des Wiederherstellungspunkts auf dem Computer einhängt, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa02-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="6fa02-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fa02-107">EXAMPLES</span></span>

### <span data-ttu-id="6fa02-108">Beispiel 1: Bereitstellen eines Wiederherstellungspunkts</span><span class="sxs-lookup"><span data-stu-id="6fa02-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="6fa02-109">Wenn das Skript ausgeführt wird, werden die Dateien des Wiederherstellungspunkts $Rp 0 bereitgestellt. \[\]</span><span class="sxs-lookup"><span data-stu-id="6fa02-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="6fa02-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fa02-110">PARAMETERS</span></span>

### <span data-ttu-id="6fa02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fa02-111">-DefaultProfile</span></span>
<span data-ttu-id="6fa02-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6fa02-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa02-113">-Path</span><span class="sxs-lookup"><span data-stu-id="6fa02-113">-Path</span></span>
<span data-ttu-id="6fa02-114">Der Speicherort, an dem die Datei im Fall einer Datei Wiederherstellung heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fa02-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="6fa02-115">Wenn-path nicht angegeben wird, wird die Skriptdatei im aktuellen Verzeichnis heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="6fa02-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa02-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6fa02-116">-RecoveryPoint</span></span>
<span data-ttu-id="6fa02-117">Wiederherstellungspunkt Objekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="6fa02-117">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa02-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fa02-118">-Confirm</span></span>
<span data-ttu-id="6fa02-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fa02-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa02-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fa02-120">-WhatIf</span></span>
<span data-ttu-id="6fa02-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fa02-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fa02-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fa02-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fa02-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fa02-123">CommonParameters</span></span>
<span data-ttu-id="6fa02-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fa02-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fa02-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fa02-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fa02-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fa02-126">INPUTS</span></span>

### <span data-ttu-id="6fa02-127">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="6fa02-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="6fa02-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fa02-128">OUTPUTS</span></span>

### <span data-ttu-id="6fa02-129">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="6fa02-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="6fa02-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fa02-130">NOTES</span></span>

## <span data-ttu-id="6fa02-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fa02-131">RELATED LINKS</span></span>

