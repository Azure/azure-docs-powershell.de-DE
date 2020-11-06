---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496514"
---
# <span data-ttu-id="12b92-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="12b92-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="12b92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12b92-102">SYNOPSIS</span></span>
<span data-ttu-id="12b92-103">Aktualisiert die Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="12b92-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12b92-104">SYNTAX</span></span>

### <span data-ttu-id="12b92-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="12b92-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b92-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="12b92-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b92-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12b92-107">DESCRIPTION</span></span>
<span data-ttu-id="12b92-108">Das Cmdlet " **Satz-AzureKeyVaultKeyAttribute** " aktualisiert die bearbeitbaren Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="12b92-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="12b92-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12b92-109">EXAMPLES</span></span>

### <span data-ttu-id="12b92-110">Beispiel 1: Ändern eines Schlüssels, um ihn zu aktivieren, und Festlegen des Ablaufdatums und der Tags</span><span class="sxs-lookup"><span data-stu-id="12b92-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="12b92-111">Mit dem ersten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="12b92-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="12b92-112">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="12b92-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="12b92-113">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="12b92-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="12b92-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="12b92-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="12b92-115">Der zweite Befehl erstellt eine Variable zum Speichern von Tag-Werten mit einem höheren Schweregrad und einer Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="12b92-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="12b92-116">Der endgültige Befehl ändert einen Schlüssel mit dem Namen ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="12b92-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="12b92-117">Der Befehl aktiviert den Schlüssel, legt dessen Ablaufzeit auf die in $Expires gespeicherte Zeit fest und legt die in $Tags gespeicherten Tags fest.</span><span class="sxs-lookup"><span data-stu-id="12b92-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="12b92-118">Beispiel 2: Ändern einer Taste zum Löschen aller Kategorien</span><span class="sxs-lookup"><span data-stu-id="12b92-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="12b92-119">Mit diesen Befehlen werden alle Tags für eine bestimmte Version eines Schlüssels mit dem Namen ITSoftware gelöscht.</span><span class="sxs-lookup"><span data-stu-id="12b92-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="12b92-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="12b92-120">PARAMETERS</span></span>

### <span data-ttu-id="12b92-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b92-121">-DefaultProfile</span></span>
<span data-ttu-id="12b92-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="12b92-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12b92-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="12b92-123">-Enable</span></span>
<span data-ttu-id="12b92-124">Gibt an, ob ein Schlüssel aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="12b92-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="12b92-125">Der Wert $true aktiviert den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="12b92-125">A value of $True enables the key.</span></span> <span data-ttu-id="12b92-126">Der Wert $false deaktiviert den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="12b92-126">A value of $False disables the key.</span></span> <span data-ttu-id="12b92-127">Wenn Sie diesen Parameter nicht angeben, ändert dieses Cmdlet nicht den Status des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="12b92-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-128">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="12b92-128">-Expires</span></span>
<span data-ttu-id="12b92-129">Gibt die Ablaufzeit als **DateTime** -Objekt für den Schlüssel an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="12b92-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="12b92-130">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="12b92-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="12b92-131">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="12b92-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="12b92-132">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="12b92-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12b92-133">-InputObject</span></span>
<span data-ttu-id="12b92-134">Key-Objekt</span><span class="sxs-lookup"><span data-stu-id="12b92-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="12b92-135">-KeyOps</span></span>
<span data-ttu-id="12b92-136">Gibt ein Array von Vorgängen an, die mit dem vom Cmdlet hinzugefügten Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="12b92-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="12b92-137">Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="12b92-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="12b92-138">Bei den akzeptablen Werten für diesen Parameter handelt es sich um eine durch trennzeichengetrennte Liste der wichtigsten Vorgänge, wie Sie in der JSON Web Key-Spezifikation definiert sind.</span><span class="sxs-lookup"><span data-stu-id="12b92-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="12b92-139">Diese Werte (Groß-/Kleinschreibung beachten) sind:</span><span class="sxs-lookup"><span data-stu-id="12b92-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="12b92-140">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="12b92-140">encrypt</span></span>
- <span data-ttu-id="12b92-141">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="12b92-141">decrypt</span></span>
- <span data-ttu-id="12b92-142">Umbrechen</span><span class="sxs-lookup"><span data-stu-id="12b92-142">wrap</span></span>
- <span data-ttu-id="12b92-143">Unwrap</span><span class="sxs-lookup"><span data-stu-id="12b92-143">unwrap</span></span>
- <span data-ttu-id="12b92-144">melden sich</span><span class="sxs-lookup"><span data-stu-id="12b92-144">sign</span></span>
- <span data-ttu-id="12b92-145">prüfen</span><span class="sxs-lookup"><span data-stu-id="12b92-145">verify</span></span>
- <span data-ttu-id="12b92-146">Backup</span><span class="sxs-lookup"><span data-stu-id="12b92-146">backup</span></span>
- <span data-ttu-id="12b92-147">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="12b92-147">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-148">-Name</span><span class="sxs-lookup"><span data-stu-id="12b92-148">-Name</span></span>
<span data-ttu-id="12b92-149">Gibt den Namen des Schlüssels an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="12b92-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="12b92-150">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="12b92-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="12b92-151">-NotBefore</span></span>
<span data-ttu-id="12b92-152">Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="12b92-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="12b92-153">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="12b92-153">This parameter uses UTC.</span></span>
<span data-ttu-id="12b92-154">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="12b92-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12b92-155">-PassThru</span></span>
<span data-ttu-id="12b92-156">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="12b92-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12b92-157">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="12b92-157">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="12b92-158">-Tag</span></span>
<span data-ttu-id="12b92-159">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="12b92-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="12b92-160">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="12b92-160">For example:</span></span>

<span data-ttu-id="12b92-161">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="12b92-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-162">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="12b92-162">-VaultName</span></span>
<span data-ttu-id="12b92-163">Gibt den Namen des Schlüsseldepots an, in dem dieses Cmdlet den Schlüssel ändert.</span><span class="sxs-lookup"><span data-stu-id="12b92-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="12b92-164">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="12b92-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-165">-Version</span><span class="sxs-lookup"><span data-stu-id="12b92-165">-Version</span></span>
<span data-ttu-id="12b92-166">Gibt die Schlüssel Version an.</span><span class="sxs-lookup"><span data-stu-id="12b92-166">Specifies the key version.</span></span>
<span data-ttu-id="12b92-167">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="12b92-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12b92-168">-Confirm</span></span>
<span data-ttu-id="12b92-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12b92-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b92-170">-WhatIf</span></span>
<span data-ttu-id="12b92-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12b92-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b92-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12b92-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12b92-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b92-173">CommonParameters</span></span>
<span data-ttu-id="12b92-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b92-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b92-175">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b92-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b92-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12b92-176">INPUTS</span></span>

### <span data-ttu-id="12b92-177">Keine</span><span class="sxs-lookup"><span data-stu-id="12b92-177">None</span></span>
<span data-ttu-id="12b92-178">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="12b92-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12b92-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12b92-179">OUTPUTS</span></span>

### <span data-ttu-id="12b92-180">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="12b92-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="12b92-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="12b92-181">NOTES</span></span>

## <span data-ttu-id="12b92-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12b92-182">RELATED LINKS</span></span>

[<span data-ttu-id="12b92-183">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="12b92-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="12b92-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="12b92-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="12b92-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="12b92-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
