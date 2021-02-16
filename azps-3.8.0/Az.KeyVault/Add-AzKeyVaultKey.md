---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 3d0f7267d1dbe899de0e0414c52a395985f09bfd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412536"
---
# <span data-ttu-id="0170c-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0170c-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="0170c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0170c-102">SYNOPSIS</span></span>
<span data-ttu-id="0170c-103">Erstellt einen Schlüssel in einem Schlüsseltresor oder importiert einen Schlüssel in einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0170c-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="0170c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0170c-104">SYNTAX</span></span>

### <span data-ttu-id="0170c-105">InteractiveCreate (Standard)</span><span class="sxs-lookup"><span data-stu-id="0170c-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0170c-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="0170c-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0170c-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="0170c-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0170c-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="0170c-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0170c-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="0170c-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0170c-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="0170c-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0170c-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0170c-111">DESCRIPTION</span></span>
<span data-ttu-id="0170c-112">Das **Cmdlet "Add-AzKeyVaultKey"** erstellt einen Schlüssel in einem Schlüsseltresor im Azure Key Vault oder importiert einen Schlüssel in einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0170c-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="0170c-113">Verwenden Sie dieses Cmdlet zum Hinzufügen von Schlüsseln mit einer der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="0170c-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="0170c-114">Erstellen Sie einen Schlüssel in einem Hardwaresicherheitsmodul (Hardware Security Module, HSM) im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="0170c-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="0170c-115">Erstellen Sie einen Schlüssel in der Software im Schlüsseltresordienst.</span><span class="sxs-lookup"><span data-stu-id="0170c-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="0170c-116">Importieren Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul (Hardware Security Module, HSM) in HSMs im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="0170c-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="0170c-117">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="0170c-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="0170c-118">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer in Hardwaresicherheitsmodule (Hardware Security Module, HSMs) im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="0170c-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="0170c-119">Für jede dieser Vorgänge können Sie Schlüsselattribute bereitstellen oder Standardeinstellungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="0170c-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="0170c-120">Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel in Ihrem Schlüsseltresor hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="0170c-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="0170c-121">Sie können auf die vorherigen Werte zugreifen, indem Sie den versionsspezifischen URI für diese Version des Schlüssels verwenden.</span><span class="sxs-lookup"><span data-stu-id="0170c-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="0170c-122">Informationen zu Schlüsselversionen und der URI-Struktur finden Sie [in](http://go.microsoft.com/fwlink/?linkid=518560) der Rest-API-Dokumentation zu Schlüsseln und Geheimen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="0170c-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="0170c-123">Hinweis: Um einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul zu importieren, müssen Sie zuerst mithilfe des Azure Key Vault BYOK Toolset ein "BYOK"-Paket (eine Datei mit der Dateinamenerweiterung BYOK) generieren.</span><span class="sxs-lookup"><span data-stu-id="0170c-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="0170c-124">Weitere Informationen finden Sie unter "Generieren und Übertragen HSM-Protected [Schlüssel für den Azure Key Vault".](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="0170c-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="0170c-125">Als bewährte Methode sollten Sie Ihren Schlüssel nach dem Erstellen oder Aktualisieren sichern, indem Sie das cmdlet Backup-AzKeyVaultKey verwenden.</span><span class="sxs-lookup"><span data-stu-id="0170c-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="0170c-126">Es gibt keine rückgängig gemachten Funktionen. Wenn Sie also versehentlich Ihren Schlüssel löschen oder ihn löschen und dann Ihre Meinung ändern, kann der Schlüssel nur wiederhergestellt werden, wenn Sie über eine Sicherung verfügen, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="0170c-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="0170c-127">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0170c-127">EXAMPLES</span></span>

### <span data-ttu-id="0170c-128">Beispiel 1: Erstellen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0170c-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="0170c-129">Mit diesem Befehl wird ein softwaregeschützter Schlüssel namens "ITSoftware" im Schlüsseltresor "Contoso" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0170c-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="0170c-130">Beispiel 2: Erstellen eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0170c-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="0170c-131">Mit diesem Befehl wird ein HSM-geschützter Schlüssel im Schlüsseltresor "Contoso" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0170c-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="0170c-132">Beispiel 3: Erstellen eines Schlüssels mit Nicht-Standardwerten</span><span class="sxs-lookup"><span data-stu-id="0170c-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="0170c-133">Der erste Befehl speichert die Werte zum Entschlüsseln und Überprüfen in der $KeyOperations Variable.</span><span class="sxs-lookup"><span data-stu-id="0170c-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="0170c-134">Der zweite Befehl erstellt ein in UTC definiertes **DateTime-Objekt** mithilfe des **Get-Date-Cmdlets.**</span><span class="sxs-lookup"><span data-stu-id="0170c-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0170c-135">Dieses Objekt gibt eine Uhrzeit in zwei Jahren in der Zukunft an.</span><span class="sxs-lookup"><span data-stu-id="0170c-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="0170c-136">Der Befehl speichert dieses Datum in der $Expires Variable.</span><span class="sxs-lookup"><span data-stu-id="0170c-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="0170c-137">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="0170c-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0170c-138">Der dritte Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein **DateTime-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="0170c-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0170c-139">Dieses Objekt gibt die aktuelle UTC-Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="0170c-139">That object specifies current UTC time.</span></span> <span data-ttu-id="0170c-140">Der Befehl speichert dieses Datum in der $NotBefore Variable.</span><span class="sxs-lookup"><span data-stu-id="0170c-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="0170c-141">Der letzte Befehl erstellt einen Schlüssel namens ITHsmNonDefault, bei dem es sich um einen HSM-geschützten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="0170c-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="0170c-142">Der Befehl gibt Werte für zulässige Schlüsselvorgänge an, die $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="0170c-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="0170c-143">Der Befehl gibt Zeiten für die in den vorherigen Befehlen erstellten Parameter *"Expires"* und *"NotBefore"* sowie Tags für hohen Schweregrad und IT an.</span><span class="sxs-lookup"><span data-stu-id="0170c-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="0170c-144">Der neue Schlüssel ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0170c-144">The new key is disabled.</span></span> <span data-ttu-id="0170c-145">Sie können es mithilfe des **Cmdlets "Set-AzKeyVaultKey"** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0170c-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="0170c-146">Beispiel 4: Importieren eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0170c-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="0170c-147">Mit diesem Befehl wird der Schlüssel "ITByok" von dem vom *Parameter "KeyFilePath"* angegebenen Speicherort importiert.</span><span class="sxs-lookup"><span data-stu-id="0170c-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="0170c-148">Der importierte Schlüssel ist ein HSM-geschützter Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0170c-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="0170c-149">Um einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul zu importieren, müssen Sie zuerst mithilfe des Azure Key Vault BYOK Toolset ein "BYOK"-Paket (eine Datei mit der Dateinamenerweiterung BYOK) generieren.</span><span class="sxs-lookup"><span data-stu-id="0170c-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="0170c-150">Weitere Informationen finden Sie unter "Generieren und Übertragen HSM-Protected [Schlüssel für den Azure Key Vault".](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="0170c-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="0170c-151">Beispiel 5: Importieren eines softwaregeschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0170c-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="0170c-152">Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Password Variable.</span><span class="sxs-lookup"><span data-stu-id="0170c-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="0170c-153">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help
ConvertTo-SecureString` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="0170c-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="0170c-154">Der zweite Befehl erstellt ein Softwarekennwort im Contoso-Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0170c-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="0170c-155">Der Befehl gibt den Speicherort für den Schlüssel und das Kennwort an, die in der Datei $Password.</span><span class="sxs-lookup"><span data-stu-id="0170c-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="0170c-156">Beispiel 6: Importieren eines Schlüssels und Zuweisen von Attributen</span><span class="sxs-lookup"><span data-stu-id="0170c-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="0170c-157">Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Password Variable.</span><span class="sxs-lookup"><span data-stu-id="0170c-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="0170c-158">Der zweite Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein **DateTime-Objekt** und speichert dieses Objekt dann in der $Expires Variable.</span><span class="sxs-lookup"><span data-stu-id="0170c-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="0170c-159">Der dritte Befehl erstellt die $tags Variable zum Festlegen von Tags für hohen Schweregrad und IT.</span><span class="sxs-lookup"><span data-stu-id="0170c-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="0170c-160">Der endgültige Befehl importiert einen Schlüssel als HSM-Schlüssel von der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="0170c-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="0170c-161">Der Befehl gibt die in der Datei gespeicherte $Expires und das Kennwort an und wendet die in $Password gespeicherten Tags $tags.</span><span class="sxs-lookup"><span data-stu-id="0170c-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="0170c-162">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0170c-162">PARAMETERS</span></span>

### <span data-ttu-id="0170c-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0170c-163">-DefaultProfile</span></span>
<span data-ttu-id="0170c-164">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0170c-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0170c-165">-Destination</span><span class="sxs-lookup"><span data-stu-id="0170c-165">-Destination</span></span>
<span data-ttu-id="0170c-166">Gibt an, ob der Schlüssel als softwaregeschützter Oder HSM-geschützter Schlüssel im Schlüsseltresordienst hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0170c-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="0170c-167">Gültige Werte sind: HSM und Software.</span><span class="sxs-lookup"><span data-stu-id="0170c-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="0170c-168">Hinweis: Wenn Sie HSM als Ziel verwenden möchten, müssen Sie über einen Schlüsseltresor verfügen, der HSMs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0170c-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="0170c-169">Weitere Informationen zu den Dienststufen und -funktionen für den Azure Key Vault finden Sie auf der Website "Preise für [den Azure Key Vault".](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="0170c-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="0170c-170">Dieser Parameter ist erforderlich, wenn Sie einen neuen Schlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="0170c-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="0170c-171">Wenn Sie einen Schlüssel mithilfe des Parameters *"KeyFilePath"* importieren, ist dieser Parameter optional:</span><span class="sxs-lookup"><span data-stu-id="0170c-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="0170c-172">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel mit der Dateinamenerweiterung BYOK importiert, wird dieser Schlüssel als HSM-geschützter Schlüssel importiert.</span><span class="sxs-lookup"><span data-stu-id="0170c-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="0170c-173">Das Cmdlet kann diesen Schlüssel nicht als softwaregeschützten Schlüssel importieren.</span><span class="sxs-lookup"><span data-stu-id="0170c-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="0170c-174">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel mit der Dateinamenerweiterung PFX importiert, importiert es den Schlüssel als softwaregeschützten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0170c-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="0170c-175">-Disable</span><span class="sxs-lookup"><span data-stu-id="0170c-175">-Disable</span></span>
<span data-ttu-id="0170c-176">Gibt an, dass der hinzugefügte Schlüssel auf den anfänglichen Status "Deaktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0170c-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="0170c-177">Jeder Versuch, den Schlüssel zu verwenden, ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="0170c-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="0170c-178">Verwenden Sie diesen Parameter, wenn Sie Schlüssel vorab laden, die Sie später aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0170c-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="0170c-179">-Expires</span><span class="sxs-lookup"><span data-stu-id="0170c-179">-Expires</span></span>
<span data-ttu-id="0170c-180">Gibt die Ablaufzeit als **"DateTime"-Objekt** für den Schlüssel an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0170c-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="0170c-181">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="0170c-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0170c-182">Verwenden Sie das Get-Date-Cmdlet, um **ein "DateTime"-Objekt** zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="0170c-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0170c-183">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="0170c-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="0170c-184">Wenn Sie diesen Parameter nicht angeben, läuft der Schlüssel nicht ab.</span><span class="sxs-lookup"><span data-stu-id="0170c-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="0170c-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0170c-185">-InputObject</span></span>
<span data-ttu-id="0170c-186">Vault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0170c-186">Vault object.</span></span>

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

### <span data-ttu-id="0170c-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="0170c-187">-KeyFilePassword</span></span>
<span data-ttu-id="0170c-188">Gibt ein Kennwort für die importierte Datei als **SecureString-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0170c-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="0170c-189">Verwenden Sie zum **Abrufen eines SecureString-Objekts** **das Cmdlet ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="0170c-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="0170c-190">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help ConvertTo-SecureString` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="0170c-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="0170c-191">Sie müssen dieses Kennwort angeben, um eine Datei mit der Dateinamenerweiterung PFX zu importieren.</span><span class="sxs-lookup"><span data-stu-id="0170c-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="0170c-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="0170c-192">-KeyFilePath</span></span>
<span data-ttu-id="0170c-193">Gibt den Pfad einer lokalen Datei an, die Schlüsselmaterial enthält, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="0170c-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="0170c-194">Die gültigen Dateinamenerweiterungen sind BYOK und PFX.</span><span class="sxs-lookup"><span data-stu-id="0170c-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="0170c-195">Wenn es sich bei der Datei um eine byok-Datei handelt, wird der Schlüssel nach dem Import automatisch durch HSMs geschützt, und Sie können diesen Standard nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="0170c-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="0170c-196">Handelt es sich bei der Datei um eine PFX-Datei, wird der Schlüssel nach dem Import automatisch durch Software geschützt.</span><span class="sxs-lookup"><span data-stu-id="0170c-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="0170c-197">Um diesen Standard außer Kraft zu setzen, legen Sie den *Zielparameter* auf HSM fest, damit der Schlüssel HSM-geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="0170c-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="0170c-198">Wenn Sie diesen Parameter angeben, ist der *Zielparameter* optional.</span><span class="sxs-lookup"><span data-stu-id="0170c-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="0170c-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="0170c-199">-KeyOps</span></span>
<span data-ttu-id="0170c-200">Gibt ein Array von Vorgängen an, die mit dem von diesem Cmdlet hinzugefügten Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="0170c-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="0170c-201">Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0170c-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="0170c-202">Bei den zulässigen Werten für diesen Parameter handelt es sich um eine durch Kommas getrennte Liste von Schlüsselvorgängen gemäß der [JSON Web Key (JWK)-Spezifikation:](http://go.microsoft.com/fwlink/?LinkID=613300)</span><span class="sxs-lookup"><span data-stu-id="0170c-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="0170c-203">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="0170c-203">Encrypt</span></span>
- <span data-ttu-id="0170c-204">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="0170c-204">Decrypt</span></span>
- <span data-ttu-id="0170c-205">Umbruch</span><span class="sxs-lookup"><span data-stu-id="0170c-205">Wrap</span></span>
- <span data-ttu-id="0170c-206">Entpacken</span><span class="sxs-lookup"><span data-stu-id="0170c-206">Unwrap</span></span>
- <span data-ttu-id="0170c-207">Signieren</span><span class="sxs-lookup"><span data-stu-id="0170c-207">Sign</span></span>
- <span data-ttu-id="0170c-208">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="0170c-208">Verify</span></span>

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

### <span data-ttu-id="0170c-209">-Name</span><span class="sxs-lookup"><span data-stu-id="0170c-209">-Name</span></span>
<span data-ttu-id="0170c-210">Gibt den Namen des Schlüssels an, der dem Schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0170c-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="0170c-211">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0170c-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="0170c-212">Der Name muss eine Zeichenfolge von 1 bis 63 Zeichen lang sein, die nur 0-9, a-z, A-Z und - (das Strichsymbol) enthält.</span><span class="sxs-lookup"><span data-stu-id="0170c-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="0170c-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0170c-213">-NotBefore</span></span>
<span data-ttu-id="0170c-214">Gibt die Uhrzeit als **"DateTime"-Objekt** an, vor dem der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0170c-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="0170c-215">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="0170c-215">This parameter uses UTC.</span></span> <span data-ttu-id="0170c-216">Verwenden Sie das Get-Date-Cmdlet, um **ein "DateTime"-Objekt** zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="0170c-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0170c-217">Wenn Sie diesen Parameter nicht angeben, kann der Schlüssel sofort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0170c-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="0170c-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0170c-218">-ResourceId</span></span>
<span data-ttu-id="0170c-219">Vault Resource Id.</span><span class="sxs-lookup"><span data-stu-id="0170c-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="0170c-220">-Size</span><span class="sxs-lookup"><span data-stu-id="0170c-220">-Size</span></span>
<span data-ttu-id="0170c-221">RSA-Schlüsselgröße, in Bits.</span><span class="sxs-lookup"><span data-stu-id="0170c-221">RSA key size, in bits.</span></span> <span data-ttu-id="0170c-222">Wenn nichts angegeben wird, stellt der Dienst einen sicheren Standardwert zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0170c-222">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="0170c-223">-Tag</span><span class="sxs-lookup"><span data-stu-id="0170c-223">-Tag</span></span>
<span data-ttu-id="0170c-224">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0170c-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0170c-225">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0170c-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0170c-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0170c-226">-VaultName</span></span>
<span data-ttu-id="0170c-227">Gibt den Namen des Schlüsseltresor an, dem dieses Cmdlet den Schlüssel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0170c-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="0170c-228">Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0170c-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="0170c-229">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0170c-229">-Confirm</span></span>
<span data-ttu-id="0170c-230">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0170c-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0170c-231">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0170c-231">-WhatIf</span></span>
<span data-ttu-id="0170c-232">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0170c-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0170c-233">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0170c-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0170c-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0170c-234">CommonParameters</span></span>
<span data-ttu-id="0170c-235">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0170c-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0170c-236">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0170c-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0170c-237">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0170c-237">INPUTS</span></span>

### <span data-ttu-id="0170c-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0170c-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0170c-239">System.String</span><span class="sxs-lookup"><span data-stu-id="0170c-239">System.String</span></span>

## <span data-ttu-id="0170c-240">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0170c-240">OUTPUTS</span></span>

### <span data-ttu-id="0170c-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0170c-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="0170c-242">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0170c-242">NOTES</span></span>

## <span data-ttu-id="0170c-243">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0170c-243">RELATED LINKS</span></span>

[<span data-ttu-id="0170c-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0170c-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="0170c-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0170c-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="0170c-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0170c-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

