---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 5452758a5cf269ef50475b8962e5fbca117dbb1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659788"
---
# <span data-ttu-id="ae846-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="ae846-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="ae846-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae846-102">SYNOPSIS</span></span>
<span data-ttu-id="ae846-103">Hebt die Registrierung eines scdpm-Servers oder-Sicherungsservers vom Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="ae846-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="ae846-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae846-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae846-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae846-105">DESCRIPTION</span></span>
<span data-ttu-id="ae846-106">Das Cmdlet " **Unregister-AzRecoveryServicesBackupManagementServer** " hebt die Registrierung eines System Center Data Protection Manager (scdpm)-Servers oder eines Azure Backup-Servers aus dem Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="ae846-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="ae846-107">Dieses Cmdlet entfernt Verweise auf die Server, die aus dem Tresor nicht registriert sind.</span><span class="sxs-lookup"><span data-stu-id="ae846-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="ae846-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ae846-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="ae846-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae846-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ae846-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae846-110">EXAMPLES</span></span>

### <span data-ttu-id="ae846-111">Beispiel 1: Aufheben der Registrierung eines scdpm-Servers aus dem Tresor</span><span class="sxs-lookup"><span data-stu-id="ae846-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="ae846-112">Der erste Befehl ruft den Sicherungs Verwaltungsserver mit dem Namen dpmserver01.contoso.com ab und speichert ihn dann in der $BMS Variablen.</span><span class="sxs-lookup"><span data-stu-id="ae846-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="ae846-113">Mit dem zweiten Befehl wird der scdpm-Server aus dem Tresor aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="ae846-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="ae846-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae846-114">PARAMETERS</span></span>

### <span data-ttu-id="ae846-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="ae846-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="ae846-116">Der Sicherungs Container für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="ae846-116">The recovery services backup container.</span></span>

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

### <span data-ttu-id="ae846-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae846-117">-DefaultProfile</span></span>
<span data-ttu-id="ae846-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae846-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae846-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae846-119">-PassThru</span></span>
<span data-ttu-id="ae846-120">Geben Sie den zu löschenden Backup-Verwaltungs Server zurück.</span><span class="sxs-lookup"><span data-stu-id="ae846-120">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="ae846-121">-Tresor</span><span class="sxs-lookup"><span data-stu-id="ae846-121">-VaultId</span></span>
<span data-ttu-id="ae846-122">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="ae846-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ae846-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae846-123">-Confirm</span></span>
<span data-ttu-id="ae846-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae846-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae846-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae846-125">-WhatIf</span></span>
<span data-ttu-id="ae846-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae846-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae846-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae846-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae846-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae846-128">CommonParameters</span></span>
<span data-ttu-id="ae846-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae846-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae846-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae846-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae846-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae846-131">INPUTS</span></span>

### <span data-ttu-id="ae846-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ae846-132">System.String</span></span>

## <span data-ttu-id="ae846-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae846-133">OUTPUTS</span></span>

### <span data-ttu-id="ae846-134">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="ae846-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="ae846-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae846-135">NOTES</span></span>

## <span data-ttu-id="ae846-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae846-136">RELATED LINKS</span></span>

[<span data-ttu-id="ae846-137">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="ae846-137">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


