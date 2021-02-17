---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: e0601285bf2adc7204cd5a946e07d032579e080b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404716"
---
# <span data-ttu-id="bc3fd-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc3fd-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="bc3fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3fd-103">Ruft Die Schlüssel des Tresors ab.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="bc3fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc3fd-104">SYNTAX</span></span>

### <span data-ttu-id="bc3fd-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc3fd-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="bc3fd-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bc3fd-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="bc3fd-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="bc3fd-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bc3fd-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="bc3fd-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="bc3fd-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc3fd-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bc3fd-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc3fd-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc3fd-114">DESCRIPTION</span></span>
<span data-ttu-id="bc3fd-115">Das **Cmdlet "Get-AzKeyVaultKey"** ruft Azure Key Vault Keys ab.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="bc3fd-116">Dieses Cmdlet ruft ein bestimmtes **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** oder eine Liste aller **KeyBundle-Objekte** in einem Schlüsseltresor oder nach Version ab.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="bc3fd-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc3fd-117">EXAMPLES</span></span>

### <span data-ttu-id="bc3fd-118">Beispiel 1: Alle Schlüssel in einem Schlüsseltresor erhalten</span><span class="sxs-lookup"><span data-stu-id="bc3fd-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="bc3fd-119">Dieser Befehl ruft alle Schlüssel im Schlüsseltresor namens Contoso ab.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="bc3fd-120">Beispiel 2: Erhalten der aktuellen Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="bc3fd-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="bc3fd-121">Dieser Befehl ruft die aktuelle Version des Schlüssels namens "Test1" im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="bc3fd-122">Beispiel 3: Alle Versionen eines Schlüssels erhalten</span><span class="sxs-lookup"><span data-stu-id="bc3fd-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="bc3fd-123">Dieser Befehl ruft alle Versionen ab, die den Schlüssel "ITPfx" im Schlüsseltresor "Contoso" haben.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="bc3fd-124">Beispiel 4: Erhalten einer bestimmten Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="bc3fd-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="bc3fd-125">Dieser Befehl ruft eine bestimmte Version des Schlüssels namens "Test1" im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="bc3fd-126">Nachdem Sie diesen Befehl ausgeführt haben, können Sie verschiedene Eigenschaften des Schlüssels prüfen, indem Sie im $Key navigieren.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="bc3fd-127">Beispiel 5: Hier erhalten Sie alle Schlüssel, die für diesen Schlüsseltresor gelöscht, aber nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="bc3fd-128">Dieser Befehl ruft alle Schlüssel ab, die zuvor gelöscht, aber nicht gelöscht wurden, im Schlüsseltresor "Contoso".</span><span class="sxs-lookup"><span data-stu-id="bc3fd-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="bc3fd-129">Beispiel 6: Ruft den wichtigsten ITPfx-Server ab, der gelöscht, aber nicht für diesen Schlüsseltresor gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="bc3fd-130">Dieser Befehl ruft den Schlüsseltest3 ab, der zuvor im Schlüsseltresor "Contoso" gelöscht, aber nicht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="bc3fd-131">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="bc3fd-132">Beispiel 7: Erhalten aller Schlüssel in einem Schlüsseltresor mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="bc3fd-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="bc3fd-133">Dieser Befehl ruft alle Schlüssel im Schlüsseltresor "Contoso" ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="bc3fd-134">Beispiel 8: Herunterladen eines öffentlichen Schlüssels als PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="bc3fd-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="bc3fd-135">Sie können den öffentlichen Schlüssel eines RSA-Schlüssels herunterladen, indem Sie den Parameter `-OutFile` angeben.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="bc3fd-136">Dies ist ein Schritt beim Importieren von HSM-geschützten Schlüsseln in den Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="bc3fd-137">Sieh https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="bc3fd-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="bc3fd-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc3fd-138">PARAMETERS</span></span>

### <span data-ttu-id="bc3fd-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3fd-139">-DefaultProfile</span></span>
<span data-ttu-id="bc3fd-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bc3fd-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc3fd-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="bc3fd-141">-IncludeVersions</span></span>
<span data-ttu-id="bc3fd-142">Gibt an, dass dieses Cmdlet alle Versionen eines Schlüssels erhält.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="bc3fd-143">Die aktuelle Version eines Schlüssels ist die erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="bc3fd-144">Wenn Sie diesen Parameter angeben, müssen Sie auch die *Parameter "Name"* und *"VaultName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="bc3fd-145">Wenn Sie den Parameter *"IncludeVersions"* nicht angeben, ruft dieses Cmdlet die aktuelle Version des Schlüssels mit dem angegebenen *Namen ab.*</span><span class="sxs-lookup"><span data-stu-id="bc3fd-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc3fd-146">-InputObject</span></span>
<span data-ttu-id="bc3fd-147">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-147">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="bc3fd-148">-InRemovedState</span></span>
<span data-ttu-id="bc3fd-149">Gibt an, ob die zuvor gelöschten Schlüssel in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-149">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-150">-Name</span><span class="sxs-lookup"><span data-stu-id="bc3fd-150">-Name</span></span>
<span data-ttu-id="bc3fd-151">Gibt den Namen des zu erhaltenden Schlüsselbündels an.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-152">-OutFile</span><span class="sxs-lookup"><span data-stu-id="bc3fd-152">-OutFile</span></span>
<span data-ttu-id="bc3fd-153">Gibt die Ausgabedatei an, für die dieser Schlüssel von diesem Cmdlet gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="bc3fd-154">Der öffentliche Schlüssel wird standardmäßig im PEM-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-154">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc3fd-155">-ResourceId</span></span>
<span data-ttu-id="bc3fd-156">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-156">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bc3fd-157">-VaultName</span></span>
<span data-ttu-id="bc3fd-158">Gibt den Namen des Schlüsseltresor an, aus dem dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="bc3fd-159">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und der ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-160">-Version</span><span class="sxs-lookup"><span data-stu-id="bc3fd-160">-Version</span></span>
<span data-ttu-id="bc3fd-161">Gibt die Schlüsselversion an.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-161">Specifies the key version.</span></span>
<span data-ttu-id="bc3fd-162">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem Namen des Schlüsseltresor, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüsselversion.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc3fd-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3fd-163">CommonParameters</span></span>
<span data-ttu-id="bc3fd-164">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc3fd-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3fd-165">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc3fd-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3fd-166">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc3fd-166">INPUTS</span></span>

### <span data-ttu-id="bc3fd-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bc3fd-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="bc3fd-168">System.String</span><span class="sxs-lookup"><span data-stu-id="bc3fd-168">System.String</span></span>

## <span data-ttu-id="bc3fd-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc3fd-169">OUTPUTS</span></span>

### <span data-ttu-id="bc3fd-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bc3fd-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bc3fd-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc3fd-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="bc3fd-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bc3fd-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bc3fd-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc3fd-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="bc3fd-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bc3fd-174">NOTES</span></span>

## <span data-ttu-id="bc3fd-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bc3fd-175">RELATED LINKS</span></span>

[<span data-ttu-id="bc3fd-176">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc3fd-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="bc3fd-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bc3fd-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="bc3fd-178">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="bc3fd-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


