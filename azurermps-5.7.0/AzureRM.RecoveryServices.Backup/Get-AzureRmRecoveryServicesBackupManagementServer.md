---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 0dac27b7e17a9336db198906cdfb60fb15738795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478362"
---
# <span data-ttu-id="a0f99-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="a0f99-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="a0f99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0f99-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f99-103">Ruft scdpm-und Azure-Backup-Verwaltungsserver ab.</span><span class="sxs-lookup"><span data-stu-id="a0f99-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0f99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0f99-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0f99-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0f99-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f99-106">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupManagementServer** " Ruft eine Liste der Sicherungs Verwaltungsserver ab, die in einem Tresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="a0f99-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="a0f99-107">Es gibt zwei Arten von Backup-Verwaltungsservern: System Center Data Protection Manager (scdpm) und Azure Backup Management-Server.</span><span class="sxs-lookup"><span data-stu-id="a0f99-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="a0f99-108">Backup-Verwaltungsserver werden separat installiert, um die Backup-Orchestrierung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a0f99-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="a0f99-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0f99-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a0f99-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0f99-110">EXAMPLES</span></span>

### <span data-ttu-id="a0f99-111">Beispiel 1: Abrufen aller Backup-Verwaltungsserver</span><span class="sxs-lookup"><span data-stu-id="a0f99-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="a0f99-112">Dieser Befehl ruft alle Sicherungs Verwaltungsserver ab, die beim Tresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="a0f99-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="a0f99-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0f99-113">PARAMETERS</span></span>

### <span data-ttu-id="a0f99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f99-114">-DefaultProfile</span></span>
<span data-ttu-id="a0f99-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0f99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f99-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a0f99-116">-Name</span></span>
<span data-ttu-id="a0f99-117">Gibt den Namen des abzurufenden Sicherungs Verwaltungsservers an.</span><span class="sxs-lookup"><span data-stu-id="a0f99-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f99-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f99-118">CommonParameters</span></span>
<span data-ttu-id="a0f99-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f99-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f99-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f99-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f99-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0f99-121">INPUTS</span></span>

### <span data-ttu-id="a0f99-122">Keine</span><span class="sxs-lookup"><span data-stu-id="a0f99-122">None</span></span>
<span data-ttu-id="a0f99-123">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a0f99-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0f99-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0f99-124">OUTPUTS</span></span>

### <span data-ttu-id="a0f99-125">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="a0f99-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="a0f99-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. BackupEngineBase]</span><span class="sxs-lookup"><span data-stu-id="a0f99-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="a0f99-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0f99-127">NOTES</span></span>

## <span data-ttu-id="a0f99-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0f99-128">RELATED LINKS</span></span>

[<span data-ttu-id="a0f99-129">Registrierung aufheben-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="a0f99-129">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


