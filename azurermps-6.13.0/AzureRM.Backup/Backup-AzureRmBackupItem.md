---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: e87ab3ec04378dc97e144d2b444ee5398ff4f4f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502249"
---
# <span data-ttu-id="f3c40-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f3c40-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="f3c40-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3c40-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c40-103">Startet eine Sicherung für ein Sicherungselement.</span><span class="sxs-lookup"><span data-stu-id="f3c40-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c40-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3c40-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3c40-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3c40-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c40-106">Das Cmdlet **Backup-AzureRmBackupItem** startet eine Sicherung für ein geschütztes Azure-Sicherungselement, das nicht an den Sicherungszeitplan gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f3c40-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="f3c40-107">Sie können eine erste Sicherung unmittelbar nach dem Aktivieren des Schutzes durchführen oder eine Sicherung starten, nachdem eine geplante Sicherung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="f3c40-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="f3c40-108">Wenn ein vorhandener Backup-Auftrag ausgeführt wird, schlägt dieses Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="f3c40-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="f3c40-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3c40-109">EXAMPLES</span></span>

### <span data-ttu-id="f3c40-110">Beispiel 1: Starten der Sicherung eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="f3c40-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="f3c40-111">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f3c40-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="f3c40-112">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="f3c40-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="f3c40-113">Der zweite Befehl ruft mithilfe des Get-AzureRmBackupContainer-Cmdlets einen Container ab, der den angegebenen Namen im Tresor in $Vault aufweist.</span><span class="sxs-lookup"><span data-stu-id="f3c40-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="f3c40-114">Der Befehl speichert das Objekt in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="f3c40-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="f3c40-115">Der letzte Befehl ruft die Sicherungselemente in $Container mithilfe des Get-AzureRmBackupItem-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f3c40-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="f3c40-116">Der Befehl übergibt die Elemente mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3c40-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f3c40-117">Das aktuelle Cmdlet beginnt mit dem Sichern des virtuellen Computers im Container.</span><span class="sxs-lookup"><span data-stu-id="f3c40-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="f3c40-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3c40-118">PARAMETERS</span></span>

### <span data-ttu-id="f3c40-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c40-119">-DefaultProfile</span></span>
<span data-ttu-id="f3c40-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3c40-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3c40-121">-Item</span><span class="sxs-lookup"><span data-stu-id="f3c40-121">-Item</span></span>
<span data-ttu-id="f3c40-122">Gibt ein Sicherungselement an, für das dieses Cmdlet einen Sicherungsvorgang startet.</span><span class="sxs-lookup"><span data-stu-id="f3c40-122">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c40-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c40-123">CommonParameters</span></span>
<span data-ttu-id="f3c40-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c40-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c40-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c40-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c40-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3c40-126">INPUTS</span></span>

### <span data-ttu-id="f3c40-127">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="f3c40-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="f3c40-128">Parameter: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3c40-128">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="f3c40-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3c40-129">OUTPUTS</span></span>

### <span data-ttu-id="f3c40-130">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="f3c40-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="f3c40-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3c40-131">NOTES</span></span>

## <span data-ttu-id="f3c40-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3c40-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3c40-133">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f3c40-133">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="f3c40-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f3c40-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="f3c40-135">Wiederherstellen – AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f3c40-135">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


