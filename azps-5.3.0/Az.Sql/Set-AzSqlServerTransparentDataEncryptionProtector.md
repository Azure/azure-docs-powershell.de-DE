---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458360"
---
# <span data-ttu-id="b3e9e-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b3e9e-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="b3e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e9e-103">Legt die transparente Datenverschlüsselung (Transparent Data Encryption, TDE) für einen SQL fest.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="b3e9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3e9e-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e9e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e9e-106">Das Set-AzSqlServerTransparentDataEncryptionProtector-Cmdlet legt das TDE-Wert für einen SQL fest.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="b3e9e-107">Wenn Sie den Typ des TDE-Typs ändern, dreht sich das Bild.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="b3e9e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3e9e-108">EXAMPLES</span></span>

### <span data-ttu-id="b3e9e-109">Beispiel 1: Festlegen des Datentyps "Transparent Data Encryption (TDE)" auf "ServiceManaged"</span><span class="sxs-lookup"><span data-stu-id="b3e9e-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="b3e9e-110">Mit diesem Befehl wird der TdE-Datentyp eines Servers auf "Dienst verwaltet" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="b3e9e-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="b3e9e-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="b3e9e-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="b3e9e-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="b3e9e-113">Beispiel 2: Festlegen des Datentyps "Transparente Datenverschlüsselung" auf den Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="b3e9e-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="b3e9e-114">Mit diesem Befehl wird ein Server so aktualisiert, dass der Serverschlüsseltresorschlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als TDE-Ereignis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="b3e9e-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="b3e9e-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="b3e9e-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="b3e9e-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="b3e9e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3e9e-117">PARAMETERS</span></span>

### <span data-ttu-id="b3e9e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3e9e-118">-AsJob</span></span>
<span data-ttu-id="b3e9e-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b3e9e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3e9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e9e-120">-DefaultProfile</span></span>
<span data-ttu-id="b3e9e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b3e9e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3e9e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b3e9e-122">-Force</span></span>
<span data-ttu-id="b3e9e-123">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="b3e9e-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b3e9e-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b3e9e-124">-KeyId</span></span>
<span data-ttu-id="b3e9e-125">Die KeyId des Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e9e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e9e-126">-ResourceGroupName</span></span>
<span data-ttu-id="b3e9e-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b3e9e-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e9e-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3e9e-128">-ServerName</span></span>
<span data-ttu-id="b3e9e-129">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e9e-130">-Type</span><span class="sxs-lookup"><span data-stu-id="b3e9e-130">-Type</span></span>
<span data-ttu-id="b3e9e-131">Der Azure Sql-Datenbank-TDE-Typ.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e9e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3e9e-132">-Confirm</span></span>
<span data-ttu-id="b3e9e-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e9e-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b3e9e-134">-WhatIf</span></span>
<span data-ttu-id="b3e9e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e9e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e9e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e9e-137">CommonParameters</span></span>
<span data-ttu-id="b3e9e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e9e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e9e-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3e9e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e9e-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3e9e-140">INPUTS</span></span>

### <span data-ttu-id="b3e9e-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="b3e9e-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="b3e9e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b3e9e-142">System.String</span></span>

## <span data-ttu-id="b3e9e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3e9e-143">OUTPUTS</span></span>

### <span data-ttu-id="b3e9e-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="b3e9e-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="b3e9e-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3e9e-145">NOTES</span></span>

## <span data-ttu-id="b3e9e-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3e9e-146">RELATED LINKS</span></span>

[<span data-ttu-id="b3e9e-147">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="b3e9e-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
