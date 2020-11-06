---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 12e1844be497baa24a3b9b4aa9c4e5690564f4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479578"
---
# <span data-ttu-id="ecac0-101">Restore-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecac0-101">Restore-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ecac0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecac0-102">SYNOPSIS</span></span>
<span data-ttu-id="ecac0-103">Stellt ein verwaltetes Speicherkonto in einem schlüsseltresor aus einer Sicherungsdatei wieder her.</span><span class="sxs-lookup"><span data-stu-id="ecac0-103">Restores a managed storage account in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecac0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecac0-104">SYNTAX</span></span>

### <span data-ttu-id="ecac0-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecac0-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecac0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecac0-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecac0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecac0-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecac0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecac0-108">DESCRIPTION</span></span>
<span data-ttu-id="ecac0-109">Mit dem Cmdlet **Restore-AzureKeyVaultManagedStorageAccount** wird ein verwaltetes Speicherkonto im angegebenen schlüsseltresor aus einer Sicherungsdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="ecac0-109">The **Restore-AzureKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="ecac0-110">Bei diesem verwalteten Speicherkonto handelt es sich um ein Replikat des gesicherten verwalteten speicherkontos in der Eingabedatei, das den gleichen Namen wie das ursprüngliche Konto hat.</span><span class="sxs-lookup"><span data-stu-id="ecac0-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="ecac0-111">Wenn der schlüsseltresor bereits ein verwaltetes Speicherkonto mit demselben Namen enthält, schlägt dieses Cmdlet fehl, anstatt das Original zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ecac0-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="ecac0-112">Der schlüsseltresor, in den Sie das verwaltete Speicherkonto wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie das verwaltete Speicherkonto gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="ecac0-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="ecac0-113">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="ecac0-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ecac0-114">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="ecac0-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ecac0-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecac0-115">EXAMPLES</span></span>

### <span data-ttu-id="ecac0-116">Beispiel 1: Wiederherstellen eines gesicherten verwalteten speicherkontos</span><span class="sxs-lookup"><span data-stu-id="ecac0-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="ecac0-117">Mit diesem Befehl wird ein verwaltetes Speicherkonto, einschließlich aller Versionen, aus der Sicherungsdatei mit dem Namen Backup. BLOB in den schlüsseltresor mit dem Namen MyKeyVault wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ecac0-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ecac0-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecac0-118">PARAMETERS</span></span>

### <span data-ttu-id="ecac0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecac0-119">-DefaultProfile</span></span>
<span data-ttu-id="ecac0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecac0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecac0-121">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="ecac0-121">-InputFile</span></span>
<span data-ttu-id="ecac0-122">Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="ecac0-122">Input file.</span></span>
<span data-ttu-id="ecac0-123">Die Eingabedatei mit dem gesicherten BLOB</span><span class="sxs-lookup"><span data-stu-id="ecac0-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="ecac0-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ecac0-124">-InputObject</span></span>
<span data-ttu-id="ecac0-125">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="ecac0-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecac0-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ecac0-126">-ResourceId</span></span>
<span data-ttu-id="ecac0-127">Keyvault-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ecac0-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecac0-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="ecac0-128">-VaultName</span></span>
<span data-ttu-id="ecac0-129">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="ecac0-129">Vault name.</span></span>
<span data-ttu-id="ecac0-130">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ecac0-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecac0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecac0-131">-Confirm</span></span>
<span data-ttu-id="ecac0-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecac0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecac0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecac0-133">-WhatIf</span></span>
<span data-ttu-id="ecac0-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecac0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecac0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecac0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecac0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecac0-136">CommonParameters</span></span>
<span data-ttu-id="ecac0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecac0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecac0-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecac0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecac0-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecac0-139">INPUTS</span></span>

### <span data-ttu-id="ecac0-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ecac0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="ecac0-141">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ecac0-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ecac0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ecac0-142">System.String</span></span>

## <span data-ttu-id="ecac0-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecac0-143">OUTPUTS</span></span>

### <span data-ttu-id="ecac0-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecac0-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ecac0-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecac0-145">NOTES</span></span>

## <span data-ttu-id="ecac0-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecac0-146">RELATED LINKS</span></span>
