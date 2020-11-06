---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: a6415d941646f335ba7cae4fc2aab39d75000ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497926"
---
# <span data-ttu-id="7990b-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7990b-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="7990b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7990b-102">SYNOPSIS</span></span>
<span data-ttu-id="7990b-103">Erstellt einen Sicherungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7990b-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7990b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7990b-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7990b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7990b-105">DESCRIPTION</span></span>
<span data-ttu-id="7990b-106">Mit dem Cmdlet **New-AzureRmBackupVault** wird ein Azure Backup Vault erstellt.</span><span class="sxs-lookup"><span data-stu-id="7990b-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="7990b-107">Dieses Cmdlet gibt ein **AzureRmBackupVault** -Objekt zurück, das als Verweis auf die Vault-Entität fungiert.</span><span class="sxs-lookup"><span data-stu-id="7990b-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="7990b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7990b-108">EXAMPLES</span></span>

### <span data-ttu-id="7990b-109">Beispiel 1: Erstellen eines Sicherungsspeichers</span><span class="sxs-lookup"><span data-stu-id="7990b-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="7990b-110">Mit diesem Befehl wird ein Azure Backup Vault mit dem Namen "Vault03" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7990b-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="7990b-111">Der Tresor befindet sich in der Ressourcengruppe namens ResourceGroup01 in der Region West USA.</span><span class="sxs-lookup"><span data-stu-id="7990b-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="7990b-112">Im Tresor wird der standardmäßige georedundante Speichertyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="7990b-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="7990b-113">Beispiel 2: Erstellen eines Sicherungs Depots, in dem lokal redundanter Speicher verwendet wird</span><span class="sxs-lookup"><span data-stu-id="7990b-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="7990b-114">Mit diesem Befehl wird ein Azure Backup Vault mit dem Namen "Vault03" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7990b-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="7990b-115">Der Tresor befindet sich in der Ressourcengruppe namens ResourceGroup02 in der Region West USA.</span><span class="sxs-lookup"><span data-stu-id="7990b-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="7990b-116">Im Tresor wird der LocallyRedundant-Speichertyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="7990b-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="7990b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7990b-117">PARAMETERS</span></span>

### <span data-ttu-id="7990b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7990b-118">-Name</span></span>
<span data-ttu-id="7990b-119">Gibt einen Namen für den Azure Backup Vault an.</span><span class="sxs-lookup"><span data-stu-id="7990b-119">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="7990b-120">Der Name muss in einer Ressourcengruppe eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7990b-120">The name must be unique in a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7990b-121">-Region</span><span class="sxs-lookup"><span data-stu-id="7990b-121">-Region</span></span>
<span data-ttu-id="7990b-122">Gibt einen Azure-Bereich an, in dem der sicherungstresor vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7990b-122">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="7990b-123">Für Szenarien mit Hybrid-Backup empfehlen wir, dass Sie einen Tresor in einer Region in der Nähe des lokalen Servers erstellen, um die Latenz zu verringern.</span><span class="sxs-lookup"><span data-stu-id="7990b-123">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="7990b-124">Für Backups von Azure Infrastructure as a Service (IaaS) Virtual Machines wird der Tresor zum Ermittlungspunkt für lokale virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="7990b-124">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7990b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7990b-125">-ResourceGroupName</span></span>
<span data-ttu-id="7990b-126">Gibt den Namen einer vorhandenen Azure-Ressourcengruppe an, in der mit diesem Cmdlet ein Sicherungsspeicher erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7990b-126">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="7990b-127">Verwenden Sie das New-AzureRMResourceGroup-Cmdlet, um eine Ressourcengruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7990b-127">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="7990b-128">Die Ressourcengruppe und der Azure Backup Vault müssen sich nicht in der gleichen Region befinden.</span><span class="sxs-lookup"><span data-stu-id="7990b-128">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7990b-129">-Speicher</span><span class="sxs-lookup"><span data-stu-id="7990b-129">-Storage</span></span>
<span data-ttu-id="7990b-130">Gibt den Speichertyp für die Sicherungsdaten an.</span><span class="sxs-lookup"><span data-stu-id="7990b-130">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="7990b-131">Die zulässigen Werte für diesen Parameter sind: LocallyRedundant und georedundant.</span><span class="sxs-lookup"><span data-stu-id="7990b-131">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="7990b-132">Der Standardwert ist georedundant.</span><span class="sxs-lookup"><span data-stu-id="7990b-132">The default value is GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7990b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7990b-133">-DefaultProfile</span></span>
<span data-ttu-id="7990b-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7990b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7990b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7990b-135">CommonParameters</span></span>
<span data-ttu-id="7990b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7990b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7990b-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7990b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7990b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7990b-138">INPUTS</span></span>

### <span data-ttu-id="7990b-139">Keine</span><span class="sxs-lookup"><span data-stu-id="7990b-139">None</span></span>

## <span data-ttu-id="7990b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7990b-140">OUTPUTS</span></span>

### <span data-ttu-id="7990b-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7990b-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="7990b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="7990b-142">NOTES</span></span>
* <span data-ttu-id="7990b-143">Keine</span><span class="sxs-lookup"><span data-stu-id="7990b-143">None</span></span>

## <span data-ttu-id="7990b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7990b-144">RELATED LINKS</span></span>

[<span data-ttu-id="7990b-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7990b-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="7990b-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7990b-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="7990b-147">Satz-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7990b-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


