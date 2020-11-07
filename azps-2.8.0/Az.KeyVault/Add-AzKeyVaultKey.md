---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: f7447725e63634642f285b6a796a2b59b4d1d301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650925"
---
# <span data-ttu-id="591b1-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="591b1-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="591b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="591b1-102">SYNOPSIS</span></span>
<span data-ttu-id="591b1-103">Erstellt einen Schlüssel in einem schlüsseltresor oder importiert einen Schlüssel in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="591b1-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="591b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="591b1-104">SYNTAX</span></span>

### <span data-ttu-id="591b1-105">InteractiveCreate (Standard)</span><span class="sxs-lookup"><span data-stu-id="591b1-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591b1-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="591b1-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591b1-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="591b1-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591b1-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="591b1-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591b1-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="591b1-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591b1-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="591b1-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="591b1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="591b1-111">DESCRIPTION</span></span>
<span data-ttu-id="591b1-112">Das Cmdlet **Add-AzKeyVaultKey** erstellt einen Schlüssel in einem schlüsseltresor im Azure Key Vault oder importiert einen Schlüssel in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="591b1-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="591b1-113">Verwenden Sie dieses Cmdlet, um Schlüssel mithilfe einer der folgenden Methoden hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="591b1-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="591b1-114">Erstellen Sie einen Schlüssel in einem Hardwaresicherheitsmodul (HSM) im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="591b1-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="591b1-115">Erstellen Sie einen Schlüssel in Software im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="591b1-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="591b1-116">Importieren Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul (HSM) zu HSMs im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="591b1-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="591b1-117">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="591b1-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="591b1-118">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer in die Hardwaresicherheitsmodule (HSMs) des Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="591b1-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="591b1-119">Für alle diese Vorgänge können Sie wichtige Attribute bereitstellen oder Standardeinstellungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="591b1-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="591b1-120">Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel in Ihrem schlüsseltresor hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="591b1-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="591b1-121">Sie können mithilfe des versionsspezifischen URIs für diese Version des Schlüssels auf die vorherigen Werte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="591b1-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="591b1-122">Informationen zu Schlüssel Versionen und der URI-Struktur finden Sie unter [Informationen zu Schlüsseln und Geheimnissen](https://go.microsoft.com/fwlink/?linkid=518560) in der Key Vault-Ruhe API-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="591b1-122">To learn about key versions and the URI structure, see [About Keys and Secrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="591b1-123">Hinweis: Wenn Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul importieren möchten, müssen Sie zunächst ein BYOK-Paket (eine Datei mit der Dateinamenerweiterung. BYOK) mithilfe des Azure Key Vault-BYOK-Toolsets erstellen.</span><span class="sxs-lookup"><span data-stu-id="591b1-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="591b1-124">Weitere Informationen finden Sie unter [so wird es gemacht: generieren und übertragen von HSM-Protected Schlüsseln für Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="591b1-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="591b1-125">Als bewährte Methode können Sie mithilfe des Backup-AzKeyVaultKey-Cmdlets Ihren Schlüssel nach dem Erstellen oder aktualisieren sichern.</span><span class="sxs-lookup"><span data-stu-id="591b1-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="591b1-126">Es gibt keine Funktion zur Undelete-Funktion, wenn Sie Ihren Schlüssel versehentlich löschen oder löschen und dann Ihre Vorstellung ändern, ist der Schlüssel nicht wiederherstellbar, es sei denn, Sie haben eine Sicherungskopie davon, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="591b1-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="591b1-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="591b1-127">EXAMPLES</span></span>

### <span data-ttu-id="591b1-128">Beispiel 1: Erstellen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="591b1-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="591b1-129">Dieser Befehl erstellt einen Software geschützten Schlüssel mit dem Namen ITSoftware im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="591b1-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="591b1-130">Beispiel 2: Erstellen eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="591b1-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="591b1-131">Mit diesem Befehl wird im schlüsseltresor mit dem Namen Contoso ein HSM-geschützter Schlüssel erstellt.</span><span class="sxs-lookup"><span data-stu-id="591b1-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="591b1-132">Beispiel 3: Erstellen eines Schlüssels mit nicht standardmäßigen Werten</span><span class="sxs-lookup"><span data-stu-id="591b1-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="591b1-133">Der erste Befehl speichert die Werte, die entschlüsselt und in der $KeyOperations Variablen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="591b1-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="591b1-134">Mit dem zweiten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt, das in UTC definiert ist.</span><span class="sxs-lookup"><span data-stu-id="591b1-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="591b1-135">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="591b1-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="591b1-136">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="591b1-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="591b1-137">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="591b1-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="591b1-138">Der dritte Befehl erstellt mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="591b1-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="591b1-139">Dieses Objekt gibt die aktuelle UTC-Zeit an.</span><span class="sxs-lookup"><span data-stu-id="591b1-139">That object specifies current UTC time.</span></span> <span data-ttu-id="591b1-140">Der Befehl speichert dieses Datum in der $NotBefore Variablen.</span><span class="sxs-lookup"><span data-stu-id="591b1-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="591b1-141">Der endgültige Befehl erstellt einen Schlüssel mit dem Namen ITHsmNonDefault, bei dem es sich um einen HSM-geschützten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="591b1-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="591b1-142">Der Befehl gibt Werte für zulässige Schlüsselvorgänge an, die $KeyOperations gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="591b1-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="591b1-143">Der Befehl gibt die Zeiten für die in den vorherigen Befehlen erstellten Ablauf-und *NotBefore* -Parameter sowie die Tags für den höchsten Schweregrad und das *Datum* an.</span><span class="sxs-lookup"><span data-stu-id="591b1-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="591b1-144">Der neue Schlüssel ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="591b1-144">The new key is disabled.</span></span> <span data-ttu-id="591b1-145">Sie können es mithilfe des Cmdlets " **festlegen-AzKeyVaultKey** " aktivieren.</span><span class="sxs-lookup"><span data-stu-id="591b1-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="591b1-146">Beispiel 4: Importieren eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="591b1-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="591b1-147">Dieser Befehl importiert den Schlüssel mit dem Namen ITByok von dem Speicherort, der vom *keyFilePath* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="591b1-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="591b1-148">Der importierte Schlüssel ist ein HSM-geschützter Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="591b1-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="591b1-149">Wenn Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul importieren möchten, müssen Sie zunächst ein BYOK-Paket (eine Datei mit der Dateinamenerweiterung. BYOK) mithilfe des Azure Key Vault-BYOK-Toolsets erstellen.</span><span class="sxs-lookup"><span data-stu-id="591b1-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="591b1-150">Weitere Informationen finden Sie unter [so wird es gemacht: generieren und übertragen von HSM-Protected Schlüsseln für Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="591b1-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="591b1-151">Beispiel 5: Importieren eines Software geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="591b1-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="591b1-152">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="591b1-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="591b1-153">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="591b1-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="591b1-154">Der zweite Befehl erstellt ein Software Kennwort im Contoso-Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="591b1-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="591b1-155">Der Befehl gibt den Speicherort für den Schlüssel und das Kennwort an, das in $Password gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="591b1-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="591b1-156">Beispiel 6: Importieren eines Schlüssels und Zuweisen von Attributen</span><span class="sxs-lookup"><span data-stu-id="591b1-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="591b1-157">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="591b1-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="591b1-158">Der zweite Befehl erstellt mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt und speichert dieses Objekt dann in der $Expires-Variablen.</span><span class="sxs-lookup"><span data-stu-id="591b1-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="591b1-159">Mit dem dritten Befehl wird die $Tags-Variable erstellt, um Tags für einen höheren Schweregrad und die Variable festzulegen.</span><span class="sxs-lookup"><span data-stu-id="591b1-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="591b1-160">Der endgültige Befehl importiert einen Schlüssel als HSM-Schlüssel vom angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="591b1-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="591b1-161">Der Befehl gibt die Ablaufzeit an, die in $Expires und dem in $Password gespeicherten Kennwort gespeichert ist, und wendet die in $Tags gespeicherten Tags an.</span><span class="sxs-lookup"><span data-stu-id="591b1-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="591b1-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="591b1-162">PARAMETERS</span></span>

### <span data-ttu-id="591b1-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591b1-163">-DefaultProfile</span></span>
<span data-ttu-id="591b1-164">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="591b1-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="591b1-165">-Ziel</span><span class="sxs-lookup"><span data-stu-id="591b1-165">-Destination</span></span>
<span data-ttu-id="591b1-166">Gibt an, ob der Schlüssel als Software geschützter Schlüssel oder als HSM-geschützter Schlüssel im Key Vault-Dienst hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="591b1-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="591b1-167">Gültige Werte sind: HSM und Software.</span><span class="sxs-lookup"><span data-stu-id="591b1-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="591b1-168">Hinweis: Wenn Sie HSM als Ziel verwenden möchten, müssen Sie über einen schlüsseltresor verfügen, der HSMs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="591b1-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="591b1-169">Weitere Informationen zu den Dienstebenen und Funktionen für Azure Key Vault finden Sie auf der [Azure Key Vault-Preis Website](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="591b1-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="591b1-170">Dieser Parameter ist erforderlich, wenn Sie einen neuen Schlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="591b1-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="591b1-171">Wenn Sie einen Schlüssel mithilfe des *keyFilePath* -Parameters importieren, ist dieser Parameter optional:</span><span class="sxs-lookup"><span data-stu-id="591b1-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="591b1-172">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel importiert, der über die Dateinamenerweiterung Byok verfügt, wird dieser Schlüssel als HSM-geschützter Schlüssel importiert.</span><span class="sxs-lookup"><span data-stu-id="591b1-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="591b1-173">Das Cmdlet kann diesen Schlüssel nicht als Software geschützten Schlüssel importieren.</span><span class="sxs-lookup"><span data-stu-id="591b1-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="591b1-174">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel importiert, der über die Dateinamenerweiterung PFX verfügt, wird der Schlüssel als Software geschützter Schlüssel importiert.</span><span class="sxs-lookup"><span data-stu-id="591b1-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-175">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="591b1-175">-Disable</span></span>
<span data-ttu-id="591b1-176">Gibt an, dass der hinzuzufügende Schlüssel auf den Anfangszustand disabled festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="591b1-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="591b1-177">Jeder Versuch, den Schlüssel zu verwenden, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="591b1-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="591b1-178">Verwenden Sie diesen Parameter, wenn Sie Schlüssel Vorabladen, die Sie später aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="591b1-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="591b1-179">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="591b1-179">-Expires</span></span>
<span data-ttu-id="591b1-180">Gibt die Ablaufzeit als **DateTime** -Objekt für den Schlüssel an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="591b1-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="591b1-181">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="591b1-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="591b1-182">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="591b1-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="591b1-183">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="591b1-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="591b1-184">Wenn Sie diesen Parameter nicht angeben, läuft der Schlüssel nicht ab.</span><span class="sxs-lookup"><span data-stu-id="591b1-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="591b1-185">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="591b1-185">-InputObject</span></span>
<span data-ttu-id="591b1-186">Vault-Objekt</span><span class="sxs-lookup"><span data-stu-id="591b1-186">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="591b1-187">-KeyFilePassword</span></span>
<span data-ttu-id="591b1-188">Gibt ein Kennwort für die importierte Datei als **SecureString** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="591b1-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="591b1-189">Verwenden Sie zum Abrufen eines **SecureString** -Objekts das Cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="591b1-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="591b1-190">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="591b1-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="591b1-191">Sie müssen dieses Kennwort angeben, um eine Datei mit der Dateinamenerweiterung PFX zu importieren.</span><span class="sxs-lookup"><span data-stu-id="591b1-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="591b1-192">-KeyFilePath</span></span>
<span data-ttu-id="591b1-193">Gibt den Pfad einer lokalen Datei an, die das Schlüsselmaterial enthält, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="591b1-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="591b1-194">Die gültigen Dateinamenerweiterungen sind Byok und PFX.</span><span class="sxs-lookup"><span data-stu-id="591b1-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="591b1-195">Wenn es sich bei der Datei um eine Byok-Datei handelt, wird der Schlüssel nach dem Import automatisch durch HSMs geschützt, und Sie können diesen Standardwert nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="591b1-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="591b1-196">Wenn es sich bei der Datei um eine PFX-Datei handelt, wird der Schlüssel nach dem Import automatisch durch Software geschützt.</span><span class="sxs-lookup"><span data-stu-id="591b1-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="591b1-197">Um diesen Standardwert zu überschreiben, setzen Sie den *Ziel* Parameter auf HSM, damit der Schlüssel HSM-geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="591b1-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="591b1-198">Wenn Sie diesen Parameter angeben, ist der *Ziel* Parameter optional.</span><span class="sxs-lookup"><span data-stu-id="591b1-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="591b1-199">-KeyOps</span></span>
<span data-ttu-id="591b1-200">Gibt ein Array von Vorgängen an, die mit dem vom Cmdlet hinzugefügten Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="591b1-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="591b1-201">Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="591b1-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="591b1-202">Bei den akzeptablen Werten für diesen Parameter handelt es sich um eine durch trennzeichengetrennte Liste der wichtigsten Vorgänge, wie Sie in der [JSON Web Key (JWK)-Spezifikation](https://go.microsoft.com/fwlink/?LinkID=613300)definiert ist:</span><span class="sxs-lookup"><span data-stu-id="591b1-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="591b1-203">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="591b1-203">Encrypt</span></span>
- <span data-ttu-id="591b1-204">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="591b1-204">Decrypt</span></span>
- <span data-ttu-id="591b1-205">Umbrechen</span><span class="sxs-lookup"><span data-stu-id="591b1-205">Wrap</span></span>
- <span data-ttu-id="591b1-206">Unwrap</span><span class="sxs-lookup"><span data-stu-id="591b1-206">Unwrap</span></span>
- <span data-ttu-id="591b1-207">Melden sich</span><span class="sxs-lookup"><span data-stu-id="591b1-207">Sign</span></span>
- <span data-ttu-id="591b1-208">Prüfen</span><span class="sxs-lookup"><span data-stu-id="591b1-208">Verify</span></span>

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

### <span data-ttu-id="591b1-209">-Name</span><span class="sxs-lookup"><span data-stu-id="591b1-209">-Name</span></span>
<span data-ttu-id="591b1-210">Gibt den Namen des Schlüssels an, der dem schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="591b1-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="591b1-211">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="591b1-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="591b1-212">Der Name muss eine Zeichenfolge von 1 bis 63 Zeichen lang sein, die nur 0-9, a-z, a-z und-(das Strichsymbol) enthält.</span><span class="sxs-lookup"><span data-stu-id="591b1-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="591b1-213">-NotBefore</span></span>
<span data-ttu-id="591b1-214">Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="591b1-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="591b1-215">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="591b1-215">This parameter uses UTC.</span></span> <span data-ttu-id="591b1-216">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="591b1-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="591b1-217">Wenn Sie diesen Parameter nicht angeben, kann der Schlüssel sofort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="591b1-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="591b1-218">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="591b1-218">-ResourceId</span></span>
<span data-ttu-id="591b1-219">Vault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="591b1-219">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-220">-Size</span><span class="sxs-lookup"><span data-stu-id="591b1-220">-Size</span></span>
<span data-ttu-id="591b1-221">RSA-Schlüsselgröße in Bits.</span><span class="sxs-lookup"><span data-stu-id="591b1-221">RSA key size, in bits.</span></span> <span data-ttu-id="591b1-222">Wenn keine Angabe erfolgt, stellt der Dienst einen sicheren Standard bereit.</span><span class="sxs-lookup"><span data-stu-id="591b1-222">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-223">-Tag</span><span class="sxs-lookup"><span data-stu-id="591b1-223">-Tag</span></span>
<span data-ttu-id="591b1-224">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="591b1-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="591b1-225">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="591b1-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="591b1-226">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="591b1-226">-VaultName</span></span>
<span data-ttu-id="591b1-227">Gibt den Namen des Schlüsselspeichers an, dem dieses Cmdlet den Schlüssel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="591b1-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="591b1-228">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="591b1-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b1-229">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="591b1-229">-Confirm</span></span>
<span data-ttu-id="591b1-230">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="591b1-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591b1-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591b1-231">-WhatIf</span></span>
<span data-ttu-id="591b1-232">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="591b1-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591b1-233">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="591b1-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591b1-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591b1-234">CommonParameters</span></span>
<span data-ttu-id="591b1-235">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591b1-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591b1-236">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591b1-236">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591b1-237">Eingaben</span><span class="sxs-lookup"><span data-stu-id="591b1-237">INPUTS</span></span>

### <span data-ttu-id="591b1-238">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="591b1-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="591b1-239">System. String</span><span class="sxs-lookup"><span data-stu-id="591b1-239">System.String</span></span>

## <span data-ttu-id="591b1-240">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="591b1-240">OUTPUTS</span></span>

### <span data-ttu-id="591b1-241">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="591b1-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="591b1-242">Notizen</span><span class="sxs-lookup"><span data-stu-id="591b1-242">NOTES</span></span>

## <span data-ttu-id="591b1-243">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="591b1-243">RELATED LINKS</span></span>

[<span data-ttu-id="591b1-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="591b1-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="591b1-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="591b1-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="591b1-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="591b1-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="591b1-247">Satz-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="591b1-247">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
