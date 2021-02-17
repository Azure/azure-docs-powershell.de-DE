---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156561"
---
# <span data-ttu-id="06ba5-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="06ba5-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="06ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="06ba5-103">Ruft SCDPM- und Azure Backup Management Servers ab.</span><span class="sxs-lookup"><span data-stu-id="06ba5-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="06ba5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06ba5-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06ba5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="06ba5-106">Das **Cmdlet "Get-AzRecoveryServicesBackupManagementServer"** ruft eine Liste der Sicherungsverwaltungsserver ab, die in einem Tresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="06ba5-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="06ba5-107">Es gibt zwei Arten von Sicherungsverwaltungsservern: System Center Data Protection Manager (SCDPM) und Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="06ba5-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="06ba5-108">Sicherungsverwaltungsserver werden separat installiert, um die Sicherungs orchestrierung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="06ba5-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="06ba5-109">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="06ba5-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="06ba5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06ba5-110">EXAMPLES</span></span>

### <span data-ttu-id="06ba5-111">Beispiel 1: Alle Sicherungsverwaltungsserver erhalten</span><span class="sxs-lookup"><span data-stu-id="06ba5-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="06ba5-112">Dieser Befehl ruft alle Sicherungsverwaltungsserver ab, die beim Tresor registriert sind.</span><span class="sxs-lookup"><span data-stu-id="06ba5-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="06ba5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06ba5-113">PARAMETERS</span></span>

### <span data-ttu-id="06ba5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ba5-114">-DefaultProfile</span></span>
<span data-ttu-id="06ba5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06ba5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ba5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="06ba5-116">-Name</span></span>
<span data-ttu-id="06ba5-117">Gibt den Namen des Sicherungsverwaltungsservers an, den Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="06ba5-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="06ba5-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="06ba5-118">-VaultId</span></span>
<span data-ttu-id="06ba5-119">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="06ba5-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="06ba5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ba5-120">CommonParameters</span></span>
<span data-ttu-id="06ba5-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ba5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ba5-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06ba5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ba5-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06ba5-123">INPUTS</span></span>

### <span data-ttu-id="06ba5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="06ba5-124">System.String</span></span>

## <span data-ttu-id="06ba5-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06ba5-125">OUTPUTS</span></span>

### <span data-ttu-id="06ba5-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="06ba5-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="06ba5-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="06ba5-127">NOTES</span></span>

## <span data-ttu-id="06ba5-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="06ba5-128">RELATED LINKS</span></span>

[<span data-ttu-id="06ba5-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="06ba5-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


