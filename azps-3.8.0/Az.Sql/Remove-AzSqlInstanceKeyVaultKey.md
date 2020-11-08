---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003152"
---
# <span data-ttu-id="522b2-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="522b2-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="522b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="522b2-102">SYNOPSIS</span></span>
<span data-ttu-id="522b2-103">Entfernt einen Key Vault-Schlüssel aus einer verwalteten SQL-Instanz</span><span class="sxs-lookup"><span data-stu-id="522b2-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="522b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="522b2-104">SYNTAX</span></span>

### <span data-ttu-id="522b2-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="522b2-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522b2-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="522b2-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522b2-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="522b2-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="522b2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="522b2-108">DESCRIPTION</span></span>
<span data-ttu-id="522b2-109">Das Remove-AzSqlInstanceKeyVaultKey-Cmdlet entfernt den schlüsseltresor Schlüssel aus der angegebenen verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="522b2-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="522b2-110">Beachten Sie, dass die Berechtigungen der verwalteten SQL-Instanz für den Tresor des Schlüssels nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="522b2-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="522b2-111">Wenn Sie Berechtigungen ändern möchten, verwenden Sie die Einstellung-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="522b2-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="522b2-112">Beachten Sie, dass dieses Cmdlet keine Änderungen an Key Vault vornimmt.</span><span class="sxs-lookup"><span data-stu-id="522b2-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="522b2-113">Wenn Sie einen Schlüssel aus dem Schlüsselspeicher entfernen möchten, verwenden Sie Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="522b2-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="522b2-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="522b2-114">EXAMPLES</span></span>

### <span data-ttu-id="522b2-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="522b2-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="522b2-116">Mit diesem Befehl wird der schlüsseltresor Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="522b2-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="522b2-117">Beispiel 2: Verwenden eines verwalteten Instanzen Objekts</span><span class="sxs-lookup"><span data-stu-id="522b2-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="522b2-118">Mit diesem Befehl wird der schlüsseltresor Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="522b2-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="522b2-119">Beispiel 3: Verwenden der Ressourcen-ID für verwaltete Instanzen</span><span class="sxs-lookup"><span data-stu-id="522b2-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="522b2-120">Mit diesem Befehl wird der schlüsseltresor Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="522b2-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="522b2-121">Beispiel 4: Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="522b2-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="522b2-122">Mit diesem Befehl wird der schlüsseltresor Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="522b2-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="522b2-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="522b2-123">PARAMETERS</span></span>

### <span data-ttu-id="522b2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522b2-124">-DefaultProfile</span></span>
<span data-ttu-id="522b2-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="522b2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="522b2-126">-Instanz</span><span class="sxs-lookup"><span data-stu-id="522b2-126">-Instance</span></span>
<span data-ttu-id="522b2-127">Das Instanzen Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="522b2-127">The instance input object</span></span>

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

### <span data-ttu-id="522b2-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="522b2-128">-InstanceName</span></span>
<span data-ttu-id="522b2-129">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="522b2-129">The instance name</span></span>

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

### <span data-ttu-id="522b2-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="522b2-130">-InstanceResourceId</span></span>
<span data-ttu-id="522b2-131">Die Ressourcen-ID der Instanz</span><span class="sxs-lookup"><span data-stu-id="522b2-131">The instance resource id</span></span>

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

### <span data-ttu-id="522b2-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="522b2-132">-KeyId</span></span>
<span data-ttu-id="522b2-133">AzureKeyVault-Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="522b2-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="522b2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="522b2-134">-ResourceGroupName</span></span>
<span data-ttu-id="522b2-135">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="522b2-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="522b2-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="522b2-136">-Confirm</span></span>
<span data-ttu-id="522b2-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="522b2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="522b2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="522b2-138">-WhatIf</span></span>
<span data-ttu-id="522b2-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="522b2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="522b2-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="522b2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="522b2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522b2-141">CommonParameters</span></span>
<span data-ttu-id="522b2-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="522b2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522b2-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="522b2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522b2-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="522b2-144">INPUTS</span></span>

### <span data-ttu-id="522b2-145">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="522b2-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="522b2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="522b2-146">System.String</span></span>

## <span data-ttu-id="522b2-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="522b2-147">OUTPUTS</span></span>

### <span data-ttu-id="522b2-148">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="522b2-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="522b2-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="522b2-149">NOTES</span></span>

## <span data-ttu-id="522b2-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="522b2-150">RELATED LINKS</span></span>
