---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289913"
---
# <span data-ttu-id="a5065-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a5065-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="a5065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5065-102">SYNOPSIS</span></span>
<span data-ttu-id="a5065-103">Ruft die SQL einer verwalteten Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="a5065-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="a5065-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5065-104">SYNTAX</span></span>

### <span data-ttu-id="a5065-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5065-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5065-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5065-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5065-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5065-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5065-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5065-108">DESCRIPTION</span></span>
<span data-ttu-id="a5065-109">Das Get-AzSqlInstanceKeyVaultKey cmdlet ruft Informationen zu den Schlüsseln des Tresors in einer verwalteten instanz SQL ab.</span><span class="sxs-lookup"><span data-stu-id="a5065-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="a5065-110">Sie können alle Schlüssel in einer verwalteten Instanz oder einen bestimmten Schlüssel anzeigen, indem Sie die KeyId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a5065-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="a5065-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5065-111">EXAMPLES</span></span>

### <span data-ttu-id="a5065-112">Beispiel 1: Alle Schlüssel des Tresors erhalten</span><span class="sxs-lookup"><span data-stu-id="a5065-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a5065-113">Dieser Befehl ruft alle Schlüssel des Schlüsseltresor einer verwalteten instanz SQL ab.</span><span class="sxs-lookup"><span data-stu-id="a5065-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="a5065-114">Beispiel 2: Erhalten eines bestimmten Schlüsseltresorschlüssels</span><span class="sxs-lookup"><span data-stu-id="a5065-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a5065-115">Dieser Befehl ruft den Schlüssel des Schlüsseltresor mit der ID ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ab.</span><span class="sxs-lookup"><span data-stu-id="a5065-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="a5065-116">Beispiel 3: Verwenden eines Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="a5065-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a5065-117">Dieser Befehl ruft den Schlüssel des Schlüsseltresor mit der ID ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ab.</span><span class="sxs-lookup"><span data-stu-id="a5065-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="a5065-118">Beispiel 4: Verwenden der Instanzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a5065-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a5065-119">Dieser Befehl ruft den Schlüssel des Schlüsseltresor mit der ID ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ab.</span><span class="sxs-lookup"><span data-stu-id="a5065-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="a5065-120">Beispiel 5: Verwenden der Pipette</span><span class="sxs-lookup"><span data-stu-id="a5065-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="a5065-121">Dieser Befehl ruft den Schlüssel des Schlüsseltresor mit der ID ' ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ab.</span><span class="sxs-lookup"><span data-stu-id="a5065-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="a5065-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5065-122">PARAMETERS</span></span>

### <span data-ttu-id="a5065-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5065-123">-DefaultProfile</span></span>
<span data-ttu-id="a5065-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5065-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5065-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="a5065-125">-Instance</span></span>
<span data-ttu-id="a5065-126">Das Instanzeingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="a5065-126">The instance input object</span></span>

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

### <span data-ttu-id="a5065-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a5065-127">-InstanceName</span></span>
<span data-ttu-id="a5065-128">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="a5065-128">The instance name</span></span>

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

### <span data-ttu-id="a5065-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="a5065-129">-InstanceResourceId</span></span>
<span data-ttu-id="a5065-130">Die Instanzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a5065-130">The instance resource id</span></span>

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

### <span data-ttu-id="a5065-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a5065-131">-KeyId</span></span>
<span data-ttu-id="a5065-132">AzureKeyVault-Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="a5065-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5065-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5065-133">-ResourceGroupName</span></span>
<span data-ttu-id="a5065-134">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a5065-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="a5065-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5065-135">-Confirm</span></span>
<span data-ttu-id="a5065-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5065-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5065-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a5065-137">-WhatIf</span></span>
<span data-ttu-id="a5065-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5065-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5065-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5065-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5065-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5065-140">CommonParameters</span></span>
<span data-ttu-id="a5065-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5065-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5065-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5065-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5065-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5065-143">INPUTS</span></span>

### <span data-ttu-id="a5065-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a5065-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="a5065-145">System.String</span><span class="sxs-lookup"><span data-stu-id="a5065-145">System.String</span></span>

## <span data-ttu-id="a5065-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5065-146">OUTPUTS</span></span>

### <span data-ttu-id="a5065-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="a5065-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="a5065-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a5065-148">NOTES</span></span>

## <span data-ttu-id="a5065-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a5065-149">RELATED LINKS</span></span>
