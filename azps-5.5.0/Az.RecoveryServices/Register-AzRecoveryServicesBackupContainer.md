---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156521"
---
# <span data-ttu-id="64466-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="64466-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="64466-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64466-102">SYNOPSIS</span></span>
<span data-ttu-id="64466-103">Das **Cmdlet Register-AzRecoveryServicesBackupContainer** registriert eine Azure VM für AzureWorkloads mit einem bestimmten WorkloadType.</span><span class="sxs-lookup"><span data-stu-id="64466-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="64466-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64466-104">SYNTAX</span></span>

### <span data-ttu-id="64466-105">Registrieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="64466-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64466-106">Erneut registrieren</span><span class="sxs-lookup"><span data-stu-id="64466-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64466-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64466-107">DESCRIPTION</span></span>
<span data-ttu-id="64466-108">Mit diesem Befehl kann Azure Backup die Ressource in einen Sicherungscontainer konvertieren, der dann im angegebenen Tresor für Wiederherstellungsdienste registriert wird.</span><span class="sxs-lookup"><span data-stu-id="64466-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="64466-109">Der Azure Backup Service kann dann Workloads des angegebenen Workloadtyps innerhalb dieses Containers ermitteln, um später geschützt zu werden.</span><span class="sxs-lookup"><span data-stu-id="64466-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="64466-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64466-110">EXAMPLES</span></span>

### <span data-ttu-id="64466-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64466-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="64466-112">Das Cmdlet registriert eine azure VM als Container für die MSSQL-Workload.</span><span class="sxs-lookup"><span data-stu-id="64466-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="64466-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64466-113">PARAMETERS</span></span>

### <span data-ttu-id="64466-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="64466-114">-BackupManagementType</span></span>
<span data-ttu-id="64466-115">Die Klasse der geschützten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="64466-115">The class of resources being protected.</span></span> <span data-ttu-id="64466-116">Derzeit wird für dieses Cmdlet AzureWorkload unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64466-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="64466-117">-Container</span><span class="sxs-lookup"><span data-stu-id="64466-117">-Container</span></span>
<span data-ttu-id="64466-118">Container, in dem sich das Element befindet</span><span class="sxs-lookup"><span data-stu-id="64466-118">Container where the item resides</span></span>

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

### <span data-ttu-id="64466-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64466-119">-DefaultProfile</span></span>
<span data-ttu-id="64466-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64466-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64466-121">-Force</span><span class="sxs-lookup"><span data-stu-id="64466-121">-Force</span></span>
<span data-ttu-id="64466-122">Erzwingen des Registrierungscontainers (Bestätigungsdialogfeld wird verhindert).</span><span class="sxs-lookup"><span data-stu-id="64466-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="64466-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="64466-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="64466-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64466-124">-ResourceId</span></span>
<span data-ttu-id="64466-125">DIE ID der Azure-Ressource, deren repräsentatives Element überprüft werden muss, wenn es bereits durch einen Wiederherstellungsservicestresor im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="64466-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="64466-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="64466-126">-VaultId</span></span>
<span data-ttu-id="64466-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="64466-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="64466-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="64466-128">-WorkloadType</span></span>
<span data-ttu-id="64466-129">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="64466-129">Workload type of the resource.</span></span> <span data-ttu-id="64466-130">Der aktuell unterstützte Wert ist AzureVM, WindowsServer, AzureFiles, MSSQL.</span><span class="sxs-lookup"><span data-stu-id="64466-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="64466-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64466-131">-Confirm</span></span>
<span data-ttu-id="64466-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64466-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64466-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="64466-133">-WhatIf</span></span>
<span data-ttu-id="64466-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64466-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="64466-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64466-135">CommonParameters</span></span>
<span data-ttu-id="64466-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64466-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64466-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64466-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64466-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64466-138">INPUTS</span></span>

### <span data-ttu-id="64466-139">System.String</span><span class="sxs-lookup"><span data-stu-id="64466-139">System.String</span></span>

## <span data-ttu-id="64466-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64466-140">OUTPUTS</span></span>

### <span data-ttu-id="64466-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="64466-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="64466-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64466-142">NOTES</span></span>

## <span data-ttu-id="64466-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64466-143">RELATED LINKS</span></span>
