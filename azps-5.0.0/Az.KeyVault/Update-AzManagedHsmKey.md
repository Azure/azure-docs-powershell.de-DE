---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179244"
---
# <span data-ttu-id="c7a18-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="c7a18-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="c7a18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7a18-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a18-103">Aktualisiert die Attribute eines Schlüssels in einem verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="c7a18-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="c7a18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7a18-104">SYNTAX</span></span>

### <span data-ttu-id="c7a18-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7a18-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a18-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c7a18-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7a18-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7a18-107">DESCRIPTION</span></span>
<span data-ttu-id="c7a18-108">Das Cmdlet **Update-AzManagedHsmKey** aktualisiert die bearbeitbaren Attribute eines Schlüssels in einem verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="c7a18-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="c7a18-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7a18-109">EXAMPLES</span></span>

### <span data-ttu-id="c7a18-110">Beispiel 1: Ändern eines Schlüssels, um ihn zu aktivieren, und Festlegen des Ablaufdatums und der Tags</span><span class="sxs-lookup"><span data-stu-id="c7a18-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="c7a18-111">Mit dem ersten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7a18-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="c7a18-112">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="c7a18-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="c7a18-113">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="c7a18-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="c7a18-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c7a18-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="c7a18-115">Der zweite Befehl erstellt eine Variable zum Speichern von Tag-Werten mit einem höheren Schweregrad und einer Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="c7a18-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="c7a18-116">Der endgültige Befehl ändert einen Schlüssel mit dem Namen testkey001.</span><span class="sxs-lookup"><span data-stu-id="c7a18-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="c7a18-117">Der Befehl aktiviert den Schlüssel, legt dessen Ablaufzeit auf die in $Expires gespeicherte Zeit fest und legt die in $Tags gespeicherten Tags fest.</span><span class="sxs-lookup"><span data-stu-id="c7a18-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="c7a18-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7a18-118">PARAMETERS</span></span>

### <span data-ttu-id="c7a18-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a18-119">-DefaultProfile</span></span>
<span data-ttu-id="c7a18-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7a18-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a18-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="c7a18-121">-Enable</span></span>
<span data-ttu-id="c7a18-122">Der Wert true aktiviert den Schlüssel und den Wert false.</span><span class="sxs-lookup"><span data-stu-id="c7a18-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="c7a18-123">Wenn diese Option nicht angegeben ist, bleibt der vorhandene aktiviert/deaktivierte Status unverändert.</span><span class="sxs-lookup"><span data-stu-id="c7a18-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-124">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="c7a18-124">-Expires</span></span>
<span data-ttu-id="c7a18-125">Die Ablaufzeit eines Schlüssels in UTC-Zeit.</span><span class="sxs-lookup"><span data-stu-id="c7a18-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="c7a18-126">Wenn Sie nicht angegeben wird, bleibt die vorhandene Ablaufzeit des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c7a18-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="c7a18-127">-HsmName</span></span>
<span data-ttu-id="c7a18-128">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="c7a18-128">HSM name.</span></span> <span data-ttu-id="c7a18-129">Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c7a18-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7a18-130">-InputObject</span></span>
<span data-ttu-id="c7a18-131">Key-Objekt</span><span class="sxs-lookup"><span data-stu-id="c7a18-131">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="c7a18-132">-KeyOps</span></span>
<span data-ttu-id="c7a18-133">Die Vorgänge, die mit dem Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c7a18-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="c7a18-134">Wenn nicht angegeben, bleiben die vorhandenen Schlüsselvorgänge des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c7a18-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c7a18-135">-Name</span></span>
<span data-ttu-id="c7a18-136">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="c7a18-136">Key name.</span></span>
<span data-ttu-id="c7a18-137">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="c7a18-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="c7a18-138">-NotBefore</span></span>
<span data-ttu-id="c7a18-139">Die UTC-Zeit, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7a18-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="c7a18-140">Wenn keine Angabe erfolgt, bleibt das vorhandene NotBefore-Attribut des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c7a18-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7a18-141">-PassThru</span></span>
<span data-ttu-id="c7a18-142">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c7a18-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c7a18-143">Wenn dieser Schalter angegeben wird, wird das aktualisierte Schlüssel Bündel Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7a18-143">If this switch is specified, returns the updated key bundle object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7a18-144">-Tag</span></span>
<span data-ttu-id="c7a18-145">Eine Hashtable stellt Schlüsselkategorien dar.</span><span class="sxs-lookup"><span data-stu-id="c7a18-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="c7a18-146">Wenn Sie nicht angegeben wird, bleiben die vorhandenen Tags des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c7a18-146">If not specified, the existings tags of the key remain unchanged.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-147">-Version</span><span class="sxs-lookup"><span data-stu-id="c7a18-147">-Version</span></span>
<span data-ttu-id="c7a18-148">Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="c7a18-148">Key version.</span></span>
<span data-ttu-id="c7a18-149">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung, Schlüsselname und Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="c7a18-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a18-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7a18-150">-Confirm</span></span>
<span data-ttu-id="c7a18-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7a18-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a18-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a18-152">-WhatIf</span></span>
<span data-ttu-id="c7a18-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7a18-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a18-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7a18-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a18-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a18-155">CommonParameters</span></span>
<span data-ttu-id="c7a18-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a18-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a18-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7a18-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a18-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7a18-158">INPUTS</span></span>

### <span data-ttu-id="c7a18-159">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c7a18-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="c7a18-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7a18-160">OUTPUTS</span></span>

### <span data-ttu-id="c7a18-161">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c7a18-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="c7a18-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7a18-162">NOTES</span></span>

## <span data-ttu-id="c7a18-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7a18-163">RELATED LINKS</span></span>

[<span data-ttu-id="c7a18-164">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="c7a18-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="c7a18-165">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="c7a18-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="c7a18-166">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="c7a18-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="c7a18-167">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="c7a18-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="c7a18-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="c7a18-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="c7a18-169">Wiederherstellen – AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="c7a18-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)