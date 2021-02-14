---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163169"
---
# <span data-ttu-id="3d8e7-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3d8e7-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="3d8e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8e7-103">Legt die transparente Datenverschlüsselung (Transparent Data Encryption, TDE) für eine verwaltete SQL fest.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="3d8e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d8e7-104">SYNTAX</span></span>

### <span data-ttu-id="3d8e7-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d8e7-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8e7-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d8e7-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d8e7-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d8e7-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d8e7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d8e7-108">DESCRIPTION</span></span>
<span data-ttu-id="3d8e7-109">Das Set-AzSqlInstanceTransparentDataEncryptionProtector-Cmdlet legt das TDE-Wert für eine verwaltete SQL fest.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="3d8e7-110">Wenn Sie den Typ des TDE-Typs ändern, dreht sich das Bild.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="3d8e7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d8e7-111">EXAMPLES</span></span>

### <span data-ttu-id="3d8e7-112">Beispiel 1: Festlegen des Datentyps "Transparent Data Encryption (TDE)" auf "ServiceManaged"</span><span class="sxs-lookup"><span data-stu-id="3d8e7-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="3d8e7-113">Mit diesem Befehl wird der TdE-Datentyp einer verwalteten Instanz auf "Dienst verwaltet" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="3d8e7-114">Beispiel 2: Festlegen des Datentyps "Transparente Datenverschlüsselung" auf den Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="3d8e7-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="3d8e7-115">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüssel des verwalteten Instanzschlüsseltresor mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als TDE-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="3d8e7-116">Beispiel 3: Festlegen des Datentyps "Transparente Datenverschlüsselung" auf Azure Key Vault mithilfe eines verwalteten Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="3d8e7-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="3d8e7-117">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüssel des verwalteten Instanzschlüsseltresor mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als TDE-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="3d8e7-118">Beispiel 4: Festlegen des Datentyps "Transparente Datenverschlüsselung" auf Azure Key Vault mithilfe der Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3d8e7-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="3d8e7-119">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüssel des verwalteten Instanzschlüsseltresor mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als TDE-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="3d8e7-120">Beispiel 5: Festlegen des Datentyps "Transparente Datenverschlüsselung" auf Azure Key Vault mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="3d8e7-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="3d8e7-121">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüssel des verwalteten Instanzschlüsseltresor mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als TDE-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="3d8e7-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d8e7-122">PARAMETERS</span></span>

### <span data-ttu-id="3d8e7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8e7-123">-DefaultProfile</span></span>
<span data-ttu-id="3d8e7-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d8e7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3d8e7-125">-Force</span></span>
<span data-ttu-id="3d8e7-126">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="3d8e7-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3d8e7-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="3d8e7-127">-Instance</span></span>
<span data-ttu-id="3d8e7-128">Das Instanzeingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="3d8e7-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8e7-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3d8e7-129">-InstanceName</span></span>
<span data-ttu-id="3d8e7-130">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="3d8e7-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8e7-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="3d8e7-131">-InstanceResourceId</span></span>
<span data-ttu-id="3d8e7-132">Die Instanzressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="3d8e7-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d8e7-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="3d8e7-133">-KeyId</span></span>
<span data-ttu-id="3d8e7-134">Die KeyId des Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8e7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8e7-135">-ResourceGroupName</span></span>
<span data-ttu-id="3d8e7-136">Der Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3d8e7-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8e7-137">-Type</span><span class="sxs-lookup"><span data-stu-id="3d8e7-137">-Type</span></span>
<span data-ttu-id="3d8e7-138">Der Typ "Azure Sql-Datenbanktransparente Datenverschlüsselung".</span><span class="sxs-lookup"><span data-stu-id="3d8e7-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d8e7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d8e7-139">-Confirm</span></span>
<span data-ttu-id="3d8e7-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8e7-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3d8e7-141">-WhatIf</span></span>
<span data-ttu-id="3d8e7-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8e7-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8e7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8e7-144">CommonParameters</span></span>
<span data-ttu-id="3d8e7-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d8e7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8e7-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d8e7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8e7-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d8e7-147">INPUTS</span></span>

### <span data-ttu-id="3d8e7-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3d8e7-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="3d8e7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3d8e7-149">System.String</span></span>

## <span data-ttu-id="3d8e7-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d8e7-150">OUTPUTS</span></span>

### <span data-ttu-id="3d8e7-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="3d8e7-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="3d8e7-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3d8e7-152">NOTES</span></span>

## <span data-ttu-id="3d8e7-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3d8e7-153">RELATED LINKS</span></span>
