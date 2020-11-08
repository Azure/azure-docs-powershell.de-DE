---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 427da45eed5e2e9e27421e67d9e6e776d9106367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004937"
---
# <span data-ttu-id="749f7-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="749f7-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="749f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="749f7-102">SYNOPSIS</span></span>
<span data-ttu-id="749f7-103">Lädt ein Skript herunter, um alle Dateien des Wiederherstellungspunkts bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="749f7-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="749f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="749f7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="749f7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="749f7-105">DESCRIPTION</span></span>
<span data-ttu-id="749f7-106">Das Get-AzRecoveryServicesBackupRPMountScript-Cmdlet lädt ein Skript herunter, das die Volumes des Wiederherstellungspunkts auf dem Computer einhängt, auf dem es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="749f7-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="749f7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="749f7-107">EXAMPLES</span></span>

### <span data-ttu-id="749f7-108">Beispiel 1: Bereitstellen eines Wiederherstellungspunkts</span><span class="sxs-lookup"><span data-stu-id="749f7-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="749f7-109">Wenn das Skript ausgeführt wird, werden die Dateien des Wiederherstellungspunkts $Rp 0 bereitgestellt. \[\]</span><span class="sxs-lookup"><span data-stu-id="749f7-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="749f7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="749f7-110">PARAMETERS</span></span>

### <span data-ttu-id="749f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="749f7-111">-DefaultProfile</span></span>
<span data-ttu-id="749f7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="749f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="749f7-113">-Path</span><span class="sxs-lookup"><span data-stu-id="749f7-113">-Path</span></span>
<span data-ttu-id="749f7-114">Der Speicherort, an dem die Datei im Fall einer Datei Wiederherstellung heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="749f7-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="749f7-115">Wenn-path nicht angegeben wird, wird die Skriptdatei im aktuellen Verzeichnis heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="749f7-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749f7-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="749f7-116">-RecoveryPoint</span></span>
<span data-ttu-id="749f7-117">Wiederherstellungspunkt Objekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="749f7-117">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="749f7-118">-Tresor</span><span class="sxs-lookup"><span data-stu-id="749f7-118">-VaultId</span></span>
<span data-ttu-id="749f7-119">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="749f7-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="749f7-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="749f7-120">-Confirm</span></span>
<span data-ttu-id="749f7-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="749f7-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749f7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="749f7-122">-WhatIf</span></span>
<span data-ttu-id="749f7-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="749f7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="749f7-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="749f7-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="749f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749f7-125">CommonParameters</span></span>
<span data-ttu-id="749f7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="749f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749f7-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="749f7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749f7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="749f7-128">INPUTS</span></span>

### <span data-ttu-id="749f7-129">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="749f7-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="749f7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="749f7-130">System.String</span></span>

## <span data-ttu-id="749f7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="749f7-131">OUTPUTS</span></span>

### <span data-ttu-id="749f7-132">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="749f7-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="749f7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="749f7-133">NOTES</span></span>

## <span data-ttu-id="749f7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="749f7-134">RELATED LINKS</span></span>
