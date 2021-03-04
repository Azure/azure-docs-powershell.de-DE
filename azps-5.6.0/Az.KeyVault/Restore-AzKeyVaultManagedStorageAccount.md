---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 136469819a43dbb918aefebd8134b38ef4a943c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918851"
---
# <span data-ttu-id="b1cc9-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1cc9-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="b1cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cc9-103">Stellt ein verwaltetes Speicherkonto in einem Schlüsseltresor aus einer Sicherungsdatei wieder her.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="b1cc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1cc9-104">SYNTAX</span></span>

### <span data-ttu-id="b1cc9-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1cc9-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1cc9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b1cc9-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1cc9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1cc9-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1cc9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1cc9-108">DESCRIPTION</span></span>
<span data-ttu-id="b1cc9-109">Das **Cmdlet Restore-AzKeyVaultManagedStorageAccount** erstellt ein verwaltetes Speicherkonto im angegebenen Schlüsseltresor aus einer Sicherungsdatei.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="b1cc9-110">Dieses verwaltete Speicherkonto ist ein Replikat des gesicherten verwalteten Speicherkontos in der Eingabedatei und hat denselben Namen wie das Original.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="b1cc9-111">Wenn der Schlüsseltresor bereits ein verwaltetes Speicherkonto mit demselben Namen enthält, schlägt dieses Cmdlet fehl, statt das Original zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="b1cc9-112">Der Schlüsseltresor, in dem Sie das verwaltete Speicherkonto wiederherstellen, kann sich vom Schlüsseltresor unterscheiden, von dem Sie das verwaltete Speicherkonto gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="b1cc9-113">Der Schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einer Azure-Region in derselben Geographie befinden (z. B. Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="b1cc9-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b1cc9-114">Siehe Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geografischen Regionen.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b1cc9-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1cc9-115">EXAMPLES</span></span>

### <span data-ttu-id="b1cc9-116">Beispiel 1: Wiederherstellen eines gesicherten verwalteten Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="b1cc9-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="b1cc9-117">Mit diesem Befehl wird ein verwaltetes Speicherkonto einschließlich aller seiner Versionen aus der Sicherungsdatei "Backup.blob" in den Schlüsseltresor "MyKeyVault" wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="b1cc9-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b1cc9-118">PARAMETERS</span></span>

### <span data-ttu-id="b1cc9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1cc9-119">-DefaultProfile</span></span>
<span data-ttu-id="b1cc9-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1cc9-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b1cc9-121">-InputFile</span></span>
<span data-ttu-id="b1cc9-122">Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-122">Input file.</span></span>
<span data-ttu-id="b1cc9-123">Die Eingabedatei mit dem gesicherten Blob</span><span class="sxs-lookup"><span data-stu-id="b1cc9-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="b1cc9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1cc9-124">-InputObject</span></span>
<span data-ttu-id="b1cc9-125">KeyVault-Objekt</span><span class="sxs-lookup"><span data-stu-id="b1cc9-125">KeyVault object</span></span>

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

### <span data-ttu-id="b1cc9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1cc9-126">-ResourceId</span></span>
<span data-ttu-id="b1cc9-127">KeyVault-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b1cc9-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="b1cc9-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b1cc9-128">-VaultName</span></span>
<span data-ttu-id="b1cc9-129">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-129">Vault name.</span></span>
<span data-ttu-id="b1cc9-130">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b1cc9-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1cc9-131">-Confirm</span></span>
<span data-ttu-id="b1cc9-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1cc9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1cc9-133">-WhatIf</span></span>
<span data-ttu-id="b1cc9-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1cc9-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1cc9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cc9-136">CommonParameters</span></span>
<span data-ttu-id="b1cc9-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1cc9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cc9-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1cc9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cc9-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1cc9-139">INPUTS</span></span>

### <span data-ttu-id="b1cc9-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b1cc9-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b1cc9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b1cc9-141">System.String</span></span>

## <span data-ttu-id="b1cc9-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1cc9-142">OUTPUTS</span></span>

### <span data-ttu-id="b1cc9-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1cc9-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="b1cc9-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b1cc9-144">NOTES</span></span>

## <span data-ttu-id="b1cc9-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b1cc9-145">RELATED LINKS</span></span>
