---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175916"
---
# <span data-ttu-id="e91fa-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e91fa-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="e91fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e91fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e91fa-103">Ruft scdpm-und Azure-Backup-Verwaltungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="e91fa-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="e91fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e91fa-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e91fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e91fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e91fa-106">Das Cmdlet " **Get-AzRecoveryServicesBackupManagementServer** " Ruft eine Liste der Sicherungs Verwaltungsserver ab, die in einem Tresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="e91fa-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="e91fa-107">Es gibt zwei Arten von Backup-Verwaltungsservern: System Center Data Protection Manager (scdpm) und Azure Backup Management-Server.</span><span class="sxs-lookup"><span data-stu-id="e91fa-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="e91fa-108">Backup-Verwaltungsserver werden separat installiert, um die Backup-Orchestrierung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e91fa-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="e91fa-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="e91fa-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e91fa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e91fa-110">EXAMPLES</span></span>

### <span data-ttu-id="e91fa-111">Beispiel 1: Abrufen aller Backup-Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="e91fa-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="e91fa-112">Dieser Befehl ruft alle Sicherungs Verwaltungsserver ab, die beim Tresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="e91fa-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="e91fa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e91fa-113">PARAMETERS</span></span>

### <span data-ttu-id="e91fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91fa-114">-DefaultProfile</span></span>
<span data-ttu-id="e91fa-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e91fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e91fa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e91fa-116">-Name</span></span>
<span data-ttu-id="e91fa-117">Gibt den Namen des abzurufenden Sicherungs Verwaltungsservers an.</span><span class="sxs-lookup"><span data-stu-id="e91fa-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="e91fa-118">-Tresor</span><span class="sxs-lookup"><span data-stu-id="e91fa-118">-VaultId</span></span>
<span data-ttu-id="e91fa-119">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="e91fa-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e91fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91fa-120">CommonParameters</span></span>
<span data-ttu-id="e91fa-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91fa-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e91fa-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91fa-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e91fa-123">INPUTS</span></span>

### <span data-ttu-id="e91fa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e91fa-124">System.String</span></span>

## <span data-ttu-id="e91fa-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e91fa-125">OUTPUTS</span></span>

### <span data-ttu-id="e91fa-126">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="e91fa-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="e91fa-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="e91fa-127">NOTES</span></span>

## <span data-ttu-id="e91fa-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e91fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="e91fa-129">Registrierung aufheben-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="e91fa-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


