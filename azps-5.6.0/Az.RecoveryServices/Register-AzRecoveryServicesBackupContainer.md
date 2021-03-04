---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 83a0e4edd82bd77358df1d95b53e388bb35a9e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919264"
---
# <span data-ttu-id="6ad9b-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6ad9b-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="6ad9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad9b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad9b-103">Das **Cmdlet Register-AzRecoveryServicesBackupContainer** registriert eine Azure VM für AzureWorkloads mit einem bestimmten WorkloadType.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="6ad9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ad9b-104">SYNTAX</span></span>

### <span data-ttu-id="6ad9b-105">Registrieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ad9b-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad9b-106">Erneute Registrierung</span><span class="sxs-lookup"><span data-stu-id="6ad9b-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad9b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ad9b-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad9b-108">Mit diesem Befehl kann Azure Backup die Ressource in einen Sicherungscontainer konvertieren, der dann im angegebenen Wiederherstellungsdienste-Tresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="6ad9b-109">Der Azure Backup-Dienst kann dann Workloads des angegebenen Workloadtyps in diesem Container ermitteln, die später geschützt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="6ad9b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ad9b-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad9b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ad9b-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="6ad9b-112">Das Cmdlet registriert eine azure VM als Container für die MsSQL-Arbeitsauslastung.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="6ad9b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ad9b-113">PARAMETERS</span></span>

### <span data-ttu-id="6ad9b-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6ad9b-114">-BackupManagementType</span></span>
<span data-ttu-id="6ad9b-115">Die Klasse der zu schützenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-115">The class of resources being protected.</span></span> <span data-ttu-id="6ad9b-116">Der für dieses Cmdlet unterstützte Wert ist derzeit AzureWorkload.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="6ad9b-117">-Container</span><span class="sxs-lookup"><span data-stu-id="6ad9b-117">-Container</span></span>
<span data-ttu-id="6ad9b-118">Container, in dem sich das Element befindet</span><span class="sxs-lookup"><span data-stu-id="6ad9b-118">Container where the item resides</span></span>

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

### <span data-ttu-id="6ad9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad9b-119">-DefaultProfile</span></span>
<span data-ttu-id="6ad9b-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad9b-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="6ad9b-121">-Force</span></span>
<span data-ttu-id="6ad9b-122">Erzwingen des Registrierungscontainers (bestätigungsdialogfeld wird verhindert).</span><span class="sxs-lookup"><span data-stu-id="6ad9b-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="6ad9b-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="6ad9b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad9b-124">-ResourceId</span></span>
<span data-ttu-id="6ad9b-125">ID der Azure-Ressource, deren repräsentatives Element überprüft werden muss, wenn es bereits durch einen RecoveryServices-Tresor im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="6ad9b-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6ad9b-126">-VaultId</span></span>
<span data-ttu-id="6ad9b-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6ad9b-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="6ad9b-128">-WorkloadType</span></span>
<span data-ttu-id="6ad9b-129">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-129">Workload type of the resource.</span></span> <span data-ttu-id="6ad9b-130">Der aktuelle unterstützte Wert ist AzureVM, WindowsServer, AzureFiles, MSSQL.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="6ad9b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ad9b-131">-Confirm</span></span>
<span data-ttu-id="6ad9b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad9b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad9b-133">-WhatIf</span></span>
<span data-ttu-id="6ad9b-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="6ad9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad9b-135">CommonParameters</span></span>
<span data-ttu-id="6ad9b-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad9b-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ad9b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad9b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ad9b-138">INPUTS</span></span>

### <span data-ttu-id="6ad9b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6ad9b-139">System.String</span></span>

## <span data-ttu-id="6ad9b-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ad9b-140">OUTPUTS</span></span>

### <span data-ttu-id="6ad9b-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="6ad9b-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="6ad9b-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6ad9b-142">NOTES</span></span>

## <span data-ttu-id="6ad9b-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6ad9b-143">RELATED LINKS</span></span>
