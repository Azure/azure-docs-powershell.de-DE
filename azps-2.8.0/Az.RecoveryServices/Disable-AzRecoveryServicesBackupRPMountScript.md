---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 934f7ac105ee1164011df9bcacc672437ef4bf78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824451"
---
# <span data-ttu-id="cef5c-101">Disable-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="cef5c-101">Disable-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="cef5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cef5c-102">SYNOPSIS</span></span>
<span data-ttu-id="cef5c-103">Die Bereitstellung aller Dateien des Wiederherstellungspunkts wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="cef5c-103">Dismounts all the files of the recovery point.</span></span>

## <span data-ttu-id="cef5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cef5c-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef5c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cef5c-105">DESCRIPTION</span></span>
<span data-ttu-id="cef5c-106">Mit dem Cmdlet "Disable-AzRecoveryServicesBackupRPMountScript" werden die Dateien des Wiederherstellungspunkts, die zuvor mithilfe des Get-AzRecoveryServicesBackupRPMountScript-Cmdlets bereitgestellt wurden, aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="cef5c-106">The Disable-AzRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="cef5c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cef5c-107">EXAMPLES</span></span>

### <span data-ttu-id="cef5c-108">Beispiel 1: Aufheben der Bereitstellungeines Wiederherstellungspunkts</span><span class="sxs-lookup"><span data-stu-id="cef5c-108">Example 1: Dismount a recovery point</span></span>
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

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="cef5c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cef5c-109">PARAMETERS</span></span>

### <span data-ttu-id="cef5c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef5c-110">-DefaultProfile</span></span>
<span data-ttu-id="cef5c-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cef5c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cef5c-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cef5c-112">-PassThru</span></span>
<span data-ttu-id="cef5c-113">Geben Sie den Wiederherstellungspunkt zurück.</span><span class="sxs-lookup"><span data-stu-id="cef5c-113">Return the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef5c-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cef5c-114">-RecoveryPoint</span></span>
<span data-ttu-id="cef5c-115">Wiederherstellungspunkt Objekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="cef5c-115">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="cef5c-116">-Tresor</span><span class="sxs-lookup"><span data-stu-id="cef5c-116">-VaultId</span></span>
<span data-ttu-id="cef5c-117">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="cef5c-117">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cef5c-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cef5c-118">-Confirm</span></span>
<span data-ttu-id="cef5c-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cef5c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef5c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef5c-120">-WhatIf</span></span>
<span data-ttu-id="cef5c-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cef5c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef5c-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cef5c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef5c-123">CommonParameters</span></span>
<span data-ttu-id="cef5c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef5c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef5c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef5c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cef5c-126">INPUTS</span></span>

### <span data-ttu-id="cef5c-127">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="cef5c-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="cef5c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cef5c-128">System.String</span></span>

## <span data-ttu-id="cef5c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cef5c-129">OUTPUTS</span></span>

### <span data-ttu-id="cef5c-130">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="cef5c-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="cef5c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cef5c-131">NOTES</span></span>

## <span data-ttu-id="cef5c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cef5c-132">RELATED LINKS</span></span>
