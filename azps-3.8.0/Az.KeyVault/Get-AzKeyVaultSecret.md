---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: af2baec6b25b770c30f5f3207e6ed6b6a4b423f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995390"
---
# <span data-ttu-id="0e4a5-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e4a5-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="0e4a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4a5-103">Ruft die Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="0e4a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e4a5-104">SYNTAX</span></span>

### <span data-ttu-id="0e4a5-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e4a5-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="0e4a5-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="0e4a5-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="0e4a5-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="0e4a5-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="0e4a5-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="0e4a5-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="0e4a5-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4a5-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="0e4a5-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e4a5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e4a5-114">DESCRIPTION</span></span>
<span data-ttu-id="0e4a5-115">Das Cmdlet " **Get-AzKeyVaultSecret** " erhält in einem schlüsseltresor Geheimnisse.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="0e4a5-116">Dieses Cmdlet ruft einen bestimmten geheimen oder alle Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="0e4a5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e4a5-117">EXAMPLES</span></span>

### <span data-ttu-id="0e4a5-118">Beispiel 1: Abrufen aller aktuellen Versionen aller Geheimnisse in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="0e4a5-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="0e4a5-119">Mit diesem Befehl werden die aktuellen Versionen aller Geheimnisse im schlüsseltresor mit dem Namen contoso abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="0e4a5-120">Beispiel 2: Abrufen aller Versionen eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0e4a5-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="0e4a5-121">Dieser Befehl ruft alle Versionen des geheimen namens secret1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="0e4a5-122">Beispiel 3: Abrufen der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0e4a5-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="0e4a5-123">Dieser Befehl ruft die aktuelle Version des geheimen namens secret1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="0e4a5-124">Beispiel 4: Abrufen einer bestimmten Version eines bestimmten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="0e4a5-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="0e4a5-125">Dieser Befehl ruft eine bestimmte Version des geheimen namens secret1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="0e4a5-126">Beispiel 5: Abrufen des nur-Text-Werts der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="0e4a5-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="0e4a5-127">Diese Befehle rufen die aktuelle Version eines geheimen namens ITSecret ab und zeigen dann den nur-Text-Wert dieses geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="0e4a5-128">Beispiel 6: Abrufen aller für diesen schlüsseltresor gelöschten, aber nicht bereinigten Geheimnisse</span><span class="sxs-lookup"><span data-stu-id="0e4a5-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="0e4a5-129">Dieser Befehl ruft alle Geheimnisse ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="0e4a5-130">Beispiel 7: Ruft den geheimen ITSecret ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="0e4a5-131">Dieser Befehl ruft den geheimen "secret1" ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="0e4a5-132">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum für diesen gelöschten Schlüssel zurück.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="0e4a5-133">Beispiel 8: Abrufen aller aktuellen Versionen aller Geheimnisse in einem schlüsseltresor mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="0e4a5-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="0e4a5-134">Dieser Befehl ruft die aktuellen Versionen aller Geheimnisse im schlüsseltresor mit dem Namen "Contoso" ab, die mit "Secret" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="0e4a5-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e4a5-135">PARAMETERS</span></span>

### <span data-ttu-id="0e4a5-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4a5-136">-DefaultProfile</span></span>
<span data-ttu-id="0e4a5-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0e4a5-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e4a5-138">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="0e4a5-138">-IncludeVersions</span></span>
<span data-ttu-id="0e4a5-139">Gibt an, dass dieses Cmdlet alle Versionen eines geheimen Schlüssels abruft.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-139">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="0e4a5-140">Die aktuelle Version eines Geheimnisses ist die erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-140">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="0e4a5-141">Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-141">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="0e4a5-142">Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des geheimen Schlüssels mit dem angegebenen *Namen* ab.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-142">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="0e4a5-143">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e4a5-143">-InputObject</span></span>
<span data-ttu-id="0e4a5-144">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-144">KeyVault Object.</span></span>

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

### <span data-ttu-id="0e4a5-145">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0e4a5-145">-InRemovedState</span></span>
<span data-ttu-id="0e4a5-146">Gibt an, ob die zuvor gelöschten Geheimnisse in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-146">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="0e4a5-147">-Name</span><span class="sxs-lookup"><span data-stu-id="0e4a5-147">-Name</span></span>
<span data-ttu-id="0e4a5-148">Gibt den Namen des abzurufenden Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-148">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4a5-149">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0e4a5-149">-ResourceId</span></span>
<span data-ttu-id="0e4a5-150">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-150">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="0e4a5-151">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="0e4a5-151">-VaultName</span></span>
<span data-ttu-id="0e4a5-152">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-152">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="0e4a5-153">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-153">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="0e4a5-154">-Version</span><span class="sxs-lookup"><span data-stu-id="0e4a5-154">-Version</span></span>
<span data-ttu-id="0e4a5-155">Gibt die geheime Version an.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-155">Specifies the secret version.</span></span>
<span data-ttu-id="0e4a5-156">Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-156">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="0e4a5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4a5-157">CommonParameters</span></span>
<span data-ttu-id="0e4a5-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e4a5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4a5-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e4a5-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4a5-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e4a5-160">INPUTS</span></span>

### <span data-ttu-id="0e4a5-161">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0e4a5-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0e4a5-162">System. String</span><span class="sxs-lookup"><span data-stu-id="0e4a5-162">System.String</span></span>

## <span data-ttu-id="0e4a5-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e4a5-163">OUTPUTS</span></span>

### <span data-ttu-id="0e4a5-164">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0e4a5-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="0e4a5-165">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e4a5-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="0e4a5-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0e4a5-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="0e4a5-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e4a5-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="0e4a5-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e4a5-168">NOTES</span></span>

## <span data-ttu-id="0e4a5-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e4a5-169">RELATED LINKS</span></span>

[<span data-ttu-id="0e4a5-170">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e4a5-170">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="0e4a5-171">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="0e4a5-171">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="0e4a5-172">Satz-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e4a5-172">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

