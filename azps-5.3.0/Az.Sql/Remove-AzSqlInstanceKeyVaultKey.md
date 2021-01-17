---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460603"
---
# <span data-ttu-id="df1e6-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="df1e6-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="df1e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="df1e6-103">Entfernt einen Schlüssel im Tresor aus einer verwalteten SQL Instanz</span><span class="sxs-lookup"><span data-stu-id="df1e6-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="df1e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df1e6-104">SYNTAX</span></span>

### <span data-ttu-id="df1e6-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="df1e6-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df1e6-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df1e6-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df1e6-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df1e6-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df1e6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df1e6-108">DESCRIPTION</span></span>
<span data-ttu-id="df1e6-109">Das Remove-AzSqlInstanceKeyVaultKey cmdlet entfernt den Schlüssel "Schlüsseltresor" aus der angegebenen verwalteten Instanz.</span><span class="sxs-lookup"><span data-stu-id="df1e6-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="df1e6-110">Beachten Sie, dass SQL verwalteten Instanzberechtigungen für den Tresor des Schlüssels nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="df1e6-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="df1e6-111">Verwenden Sie Set-AzKeyVaultAccessPolicy, um Berechtigungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="df1e6-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="df1e6-112">Beachten Sie, dass dieses Cmdlet keine Änderungen am Schlüsseltresor vor nimmt.</span><span class="sxs-lookup"><span data-stu-id="df1e6-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="df1e6-113">Verwenden Sie "Remove-AzureKeyVaultKey", um einen Schlüssel aus dem Schlüsseltresor zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="df1e6-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="df1e6-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df1e6-114">EXAMPLES</span></span>

### <span data-ttu-id="df1e6-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df1e6-115">Example 1</span></span>
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

<span data-ttu-id="df1e6-116">Mit diesem Befehl wird der Schlüssel "Schlüsseltresor" mit "ID" https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="df1e6-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="df1e6-117">Beispiel 2: Verwenden eines verwalteten Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="df1e6-117">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="df1e6-118">Mit diesem Befehl wird der Schlüssel "Schlüsseltresor" mit "ID" https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="df1e6-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="df1e6-119">Beispiel 3: Verwenden der Ressourcen-ID einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="df1e6-119">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="df1e6-120">Mit diesem Befehl wird der Schlüssel "Schlüsseltresor" mit "ID" https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="df1e6-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="df1e6-121">Beispiel 4: Verwenden der Pipette</span><span class="sxs-lookup"><span data-stu-id="df1e6-121">Example 4: Using piping</span></span>
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

<span data-ttu-id="df1e6-122">Mit diesem Befehl wird der Schlüssel "Schlüsseltresor" mit "ID" https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 aus der angegebenen verwalteten Instanz entfernt.</span><span class="sxs-lookup"><span data-stu-id="df1e6-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="df1e6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df1e6-123">PARAMETERS</span></span>

### <span data-ttu-id="df1e6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1e6-124">-DefaultProfile</span></span>
<span data-ttu-id="df1e6-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df1e6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1e6-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="df1e6-126">-Instance</span></span>
<span data-ttu-id="df1e6-127">Das Instanzeingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="df1e6-127">The instance input object</span></span>

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

### <span data-ttu-id="df1e6-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="df1e6-128">-InstanceName</span></span>
<span data-ttu-id="df1e6-129">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="df1e6-129">The instance name</span></span>

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

### <span data-ttu-id="df1e6-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="df1e6-130">-InstanceResourceId</span></span>
<span data-ttu-id="df1e6-131">Die Instanzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="df1e6-131">The instance resource id</span></span>

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

### <span data-ttu-id="df1e6-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="df1e6-132">-KeyId</span></span>
<span data-ttu-id="df1e6-133">AzureKeyVault-Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="df1e6-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="df1e6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1e6-134">-ResourceGroupName</span></span>
<span data-ttu-id="df1e6-135">Der Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="df1e6-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="df1e6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df1e6-136">-Confirm</span></span>
<span data-ttu-id="df1e6-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df1e6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1e6-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="df1e6-138">-WhatIf</span></span>
<span data-ttu-id="df1e6-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df1e6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df1e6-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df1e6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1e6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1e6-141">CommonParameters</span></span>
<span data-ttu-id="df1e6-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1e6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1e6-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df1e6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1e6-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df1e6-144">INPUTS</span></span>

### <span data-ttu-id="df1e6-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="df1e6-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="df1e6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="df1e6-146">System.String</span></span>

## <span data-ttu-id="df1e6-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df1e6-147">OUTPUTS</span></span>

### <span data-ttu-id="df1e6-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="df1e6-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="df1e6-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="df1e6-149">NOTES</span></span>

## <span data-ttu-id="df1e6-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="df1e6-150">RELATED LINKS</span></span>
