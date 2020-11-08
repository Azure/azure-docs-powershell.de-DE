---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: cae763eedd98a98c7e09855a295791ddc96d5339
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166402"
---
# <span data-ttu-id="86975-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="86975-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="86975-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86975-102">SYNOPSIS</span></span>
<span data-ttu-id="86975-103">Aktualisiert die Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="86975-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="86975-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86975-104">SYNTAX</span></span>

### <span data-ttu-id="86975-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="86975-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86975-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="86975-106">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86975-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86975-107">DESCRIPTION</span></span>
<span data-ttu-id="86975-108">Das Cmdlet **Update-AzKeyVaultKey** aktualisiert die bearbeitbaren Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="86975-108">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="86975-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86975-109">EXAMPLES</span></span>

### <span data-ttu-id="86975-110">Beispiel 1: Ändern eines Schlüssels, um ihn zu aktivieren, und Festlegen des Ablaufdatums und der Tags</span><span class="sxs-lookup"><span data-stu-id="86975-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="86975-111">Mit dem ersten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="86975-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="86975-112">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="86975-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="86975-113">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="86975-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="86975-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="86975-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="86975-115">Der zweite Befehl erstellt eine Variable zum Speichern von Tag-Werten mit einem höheren Schweregrad und einer Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="86975-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="86975-116">Der endgültige Befehl ändert einen Schlüssel mit dem Namen ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="86975-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="86975-117">Der Befehl aktiviert den Schlüssel, legt dessen Ablaufzeit auf die in $Expires gespeicherte Zeit fest und legt die in $Tags gespeicherten Tags fest.</span><span class="sxs-lookup"><span data-stu-id="86975-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="86975-118">Beispiel 2: Ändern einer Taste zum Löschen aller Kategorien</span><span class="sxs-lookup"><span data-stu-id="86975-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="86975-119">Mit diesen Befehlen werden alle Tags für eine bestimmte Version eines Schlüssels mit dem Namen ITSoftware gelöscht.</span><span class="sxs-lookup"><span data-stu-id="86975-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="86975-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="86975-120">PARAMETERS</span></span>

### <span data-ttu-id="86975-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86975-121">-DefaultProfile</span></span>
<span data-ttu-id="86975-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86975-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86975-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="86975-123">-Enable</span></span>
<span data-ttu-id="86975-124">Der Wert true aktiviert den Schlüssel und den Wert false.</span><span class="sxs-lookup"><span data-stu-id="86975-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="86975-125">Wenn diese Option nicht angegeben ist, bleibt der vorhandene aktiviert/deaktivierte Status unverändert.</span><span class="sxs-lookup"><span data-stu-id="86975-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="86975-126">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="86975-126">-Expires</span></span>
<span data-ttu-id="86975-127">Die Ablaufzeit eines Schlüssels in UTC-Zeit.</span><span class="sxs-lookup"><span data-stu-id="86975-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="86975-128">Wenn Sie nicht angegeben wird, bleibt die vorhandene Ablaufzeit des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="86975-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="86975-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="86975-129">-InputObject</span></span>
<span data-ttu-id="86975-130">Key-Objekt</span><span class="sxs-lookup"><span data-stu-id="86975-130">Key object</span></span>

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

### <span data-ttu-id="86975-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="86975-131">-KeyOps</span></span>
<span data-ttu-id="86975-132">Die Vorgänge, die mit dem Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="86975-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="86975-133">Wenn nicht angegeben, bleiben die vorhandenen Schlüsselvorgänge des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="86975-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="86975-134">-Name</span><span class="sxs-lookup"><span data-stu-id="86975-134">-Name</span></span>
<span data-ttu-id="86975-135">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="86975-135">Key name.</span></span>
<span data-ttu-id="86975-136">Cmdlet erstellt den FQDN eines Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="86975-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="86975-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="86975-137">-NotBefore</span></span>
<span data-ttu-id="86975-138">Die UTC-Zeit, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="86975-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="86975-139">Wenn keine Angabe erfolgt, bleibt das vorhandene NotBefore-Attribut des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="86975-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="86975-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86975-140">-PassThru</span></span>
<span data-ttu-id="86975-141">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="86975-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="86975-142">Wenn dieser Schalter angegeben wird, wird das aktualisierte Schlüssel Bündel Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="86975-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="86975-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="86975-143">-Tag</span></span>
<span data-ttu-id="86975-144">Eine Hashtable stellt Schlüsselkategorien dar.</span><span class="sxs-lookup"><span data-stu-id="86975-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="86975-145">Wenn Sie nicht angegeben wird, bleiben die vorhandenen Tags des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="86975-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="86975-146">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="86975-146">-VaultName</span></span>
<span data-ttu-id="86975-147">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="86975-147">Vault name.</span></span>
<span data-ttu-id="86975-148">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="86975-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="86975-149">-Version</span><span class="sxs-lookup"><span data-stu-id="86975-149">-Version</span></span>
<span data-ttu-id="86975-150">Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="86975-150">Key version.</span></span>
<span data-ttu-id="86975-151">Cmdlet erstellt den FQDN eines Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung, Schlüsselname und Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="86975-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="86975-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86975-152">-Confirm</span></span>
<span data-ttu-id="86975-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86975-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86975-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86975-154">-WhatIf</span></span>
<span data-ttu-id="86975-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86975-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86975-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86975-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86975-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86975-157">CommonParameters</span></span>
<span data-ttu-id="86975-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86975-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86975-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86975-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86975-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86975-160">INPUTS</span></span>

### <span data-ttu-id="86975-161">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="86975-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="86975-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86975-162">OUTPUTS</span></span>

### <span data-ttu-id="86975-163">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="86975-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="86975-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="86975-164">NOTES</span></span>

## <span data-ttu-id="86975-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86975-165">RELATED LINKS</span></span>
