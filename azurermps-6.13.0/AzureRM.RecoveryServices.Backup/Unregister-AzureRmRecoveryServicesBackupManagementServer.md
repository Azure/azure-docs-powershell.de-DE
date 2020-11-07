---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 4ef306b80aaf5fbb03b5ee4e98104829d8853ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663113"
---
# <span data-ttu-id="55231-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="55231-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="55231-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55231-102">SYNOPSIS</span></span>
<span data-ttu-id="55231-103">Hebt die Registrierung eines scdpm-Servers oder-Sicherungsservers vom Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="55231-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55231-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55231-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55231-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55231-105">DESCRIPTION</span></span>
<span data-ttu-id="55231-106">Das Cmdlet " **Unregister-AzureRmRecoveryServicesBackupManagementServer** " hebt die Registrierung eines System Center Data Protection Manager (scdpm)-Servers oder eines Azure Backup-Servers aus dem Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="55231-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="55231-107">Dieses Cmdlet entfernt Verweise auf die Server, die aus dem Tresor nicht registriert sind.</span><span class="sxs-lookup"><span data-stu-id="55231-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="55231-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55231-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="55231-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="55231-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="55231-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55231-110">EXAMPLES</span></span>

### <span data-ttu-id="55231-111">Beispiel 1: Aufheben der Registrierung eines scdpm-Servers aus dem Tresor</span><span class="sxs-lookup"><span data-stu-id="55231-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="55231-112">Der erste Befehl ruft den Sicherungs Verwaltungsserver mit dem Namen dpmserver01.contoso.com ab und speichert ihn dann in der $BMS Variablen.</span><span class="sxs-lookup"><span data-stu-id="55231-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="55231-113">Mit dem zweiten Befehl wird der scdpm-Server aus dem Tresor aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="55231-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="55231-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="55231-114">PARAMETERS</span></span>

### <span data-ttu-id="55231-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="55231-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="55231-116">Gibt ein scdpm-Serverobjekt an, dessen Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="55231-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="55231-117">Verwenden Sie das Get-AzureRmRecoveryServicesBackupManagementServer-Cmdlet, um ein **BackupManagementServer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="55231-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="55231-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55231-118">-DefaultProfile</span></span>
<span data-ttu-id="55231-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55231-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55231-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55231-120">-PassThru</span></span>
<span data-ttu-id="55231-121">Geben Sie den zu löschenden Backup-Verwaltungs Server zurück.</span><span class="sxs-lookup"><span data-stu-id="55231-121">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="55231-122">-Tresor</span><span class="sxs-lookup"><span data-stu-id="55231-122">-VaultId</span></span>
<span data-ttu-id="55231-123">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="55231-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="55231-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55231-124">-Confirm</span></span>
<span data-ttu-id="55231-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55231-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55231-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55231-126">-WhatIf</span></span>
<span data-ttu-id="55231-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55231-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55231-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55231-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55231-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55231-129">CommonParameters</span></span>
<span data-ttu-id="55231-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55231-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55231-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55231-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55231-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55231-132">INPUTS</span></span>

### <span data-ttu-id="55231-133">System. String</span><span class="sxs-lookup"><span data-stu-id="55231-133">System.String</span></span>
<span data-ttu-id="55231-134">Parameter: Vault-ByValue</span><span class="sxs-lookup"><span data-stu-id="55231-134">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="55231-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55231-135">OUTPUTS</span></span>

### <span data-ttu-id="55231-136">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="55231-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="55231-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="55231-137">NOTES</span></span>

## <span data-ttu-id="55231-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55231-138">RELATED LINKS</span></span>

[<span data-ttu-id="55231-139">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="55231-139">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


