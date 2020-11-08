---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: a6c47561b8fdb9e748940c917d85548d25be1ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997384"
---
# <span data-ttu-id="8a6ee-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8a6ee-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="8a6ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6ee-103">Mit diesem Befehl kann Azure Backup die Ressource in einen Sicherungs Container konvertieren, der dann für den angegebenen Recovery Services Vault registriert wird.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="8a6ee-104">Der Azure Backup-Dienst kann dann Arbeitslasten des angegebenen Arbeits Auslastungs Typs innerhalb dieses Containers ermitteln, um später geschützt zu werden.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="8a6ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a6ee-105">SYNTAX</span></span>

### <span data-ttu-id="8a6ee-106">Registrieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a6ee-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6ee-107">Registrieren</span><span class="sxs-lookup"><span data-stu-id="8a6ee-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a6ee-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a6ee-108">DESCRIPTION</span></span>
<span data-ttu-id="8a6ee-109">Das Cmdlet registriert eine Azure VM für AzureWorkloads mit einem bestimmten workloadtype.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="8a6ee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a6ee-110">EXAMPLES</span></span>

### <span data-ttu-id="8a6ee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a6ee-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="8a6ee-112">Das Cmdlet registriert eine Azure VM für die Arbeitsauslastung MSSQL.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="8a6ee-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a6ee-113">PARAMETERS</span></span>

### <span data-ttu-id="8a6ee-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8a6ee-114">-BackupManagementType</span></span>
<span data-ttu-id="8a6ee-115">Der Sicherungs Verwaltungstyp des Azure-Sicherungs Containers</span><span class="sxs-lookup"><span data-stu-id="8a6ee-115">The backup management type of the Azure Backup container</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6ee-116">-Container</span><span class="sxs-lookup"><span data-stu-id="8a6ee-116">-Container</span></span>
<span data-ttu-id="8a6ee-117">Container, in dem sich das Element befindet</span><span class="sxs-lookup"><span data-stu-id="8a6ee-117">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6ee-118">-DefaultProfile</span></span>
<span data-ttu-id="8a6ee-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6ee-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8a6ee-120">-Force</span></span>
<span data-ttu-id="8a6ee-121">Register Container erzwingen (Bestätigungsdialogfeld wird verhindert).</span><span class="sxs-lookup"><span data-stu-id="8a6ee-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="8a6ee-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="8a6ee-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8a6ee-123">-ResourceId</span></span>
<span data-ttu-id="8a6ee-124">Die ID der Azure-Ressource, deren repräsentatives Element überprüft werden muss, wenn es bereits durch einige RecoveryServices-Tresor im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6ee-125">-Tresor</span><span class="sxs-lookup"><span data-stu-id="8a6ee-125">-VaultId</span></span>
<span data-ttu-id="8a6ee-126">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="8a6ee-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8a6ee-127">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="8a6ee-127">-WorkloadType</span></span>
<span data-ttu-id="8a6ee-128">Arbeits Auslastungs der Ressource (Beispiel: AzureVM, Windows Server, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="8a6ee-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

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

### <span data-ttu-id="8a6ee-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a6ee-129">-Confirm</span></span>
<span data-ttu-id="8a6ee-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6ee-131">-WhatIf</span></span>
<span data-ttu-id="8a6ee-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a6ee-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6ee-134">CommonParameters</span></span>
<span data-ttu-id="8a6ee-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6ee-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a6ee-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6ee-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a6ee-137">INPUTS</span></span>

### <span data-ttu-id="8a6ee-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8a6ee-138">System.String</span></span>

## <span data-ttu-id="8a6ee-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a6ee-139">OUTPUTS</span></span>

### <span data-ttu-id="8a6ee-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="8a6ee-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="8a6ee-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a6ee-141">NOTES</span></span>

## <span data-ttu-id="8a6ee-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a6ee-142">RELATED LINKS</span></span>
