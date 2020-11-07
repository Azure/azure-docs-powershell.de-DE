---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 0321fc68c22e3bea973c25f9bbb27e0c5736e944
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825723"
---
# <span data-ttu-id="aa772-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="aa772-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="aa772-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa772-102">SYNOPSIS</span></span>
<span data-ttu-id="aa772-103">Legt die transparente Daten Verschlüsselungs-Beschützer für eine verwaltete SQL-Instanz fest.</span><span class="sxs-lookup"><span data-stu-id="aa772-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="aa772-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa772-104">SYNTAX</span></span>

### <span data-ttu-id="aa772-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa772-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa772-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa772-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa772-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa772-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa772-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa772-108">DESCRIPTION</span></span>
<span data-ttu-id="aa772-109">Das Set-AzSqlInstanceTransparentDataEncryptionProtector-Cmdlet legt die DSA-Beschützer für eine verwaltete SQL-Instanz fest.</span><span class="sxs-lookup"><span data-stu-id="aa772-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="aa772-110">Durch Ändern des DSA-Protector-Typs wird der Protector gedreht.</span><span class="sxs-lookup"><span data-stu-id="aa772-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="aa772-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa772-111">EXAMPLES</span></span>

### <span data-ttu-id="aa772-112">Beispiel 1: Einrichten des DSA-Protector-Typs (transparent Data Encryption) auf ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="aa772-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="aa772-113">Dieser Befehl aktualisiert den Typ des DSA-Beschützers einer verwalteten Instanz in Dienst verwaltet.</span><span class="sxs-lookup"><span data-stu-id="aa772-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="aa772-114">Beispiel 2: Einrichten des transparenten Daten Verschlüsselungsschutz-Typs auf Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="aa772-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="aa772-115">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüsselspeicher Schlüssel der verwalteten Instanz mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als DSA-Beschützer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa772-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="aa772-116">Beispiel 3: Einrichten des transparenten Daten Verschlüsselungsschutz-Typs auf Azure Key Vault mithilfe eines verwalteten Instanzen Objekts</span><span class="sxs-lookup"><span data-stu-id="aa772-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="aa772-117">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüsselspeicher Schlüssel der verwalteten Instanz mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als DSA-Beschützer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa772-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="aa772-118">Beispiel 4: Einrichten des transparenten Daten Verschlüsselungs Protector-Typs auf Azure Key Vault mithilfe der Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="aa772-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="aa772-119">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüsselspeicher Schlüssel der verwalteten Instanz mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als DSA-Beschützer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa772-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="aa772-120">Beispiel 5: Einrichten des transparenten Daten Verschlüsselungsschutz-Typs auf Azure Key Vault mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="aa772-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="aa772-121">Mit diesem Befehl wird die angegebene verwaltete Instanz so aktualisiert, dass der Schlüsselspeicher Schlüssel der verwalteten Instanz mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als DSA-Beschützer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa772-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="aa772-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa772-122">PARAMETERS</span></span>

### <span data-ttu-id="aa772-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa772-123">-DefaultProfile</span></span>
<span data-ttu-id="aa772-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa772-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa772-125">-Force</span><span class="sxs-lookup"><span data-stu-id="aa772-125">-Force</span></span>
<span data-ttu-id="aa772-126">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="aa772-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aa772-127">-Instanz</span><span class="sxs-lookup"><span data-stu-id="aa772-127">-Instance</span></span>
<span data-ttu-id="aa772-128">Das Instanzen Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="aa772-128">The instance input object</span></span>

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

### <span data-ttu-id="aa772-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="aa772-129">-InstanceName</span></span>
<span data-ttu-id="aa772-130">Der Instanzname</span><span class="sxs-lookup"><span data-stu-id="aa772-130">The instance name</span></span>

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

### <span data-ttu-id="aa772-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="aa772-131">-InstanceResourceId</span></span>
<span data-ttu-id="aa772-132">Die Ressourcen-ID der Instanz</span><span class="sxs-lookup"><span data-stu-id="aa772-132">The instance resource id</span></span>

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

### <span data-ttu-id="aa772-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="aa772-133">-KeyId</span></span>
<span data-ttu-id="aa772-134">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="aa772-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="aa772-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa772-135">-ResourceGroupName</span></span>
<span data-ttu-id="aa772-136">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aa772-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="aa772-137">-Typ</span><span class="sxs-lookup"><span data-stu-id="aa772-137">-Type</span></span>
<span data-ttu-id="aa772-138">Der Azure SQL-Datenbank-Daten Verschlüsselungsschutz-Typ</span><span class="sxs-lookup"><span data-stu-id="aa772-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="aa772-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa772-139">-Confirm</span></span>
<span data-ttu-id="aa772-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa772-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa772-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa772-141">-WhatIf</span></span>
<span data-ttu-id="aa772-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa772-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa772-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa772-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa772-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa772-144">CommonParameters</span></span>
<span data-ttu-id="aa772-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa772-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa772-146">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa772-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa772-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa772-147">INPUTS</span></span>

### <span data-ttu-id="aa772-148">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="aa772-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="aa772-149">System. String</span><span class="sxs-lookup"><span data-stu-id="aa772-149">System.String</span></span>

## <span data-ttu-id="aa772-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa772-150">OUTPUTS</span></span>

### <span data-ttu-id="aa772-151">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="aa772-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="aa772-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa772-152">NOTES</span></span>

## <span data-ttu-id="aa772-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa772-153">RELATED LINKS</span></span>
