---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: 2613761db4a975f1bd4e04458ccdc5df81c0a2d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659967"
---
# <span data-ttu-id="5b25e-101">Disable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="5b25e-101">Disable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="5b25e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b25e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b25e-103">Deaktiviert die automatische Sicherung für ein geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="5b25e-103">Disables auto backup for a protectable item.</span></span>

## <span data-ttu-id="5b25e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b25e-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b25e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b25e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b25e-106">Das Cmdlet **Disable-AzRecoveryServicesBackupAutoProtection** deaktiviert den Schutz für ein geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="5b25e-106">The **Disable-AzRecoveryServicesBackupAutoProtection** cmdlet disables protection on a protectable item.</span></span>

## <span data-ttu-id="5b25e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b25e-107">EXAMPLES</span></span>

### <span data-ttu-id="5b25e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b25e-108">Example 1</span></span>
```
PS C:\> $container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer
PS C:\> Get-AzRecoveryServicesBackupProtectableItem -Container $container -WorkloadType "MSSQL" -ItemType "SQLInstance" | Disable-AzRecoveryServicesBackupAutoProtection -BackupManagementType "AzureWorkload" -WorkloadType "MSSQL"
```

<span data-ttu-id="5b25e-109">Das erste Cmdlet deaktiviert die Richtlinie für den Sicherungsschutz.</span><span class="sxs-lookup"><span data-stu-id="5b25e-109">The first cmdlet disables the Backup protection policy.</span></span>

## <span data-ttu-id="5b25e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b25e-110">PARAMETERS</span></span>

### <span data-ttu-id="5b25e-111">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5b25e-111">-BackupManagementType</span></span>
<span data-ttu-id="5b25e-112">Sicherungs Verwaltungstyp der Ressource (Beispiel: MAB, DPM).</span><span class="sxs-lookup"><span data-stu-id="5b25e-112">Backup Management type of the resource (for example: MAB, DPM).</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b25e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b25e-113">-DefaultProfile</span></span>
<span data-ttu-id="5b25e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b25e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b25e-115">-InputItem</span><span class="sxs-lookup"><span data-stu-id="5b25e-115">-InputItem</span></span>
<span data-ttu-id="5b25e-116">Element-ID</span><span class="sxs-lookup"><span data-stu-id="5b25e-116">Item Id</span></span>

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

### <span data-ttu-id="5b25e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b25e-117">-PassThru</span></span>
<span data-ttu-id="5b25e-118">Gibt das Ergebnis für den automatischen Schutz zurück.</span><span class="sxs-lookup"><span data-stu-id="5b25e-118">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="5b25e-119">-Tresor</span><span class="sxs-lookup"><span data-stu-id="5b25e-119">-VaultId</span></span>
<span data-ttu-id="5b25e-120">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="5b25e-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b25e-121">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="5b25e-121">-WorkloadType</span></span>
<span data-ttu-id="5b25e-122">Arbeits Auslastungs der Ressource (Beispiel: AzureVM, Windows Server, AzureFiles).</span><span class="sxs-lookup"><span data-stu-id="5b25e-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles).</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b25e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b25e-123">-Confirm</span></span>
<span data-ttu-id="5b25e-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b25e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b25e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b25e-125">-WhatIf</span></span>
<span data-ttu-id="5b25e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b25e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b25e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b25e-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b25e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b25e-128">CommonParameters</span></span>
<span data-ttu-id="5b25e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b25e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b25e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b25e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b25e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b25e-131">INPUTS</span></span>

### <span data-ttu-id="5b25e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5b25e-132">System.String</span></span>

## <span data-ttu-id="5b25e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b25e-133">OUTPUTS</span></span>

### <span data-ttu-id="5b25e-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b25e-134">System.Boolean</span></span>

## <span data-ttu-id="5b25e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b25e-135">NOTES</span></span>

## <span data-ttu-id="5b25e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b25e-136">RELATED LINKS</span></span>
