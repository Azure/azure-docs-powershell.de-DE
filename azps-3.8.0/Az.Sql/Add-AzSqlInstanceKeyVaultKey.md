---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995972"
---
# <span data-ttu-id="2d262-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d262-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="2d262-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d262-102">SYNOPSIS</span></span>
<span data-ttu-id="2d262-103">Fügt der bereitgestellten verwalteten Instanz einen Key Vault-Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d262-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="2d262-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d262-104">SYNTAX</span></span>

### <span data-ttu-id="2d262-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d262-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d262-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d262-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d262-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d262-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d262-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d262-108">DESCRIPTION</span></span>
<span data-ttu-id="2d262-109">Das Add-AzSqlInstanceKeyVaultKey-Cmdlet fügt der bereitgestellten verwalteten Instanz einen Key Vault-Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d262-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="2d262-110">Die verwaltete Instanz muss über die Berechtigungen "abrufen, wrapKey, unwrapKey" für den Tresor verfügen, indem Sie das folgende Skript verwenden, um der verwalteten Instanz die Berechtigung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="2d262-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="2d262-111">$managedInstance = Get-AzSqlInstance-Name "ContosoManagedInstanceName"-ResourceGroupName "ContosoResourceGroup" Set-AzKeyVaultAccessPolicy-vaultname ContosoVault-ObjectID $managedInstance. Identity. Principal-PermissionsToKeys, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="2d262-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="2d262-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d262-112">EXAMPLES</span></span>

### <span data-ttu-id="2d262-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d262-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="2d262-114">Dieser Befehl fügt der SQL-verwalteten Instanz mit dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Namen "ContosoManagedInstanceName" in der Ressourcengruppe "ContosoResourceGroup" den Key Vault-Schlüssel mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d262-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="2d262-115">Beispiel 2: Verwenden eines verwalteten Instanzen Objekts</span><span class="sxs-lookup"><span data-stu-id="2d262-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="2d262-116">Dieser Befehl fügt der SQL-verwalteten Instanz mit dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Namen "ContosoManagedInstanceName" in der Ressourcengruppe "ContosoResourceGroup" den Key Vault-Schlüssel mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d262-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="2d262-117">Beispiel 3: Verwenden der Ressourcen-ID für verwaltete Instanzen</span><span class="sxs-lookup"><span data-stu-id="2d262-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="2d262-118">Dieser Befehl fügt der SQL-verwalteten Instanz mit dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Namen "ContosoManagedInstanceName" in der Ressourcengruppe "ContosoResourceGroup" den Key Vault-Schlüssel mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d262-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="2d262-119">Beispiel 4: Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="2d262-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="2d262-120">Dieser Befehl fügt der SQL-verwalteten Instanz mit dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Namen "ContosoManagedInstanceName" in der Ressourcengruppe "ContosoResourceGroup" den Key Vault-Schlüssel mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d262-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="2d262-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d262-121">PARAMETERS</span></span>

### <span data-ttu-id="2d262-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d262-122">-DefaultProfile</span></span>
<span data-ttu-id="2d262-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d262-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d262-124">-Instanz</span><span class="sxs-lookup"><span data-stu-id="2d262-124">-Instance</span></span>
<span data-ttu-id="2d262-125">Das Instanzen Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="2d262-125">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d262-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2d262-126">-InstanceName</span></span>
<span data-ttu-id="2d262-127">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="2d262-127">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d262-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="2d262-128">-InstanceResourceId</span></span>
<span data-ttu-id="2d262-129">Die Ressourcen-ID der Instanz</span><span class="sxs-lookup"><span data-stu-id="2d262-129">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d262-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="2d262-130">-KeyId</span></span>
<span data-ttu-id="2d262-131">AzureKeyVault-Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="2d262-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="2d262-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d262-132">-ResourceGroupName</span></span>
<span data-ttu-id="2d262-133">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2d262-133">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d262-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d262-134">-Confirm</span></span>
<span data-ttu-id="2d262-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d262-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d262-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d262-136">-WhatIf</span></span>
<span data-ttu-id="2d262-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d262-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d262-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d262-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d262-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d262-139">CommonParameters</span></span>
<span data-ttu-id="2d262-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d262-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d262-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d262-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d262-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d262-142">INPUTS</span></span>

### <span data-ttu-id="2d262-143">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="2d262-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="2d262-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2d262-144">System.String</span></span>

## <span data-ttu-id="2d262-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d262-145">OUTPUTS</span></span>

### <span data-ttu-id="2d262-146">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="2d262-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="2d262-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d262-147">NOTES</span></span>

## <span data-ttu-id="2d262-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d262-148">RELATED LINKS</span></span>
