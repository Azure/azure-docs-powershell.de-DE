---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: cc52435ff0b288656e4a917620659737f33916ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460879"
---
# <span data-ttu-id="4541b-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="4541b-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="4541b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4541b-102">SYNOPSIS</span></span>
<span data-ttu-id="4541b-103">Die Registrierung eines SCDPM- oder Sicherungsservers aus dem Tresor wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="4541b-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="4541b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4541b-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4541b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4541b-105">DESCRIPTION</span></span>
<span data-ttu-id="4541b-106">Das **Cmdlet "Unregister-AzRecoveryServicesBackupManagementServer"** registriert einen System Center Data Protection Manager (SCDPM)-Server oder einen Azure Backup Server aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="4541b-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="4541b-107">Mit diesem Cmdlet werden Verweise auf die Server entfernt, deren Registrierung im Tresor aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="4541b-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="4541b-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle mit diesem Container verknüpften geschützten Daten löschen.</span><span class="sxs-lookup"><span data-stu-id="4541b-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="4541b-109">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="4541b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4541b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4541b-110">EXAMPLES</span></span>

### <span data-ttu-id="4541b-111">Beispiel 1: Aufheben der Registrierung eines SCDPM-Servers aus dem Tresor</span><span class="sxs-lookup"><span data-stu-id="4541b-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```powershell
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="4541b-112">Der erste Befehl ruft den Sicherungsverwaltungsserver mit dem Namen dpmserver01.contoso.com und speichert ihn dann in der $BMS Variable.</span><span class="sxs-lookup"><span data-stu-id="4541b-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="4541b-113">Mit dem zweiten Befehl wird die Registrierung des SCDPM-Servers aus dem Tresor aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="4541b-113">The second command unregisters the SCDPM server from the vault.</span></span>

### <span data-ttu-id="4541b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4541b-114">Example 2</span></span>

<span data-ttu-id="4541b-115">Die Registrierung eines SCDPM- oder Sicherungsservers aus dem Tresor wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="4541b-115">Unregisters a SCDPM server or Backup server from the vault.</span></span> <span data-ttu-id="4541b-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="4541b-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer <BackupEngineBase> -VaultId $vault.ID
```

## <span data-ttu-id="4541b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4541b-117">PARAMETERS</span></span>

### <span data-ttu-id="4541b-118">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="4541b-118">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="4541b-119">Der Sicherungscontainer für die Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="4541b-119">The recovery services backup container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4541b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4541b-120">-DefaultProfile</span></span>
<span data-ttu-id="4541b-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4541b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4541b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4541b-122">-PassThru</span></span>
<span data-ttu-id="4541b-123">Geben Sie den sicherungsverwaltungsserver zurück, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4541b-123">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="4541b-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4541b-124">-VaultId</span></span>
<span data-ttu-id="4541b-125">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="4541b-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4541b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4541b-126">-Confirm</span></span>
<span data-ttu-id="4541b-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4541b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4541b-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4541b-128">-WhatIf</span></span>
<span data-ttu-id="4541b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4541b-129">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="4541b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4541b-130">CommonParameters</span></span>
<span data-ttu-id="4541b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4541b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4541b-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4541b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4541b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4541b-133">INPUTS</span></span>

### <span data-ttu-id="4541b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4541b-134">System.String</span></span>

## <span data-ttu-id="4541b-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4541b-135">OUTPUTS</span></span>

### <span data-ttu-id="4541b-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="4541b-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="4541b-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4541b-137">NOTES</span></span>

## <span data-ttu-id="4541b-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4541b-138">RELATED LINKS</span></span>

[<span data-ttu-id="4541b-139">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="4541b-139">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


