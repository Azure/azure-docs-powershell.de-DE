---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480561"
---
# <span data-ttu-id="e2329-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e2329-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="e2329-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2329-102">SYNOPSIS</span></span>
<span data-ttu-id="e2329-103">Ändert den Speichertyp eines Sicherungs Depots.</span><span class="sxs-lookup"><span data-stu-id="e2329-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2329-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2329-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2329-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2329-105">DESCRIPTION</span></span>
<span data-ttu-id="e2329-106">Das Cmdlet " **Satz-AzureRmBackupVault** " ändert den Speichertyp eines Azure Backup Vaults.</span><span class="sxs-lookup"><span data-stu-id="e2329-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="e2329-107">Sie können andere Eigenschaften eines Tresors nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e2329-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="e2329-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2329-108">EXAMPLES</span></span>

### <span data-ttu-id="e2329-109">Beispiel 1: Ändern des Speichers für einen vorhandenen Tresor</span><span class="sxs-lookup"><span data-stu-id="e2329-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="e2329-110">Dieser Befehl ruft das Azure Backup Vault mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="e2329-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="e2329-111">Der Befehl übergibt diesen Tresor mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2329-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e2329-112">Das aktuelle Cmdlet ändert den Speichertyp in LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="e2329-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="e2329-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2329-113">PARAMETERS</span></span>

### <span data-ttu-id="e2329-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2329-114">-DefaultProfile</span></span>
<span data-ttu-id="e2329-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e2329-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2329-116">-Speicher</span><span class="sxs-lookup"><span data-stu-id="e2329-116">-Storage</span></span>
<span data-ttu-id="e2329-117">Gibt den Speichertyp für die Sicherungsdaten an.</span><span class="sxs-lookup"><span data-stu-id="e2329-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="e2329-118">Die zulässigen Werte für diesen Parameter sind: LocallyRedundant und georedundant.</span><span class="sxs-lookup"><span data-stu-id="e2329-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2329-119">-Vault</span><span class="sxs-lookup"><span data-stu-id="e2329-119">-Vault</span></span>
<span data-ttu-id="e2329-120">Gibt ein Sicherungs Depot an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e2329-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="e2329-121">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e2329-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2329-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2329-122">CommonParameters</span></span>
<span data-ttu-id="e2329-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2329-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2329-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2329-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2329-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2329-125">INPUTS</span></span>

### <span data-ttu-id="e2329-126">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="e2329-126">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="e2329-127">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2329-127">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="e2329-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2329-128">OUTPUTS</span></span>

### <span data-ttu-id="e2329-129">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="e2329-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="e2329-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2329-130">NOTES</span></span>
* <span data-ttu-id="e2329-131">Wenn Sie den ersten Server oder virtuellen Computer für einen Tresor registrieren, ist der Speichertyp gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e2329-131">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="e2329-132">Anschließend können Sie den Speichertyp nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e2329-132">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="e2329-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2329-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2329-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e2329-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="e2329-135">Neu – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e2329-135">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="e2329-136">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e2329-136">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


