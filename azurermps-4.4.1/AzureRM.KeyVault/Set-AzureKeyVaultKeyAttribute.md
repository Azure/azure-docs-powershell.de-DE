---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690302
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: fbc2c4cd56da23bef29716800316f479159af148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504109"
---
# <span data-ttu-id="cda7d-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="cda7d-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="cda7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cda7d-102">SYNOPSIS</span></span>
<span data-ttu-id="cda7d-103">Aktualisiert die Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="cda7d-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cda7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cda7d-104">SYNTAX</span></span>

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda7d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cda7d-105">DESCRIPTION</span></span>
<span data-ttu-id="cda7d-106">Das Cmdlet " **Satz-AzureKeyVaultKeyAttribute** " aktualisiert die bearbeitbaren Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="cda7d-106">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="cda7d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cda7d-107">EXAMPLES</span></span>

### <span data-ttu-id="cda7d-108">Beispiel 1: Ändern eines Schlüssels, um ihn zu aktivieren, und Festlegen des Ablaufdatums und der Tags</span><span class="sxs-lookup"><span data-stu-id="cda7d-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="cda7d-109">Mit dem ersten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="cda7d-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cda7d-110">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="cda7d-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="cda7d-111">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="cda7d-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="cda7d-112">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cda7d-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="cda7d-113">Der zweite Befehl erstellt eine Variable zum Speichern von Tag-Werten mit einem höheren Schweregrad und einer Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="cda7d-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="cda7d-114">Der endgültige Befehl ändert einen Schlüssel mit dem Namen ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="cda7d-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="cda7d-115">Der Befehl aktiviert den Schlüssel, legt dessen Ablaufzeit auf die in $Expires gespeicherte Zeit fest und legt die in $Tags gespeicherten Tags fest.</span><span class="sxs-lookup"><span data-stu-id="cda7d-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="cda7d-116">Beispiel 2: Ändern einer Taste zum Löschen aller Kategorien</span><span class="sxs-lookup"><span data-stu-id="cda7d-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="cda7d-117">Mit diesen Befehlen werden alle Tags für eine bestimmte Version eines Schlüssels mit dem Namen ITSoftware gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cda7d-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="cda7d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="cda7d-118">PARAMETERS</span></span>

### <span data-ttu-id="cda7d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cda7d-119">-Confirm</span></span>
<span data-ttu-id="cda7d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cda7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda7d-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="cda7d-121">-Enable</span></span>
<span data-ttu-id="cda7d-122">Gibt an, ob ein Schlüssel aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cda7d-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="cda7d-123">Der Wert $true aktiviert den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="cda7d-123">A value of $True enables the key.</span></span> <span data-ttu-id="cda7d-124">Der Wert $false deaktiviert den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="cda7d-124">A value of $False disables the key.</span></span> <span data-ttu-id="cda7d-125">Wenn Sie diesen Parameter nicht angeben, ändert dieses Cmdlet nicht den Status des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="cda7d-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="cda7d-126">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="cda7d-126">-Expires</span></span>
<span data-ttu-id="cda7d-127">Gibt die Ablaufzeit als **DateTime** -Objekt für den Schlüssel an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cda7d-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="cda7d-128">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="cda7d-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cda7d-129">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cda7d-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cda7d-130">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cda7d-130">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda7d-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="cda7d-131">-KeyOps</span></span>
<span data-ttu-id="cda7d-132">Gibt ein Array von Vorgängen an, die mit dem vom Cmdlet hinzugefügten Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="cda7d-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="cda7d-133">Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cda7d-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="cda7d-134">Bei den akzeptablen Werten für diesen Parameter handelt es sich um eine durch trennzeichengetrennte Liste der wichtigsten Vorgänge, wie Sie in der JSON Web Key-Spezifikation definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cda7d-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="cda7d-135">Diese Werte (Groß-/Kleinschreibung beachten) sind:</span><span class="sxs-lookup"><span data-stu-id="cda7d-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="cda7d-136">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="cda7d-136">encrypt</span></span>
- <span data-ttu-id="cda7d-137">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="cda7d-137">decrypt</span></span>
- <span data-ttu-id="cda7d-138">Umbrechen</span><span class="sxs-lookup"><span data-stu-id="cda7d-138">wrap</span></span>
- <span data-ttu-id="cda7d-139">Unwrap</span><span class="sxs-lookup"><span data-stu-id="cda7d-139">unwrap</span></span>
- <span data-ttu-id="cda7d-140">melden sich</span><span class="sxs-lookup"><span data-stu-id="cda7d-140">sign</span></span>
- <span data-ttu-id="cda7d-141">prüfen</span><span class="sxs-lookup"><span data-stu-id="cda7d-141">verify</span></span>
- <span data-ttu-id="cda7d-142">Backup</span><span class="sxs-lookup"><span data-stu-id="cda7d-142">backup</span></span>
- <span data-ttu-id="cda7d-143">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="cda7d-143">restore</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda7d-144">-Name</span><span class="sxs-lookup"><span data-stu-id="cda7d-144">-Name</span></span>
<span data-ttu-id="cda7d-145">Gibt den Namen des Schlüssels an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cda7d-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="cda7d-146">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="cda7d-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda7d-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="cda7d-147">-NotBefore</span></span>
<span data-ttu-id="cda7d-148">Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cda7d-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="cda7d-149">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="cda7d-149">This parameter uses UTC.</span></span>
<span data-ttu-id="cda7d-150">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cda7d-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda7d-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cda7d-151">-PassThru</span></span>
<span data-ttu-id="cda7d-152">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cda7d-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cda7d-153">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="cda7d-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cda7d-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="cda7d-154">-Tag</span></span>
<span data-ttu-id="cda7d-155">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="cda7d-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cda7d-156">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cda7d-156">For example:</span></span>

<span data-ttu-id="cda7d-157">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="cda7d-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda7d-158">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="cda7d-158">-VaultName</span></span>
<span data-ttu-id="cda7d-159">Gibt den Namen des Schlüsseldepots an, in dem dieses Cmdlet den Schlüssel ändert.</span><span class="sxs-lookup"><span data-stu-id="cda7d-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="cda7d-160">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="cda7d-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda7d-161">-Version</span><span class="sxs-lookup"><span data-stu-id="cda7d-161">-Version</span></span>
<span data-ttu-id="cda7d-162">Gibt die Schlüssel Version an.</span><span class="sxs-lookup"><span data-stu-id="cda7d-162">Specifies the key version.</span></span>
<span data-ttu-id="cda7d-163">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="cda7d-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda7d-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda7d-164">-WhatIf</span></span>
<span data-ttu-id="cda7d-165">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cda7d-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cda7d-166">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cda7d-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda7d-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda7d-167">-DefaultProfile</span></span>
<span data-ttu-id="cda7d-168">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cda7d-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cda7d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda7d-169">CommonParameters</span></span>
<span data-ttu-id="cda7d-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda7d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda7d-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda7d-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda7d-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cda7d-172">INPUTS</span></span>

## <span data-ttu-id="cda7d-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cda7d-173">OUTPUTS</span></span>

### <span data-ttu-id="cda7d-174">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="cda7d-174">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="cda7d-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="cda7d-175">NOTES</span></span>

## <span data-ttu-id="cda7d-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cda7d-176">RELATED LINKS</span></span>

[<span data-ttu-id="cda7d-177">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cda7d-177">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="cda7d-178">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cda7d-178">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="cda7d-179">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cda7d-179">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
