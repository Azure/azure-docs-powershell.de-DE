---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: f82abc45a9b78093c13764ab0eb28f2593c7fabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498474"
---
# <span data-ttu-id="b049e-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b049e-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="b049e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b049e-102">SYNOPSIS</span></span>
<span data-ttu-id="b049e-103">Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.</span><span class="sxs-lookup"><span data-stu-id="b049e-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b049e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b049e-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b049e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b049e-105">DESCRIPTION</span></span>
<span data-ttu-id="b049e-106">Das Cmdlet " **Get-AzureRmBackupRecoveryPoint** " Ruft die Wiederherstellungspunkte für ein gesichertes Azure-Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="b049e-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="b049e-107">Nachdem ein Element gesichert wurde, speichert Backup einen oder mehrere Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="b049e-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="b049e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b049e-108">EXAMPLES</span></span>

### <span data-ttu-id="b049e-109">Beispiel 1: Abrufen von Wiederherstellungspunkten für ein Element</span><span class="sxs-lookup"><span data-stu-id="b049e-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="b049e-110">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="b049e-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="b049e-111">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="b049e-111">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="b049e-112">Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupContainer** einen Container mit dem angegebenen Namen im Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="b049e-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="b049e-113">Der Befehl speichert das Objekt in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="b049e-113">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="b049e-114">Der dritte Befehl ruft das Sicherungselement im Container in $Container mit dem Cmdlet **Get-AzureRmBackupItem** ab.</span><span class="sxs-lookup"><span data-stu-id="b049e-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="b049e-115">Der Befehl speichert das Objekt in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="b049e-115">The command stores that object in the $BackupItem variable.</span></span>
<span data-ttu-id="b049e-116">Der endgültige Befehl ruft Wiederherstellungspunkte für das Element in $BackupItem ab.</span><span class="sxs-lookup"><span data-stu-id="b049e-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="b049e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b049e-117">PARAMETERS</span></span>

### <span data-ttu-id="b049e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b049e-118">-DefaultProfile</span></span>
<span data-ttu-id="b049e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b049e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b049e-120">-Item</span><span class="sxs-lookup"><span data-stu-id="b049e-120">-Item</span></span>
<span data-ttu-id="b049e-121">Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.</span><span class="sxs-lookup"><span data-stu-id="b049e-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="b049e-122">Verwenden Sie zum Abrufen eines **AzureRmBackupItem** das Get-AzureRmBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b049e-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="b049e-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="b049e-123">-RecoveryPointId</span></span>
<span data-ttu-id="b049e-124">Gibt die ID eines Wiederherstellungspunkts an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b049e-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b049e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b049e-125">CommonParameters</span></span>
<span data-ttu-id="b049e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b049e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b049e-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b049e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b049e-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b049e-128">INPUTS</span></span>

### <span data-ttu-id="b049e-129">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="b049e-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="b049e-130">Parameter: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b049e-130">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="b049e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b049e-131">OUTPUTS</span></span>

### <span data-ttu-id="b049e-132">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b049e-132">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint</span></span>

## <span data-ttu-id="b049e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b049e-133">NOTES</span></span>

## <span data-ttu-id="b049e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b049e-134">RELATED LINKS</span></span>

[<span data-ttu-id="b049e-135">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b049e-135">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b049e-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b049e-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="b049e-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b049e-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


