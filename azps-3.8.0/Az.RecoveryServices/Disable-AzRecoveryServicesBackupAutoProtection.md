---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 97eae8c5c545297a7d6287a951ec02433d591168
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847128"
---
# <span data-ttu-id="fcb15-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="fcb15-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="fcb15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcb15-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb15-103">Deaktiviert die automatische Sicherung für ein geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="fcb15-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="fcb15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb15-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb15-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcb15-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb15-106">Das Cmdlet **Disable-AzRecoveryServicesBackupAutoProtection** deaktiviert den Schutz für ein geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="fcb15-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="fcb15-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcb15-107">EXAMPLES</span></span>

### <span data-ttu-id="fcb15-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcb15-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="fcb15-109">Das erste Cmdlet deaktiviert die Richtlinie für den Sicherungsschutz.</span><span class="sxs-lookup"><span data-stu-id="fcb15-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="fcb15-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb15-110">PARAMETERS</span></span>

### <span data-ttu-id="fcb15-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="fcb15-111">-BackupManagementType</span></span>
<span data-ttu-id="fcb15-112">Sicherungs Verwaltungstyp der Ressource (Beispiel: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="fcb15-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb15-113">-DefaultProfile</span></span>
<span data-ttu-id="fcb15-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcb15-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb15-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="fcb15-115">-InputItem</span></span>
<span data-ttu-id="fcb15-116">Element-ID</span><span class="sxs-lookup"><span data-stu-id="fcb15-116">Item Id</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb15-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcb15-117">-PassThru</span></span>
<span data-ttu-id="fcb15-118">Gibt das Ergebnis für den automatischen Schutz zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb15-118">Return the result for auto protection.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb15-119">-Tresor</span><span class="sxs-lookup"><span data-stu-id="fcb15-119">-VaultId</span></span>
<span data-ttu-id="fcb15-120">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="fcb15-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fcb15-121">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="fcb15-121">-WorkloadType</span></span>
<span data-ttu-id="fcb15-122">Arbeits Auslastungs der Ressource (Beispiel: AzureVM, Windows Server, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="fcb15-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb15-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcb15-123">-Confirm</span></span>
<span data-ttu-id="fcb15-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcb15-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb15-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb15-125">-WhatIf</span></span>
<span data-ttu-id="fcb15-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcb15-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb15-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcb15-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb15-128">CommonParameters</span></span>
<span data-ttu-id="fcb15-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb15-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcb15-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb15-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcb15-131">INPUTS</span></span>

### <span data-ttu-id="fcb15-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb15-132">System.String</span></span>

## <span data-ttu-id="fcb15-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcb15-133">OUTPUTS</span></span>

### <span data-ttu-id="fcb15-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fcb15-134">System.Boolean</span></span>

## <span data-ttu-id="fcb15-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcb15-135">NOTES</span></span>

## <span data-ttu-id="fcb15-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcb15-136">RELATED LINKS</span></span>
