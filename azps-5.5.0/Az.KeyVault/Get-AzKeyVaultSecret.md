---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 6824777d5df0f06705f4c10c4af248f1f8e8714a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175268"
---
# <span data-ttu-id="19c7a-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19c7a-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="19c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="19c7a-103">Ruft die geheimen Daten in einem Schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="19c7a-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="19c7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19c7a-104">SYNTAX</span></span>

### <span data-ttu-id="19c7a-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="19c7a-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="19c7a-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="19c7a-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="19c7a-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="19c7a-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="19c7a-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="19c7a-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="19c7a-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c7a-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="19c7a-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19c7a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19c7a-114">DESCRIPTION</span></span>
<span data-ttu-id="19c7a-115">Das **Get-AzKeyVaultSecret-Cmdlet** erhält geheime Daten in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="19c7a-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="19c7a-116">Dieses Cmdlet erhält ein bestimmtes Geheimes oder alle geheimen Daten in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="19c7a-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="19c7a-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="19c7a-117">EXAMPLES</span></span>

### <span data-ttu-id="19c7a-118">Beispiel 1: Erhalten aller aktuellen Versionen aller geheimen Daten in einem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="19c7a-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="19c7a-119">Dieser Befehl ruft die aktuellen Versionen aller geheimen Daten im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="19c7a-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="19c7a-120">Beispiel 2: Alle Versionen eines bestimmten geheimen Schlüssels erhalten</span><span class="sxs-lookup"><span data-stu-id="19c7a-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="19c7a-121">Dieser Befehl ruft alle Versionen des geheimen Namens "secret1" im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="19c7a-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="19c7a-122">Beispiel 3: Erhalten der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="19c7a-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="19c7a-123">Dieser Befehl ruft die aktuelle Version des geheimen Namens "secret1" im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="19c7a-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="19c7a-124">Beispiel 4: Erhalten einer bestimmten Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="19c7a-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="19c7a-125">Dieser Befehl ruft eine bestimmte Version des geheimen Namens "secret1" im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="19c7a-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="19c7a-126">Beispiel 5: Den Nur-Text-Wert der aktuellen Version eines bestimmten geheimen Schlüssels erhalten</span><span class="sxs-lookup"><span data-stu-id="19c7a-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

<span data-ttu-id="19c7a-127">Das Cmdlet gibt das Geheime als Zeichenfolge zurück, wenn `-AsPlainText` es angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="19c7a-127">The cmdlet returns the secret as a string when `-AsPlainText` is applied.</span></span>

### <span data-ttu-id="19c7a-128">Beispiel 6: Erhalten Sie alle geheimen Daten, die für diesen Schlüsseltresor gelöscht, aber nicht gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="19c7a-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="19c7a-129">Dieser Befehl ruft alle geheimen Daten ab, die zuvor gelöscht, aber nicht gelöscht wurden, im Schlüsseltresor "Contoso".</span><span class="sxs-lookup"><span data-stu-id="19c7a-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="19c7a-130">Beispiel 7: Ruft den geheimen ITSecret ab, der für diesen Schlüsseltresor gelöscht, aber nicht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="19c7a-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="19c7a-131">Dieser Befehl ruft den geheimen "geheimen1" ab, der zuvor im Schlüsseltresor "Contoso" gelöscht, aber nicht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="19c7a-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="19c7a-132">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten geheimen Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="19c7a-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="19c7a-133">Beispiel 8: Erhalten aller aktuellen Versionen aller geheimen Daten in einem Schlüsseltresor mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="19c7a-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="19c7a-134">Dieser Befehl ruft die aktuellen Versionen aller geheimen Daten im Schlüsseltresor "Contoso" ab, die mit "geheim" beginnen.</span><span class="sxs-lookup"><span data-stu-id="19c7a-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="19c7a-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c7a-135">PARAMETERS</span></span>

