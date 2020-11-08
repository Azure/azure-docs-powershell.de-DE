---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180407"
---
# <span data-ttu-id="efb4b-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="efb4b-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="efb4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="efb4b-102">SYNOPSIS</span></span>
<span data-ttu-id="efb4b-103">Erstellt einen Schlüssel in einem verwalteten HSM aus einem gesicherten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="efb4b-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="efb4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="efb4b-104">SYNTAX</span></span>

### <span data-ttu-id="efb4b-105">ByHsmName (Standard)</span><span class="sxs-lookup"><span data-stu-id="efb4b-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb4b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="efb4b-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb4b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="efb4b-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb4b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efb4b-108">DESCRIPTION</span></span>
<span data-ttu-id="efb4b-109">Das Cmdlet **Restore-AzManagedHsmKey** erstellt einen Schlüssel im angegebenen verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="efb4b-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="efb4b-110">Dieser Schlüssel ist ein Replikat des gesicherten Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="efb4b-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="efb4b-111">Wenn das verwaltete HSM bereits über einen Schlüssel mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt den ursprünglichen Schlüssel zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="efb4b-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="efb4b-112">Wenn die Sicherung mehrere Versionen eines Schlüssels enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="efb4b-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="efb4b-113">Das verwaltete HSM, in das Sie den Schlüssel wiederherstellen, kann sich vom verwalteten HSM unterscheiden, von dem Sie den Schlüssel gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="efb4b-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="efb4b-114">Das verwaltete HSM muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="efb4b-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="efb4b-115">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="efb4b-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="efb4b-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efb4b-116">EXAMPLES</span></span>

### <span data-ttu-id="efb4b-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efb4b-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="efb4b-118">Mit diesem Befehl wird ein Schlüssel, einschließlich aller seiner Versionen, aus der Sicherungsdatei Backup. BLOB in das verwaltete HSM mit dem Namen testmhsm wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="efb4b-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="efb4b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="efb4b-119">PARAMETERS</span></span>

### <span data-ttu-id="efb4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb4b-120">-DefaultProfile</span></span>
<span data-ttu-id="efb4b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="efb4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb4b-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="efb4b-122">-HsmName</span></span>
<span data-ttu-id="efb4b-123">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="efb4b-123">HSM name.</span></span> <span data-ttu-id="efb4b-124">Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="efb4b-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb4b-125">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="efb4b-125">-InputFile</span></span>
<span data-ttu-id="efb4b-126">Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="efb4b-126">Input file.</span></span>
<span data-ttu-id="efb4b-127">Die Eingabedatei mit dem gesicherten BLOB</span><span class="sxs-lookup"><span data-stu-id="efb4b-127">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="efb4b-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="efb4b-128">-InputObject</span></span>
<span data-ttu-id="efb4b-129">HSM-Objekt</span><span class="sxs-lookup"><span data-stu-id="efb4b-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efb4b-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="efb4b-130">-ResourceId</span></span>
<span data-ttu-id="efb4b-131">HSM-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="efb4b-131">HSM Resource Id</span></span>

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

### <span data-ttu-id="efb4b-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="efb4b-132">-Confirm</span></span>
<span data-ttu-id="efb4b-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="efb4b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb4b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb4b-134">-WhatIf</span></span>
<span data-ttu-id="efb4b-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efb4b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb4b-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efb4b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb4b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb4b-137">CommonParameters</span></span>
<span data-ttu-id="efb4b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb4b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb4b-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efb4b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb4b-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="efb4b-140">INPUTS</span></span>

### <span data-ttu-id="efb4b-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="efb4b-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="efb4b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="efb4b-142">System.String</span></span>

## <span data-ttu-id="efb4b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="efb4b-143">OUTPUTS</span></span>

### <span data-ttu-id="efb4b-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="efb4b-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="efb4b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="efb4b-145">NOTES</span></span>

## <span data-ttu-id="efb4b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="efb4b-146">RELATED LINKS</span></span>

[<span data-ttu-id="efb4b-147">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="efb4b-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="efb4b-148">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="efb4b-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="efb4b-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="efb4b-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="efb4b-150">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="efb4b-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="efb4b-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="efb4b-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="efb4b-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="efb4b-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)