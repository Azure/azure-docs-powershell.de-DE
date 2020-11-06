---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 2805ebfd5849306dadb4cf913660c8fac1602d79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497762"
---
# <span data-ttu-id="9a0b4-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9a0b4-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="9a0b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0b4-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a0b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a0b4-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a0b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a0b4-105">DESCRIPTION</span></span>
<span data-ttu-id="9a0b4-106">Das Cmdlet " **Get-AzureRmBackupRecoveryPoint** " Ruft die Wiederherstellungspunkte für ein gesichertes Azure-Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="9a0b4-107">Nachdem ein Element gesichert wurde, speichert Backup einen oder mehrere Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="9a0b4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a0b4-108">EXAMPLES</span></span>

### <span data-ttu-id="9a0b4-109">Beispiel 1: Abrufen von Wiederherstellungspunkten für ein Element</span><span class="sxs-lookup"><span data-stu-id="9a0b4-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="9a0b4-110">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="9a0b4-111">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9a0b4-112">Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupContainer** einen Container mit dem angegebenen Namen im Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="9a0b4-113">Der Befehl speichert das Objekt in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="9a0b4-114">Der dritte Befehl ruft das Sicherungselement im Container in $Container mit dem Cmdlet **Get-AzureRmBackupItem** ab.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="9a0b4-115">Der Befehl speichert das Objekt in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="9a0b4-116">Der endgültige Befehl ruft Wiederherstellungspunkte für das Element in $BackupItem ab.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="9a0b4-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a0b4-117">PARAMETERS</span></span>

### <span data-ttu-id="9a0b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0b4-118">-DefaultProfile</span></span>
<span data-ttu-id="9a0b4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9a0b4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a0b4-120">-Item</span><span class="sxs-lookup"><span data-stu-id="9a0b4-120">-Item</span></span>
<span data-ttu-id="9a0b4-121">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="9a0b4-122">Verwenden Sie zum Abrufen eines **AzureRmBackupItem** das Get-AzureRmBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0b4-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9a0b4-123">-RecoveryPointId</span></span>
<span data-ttu-id="9a0b4-124">Gibt die ID eines Wiederherstellungspunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9a0b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0b4-125">CommonParameters</span></span>
<span data-ttu-id="9a0b4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0b4-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0b4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0b4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a0b4-128">INPUTS</span></span>

### <span data-ttu-id="9a0b4-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="9a0b4-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="9a0b4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a0b4-130">OUTPUTS</span></span>

### <span data-ttu-id="9a0b4-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9a0b4-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="9a0b4-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a0b4-132">NOTES</span></span>

## <span data-ttu-id="9a0b4-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a0b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="9a0b4-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9a0b4-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="9a0b4-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="9a0b4-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="9a0b4-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9a0b4-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