### <span data-ttu-id="19c7a-136">-AsPlainText</span><span class="sxs-lookup"><span data-stu-id="19c7a-136">-AsPlainText</span></span>
<span data-ttu-id="19c7a-137">Wenn dies festgelegt ist, konvertiert das Cmdlet den geheimen Schlüssel in der sicheren Zeichenfolge als Ausgabe in die entschlüsselte Nur-Text-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="19c7a-137">When set, the cmdlet will convert secret in secure string to the decrypted plaintext string as output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, BySecretName, ByInputObjectVaultName, ByInputObjectSecretName, ByResourceIdVaultName, ByResourceIdSecretName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c7a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c7a-138">-DefaultProfile</span></span>
<span data-ttu-id="19c7a-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="19c7a-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19c7a-140">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="19c7a-140">-IncludeVersions</span></span>
<span data-ttu-id="19c7a-141">Gibt an, dass dieses Cmdlet alle Versionen eines geheimen Schlüssels erhält.</span><span class="sxs-lookup"><span data-stu-id="19c7a-141">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="19c7a-142">Die aktuelle Version eines Geheimen ist die erste Version in der Liste.</span><span class="sxs-lookup"><span data-stu-id="19c7a-142">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="19c7a-143">Wenn Sie diesen Parameter angeben, müssen Sie auch die *Parameter "Name"* und *"VaultName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="19c7a-143">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="19c7a-144">Wenn Sie den Parameter *"IncludeVersions"* nicht angeben, ruft dieses Cmdlet die aktuelle Version des Geheimen mit dem angegebenen *Namen ab.*</span><span class="sxs-lookup"><span data-stu-id="19c7a-144">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c7a-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19c7a-145">-InputObject</span></span>
<span data-ttu-id="19c7a-146">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="19c7a-146">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c7a-147">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="19c7a-147">-InRemovedState</span></span>
<span data-ttu-id="19c7a-148">Gibt an, ob die zuvor gelöschten geheimen Daten in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19c7a-148">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="19c7a-149">-Name</span><span class="sxs-lookup"><span data-stu-id="19c7a-149">-Name</span></span>
<span data-ttu-id="19c7a-150">Gibt den Namen des geheimen Schlüssels an, den Sie erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="19c7a-150">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="19c7a-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19c7a-151">-ResourceId</span></span>
<span data-ttu-id="19c7a-152">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="19c7a-152">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c7a-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="19c7a-153">-VaultName</span></span>
<span data-ttu-id="19c7a-154">Gibt den Namen des Schlüsseltresor an, zu dem das Geheimnis gehört.</span><span class="sxs-lookup"><span data-stu-id="19c7a-154">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="19c7a-155">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="19c7a-155">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c7a-156">-Version</span><span class="sxs-lookup"><span data-stu-id="19c7a-156">-Version</span></span>
<span data-ttu-id="19c7a-157">Gibt die geheime Version an.</span><span class="sxs-lookup"><span data-stu-id="19c7a-157">Specifies the secret version.</span></span>
<span data-ttu-id="19c7a-158">Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem Namen des Schlüsseltresor, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="19c7a-158">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c7a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c7a-159">CommonParameters</span></span>
<span data-ttu-id="19c7a-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c7a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c7a-161">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19c7a-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c7a-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="19c7a-162">INPUTS</span></span>

### <span data-ttu-id="19c7a-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="19c7a-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="19c7a-164">System.String</span><span class="sxs-lookup"><span data-stu-id="19c7a-164">System.String</span></span>

## <span data-ttu-id="19c7a-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="19c7a-165">OUTPUTS</span></span>

### <span data-ttu-id="19c7a-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="19c7a-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="19c7a-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19c7a-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="19c7a-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="19c7a-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="19c7a-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19c7a-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="19c7a-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="19c7a-170">NOTES</span></span>

## <span data-ttu-id="19c7a-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="19c7a-171">RELATED LINKS</span></span>

[<span data-ttu-id="19c7a-172">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19c7a-172">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="19c7a-173">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="19c7a-173">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="19c7a-174">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19c7a-174">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

