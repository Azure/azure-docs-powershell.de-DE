---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174059"
---
# <span data-ttu-id="aed5c-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="aed5c-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="aed5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aed5c-102">SYNOPSIS</span></span>
<span data-ttu-id="aed5c-103">Legt die transparente Daten Verschlüsselungs-Beschützer für einen SQL Server fest.</span><span class="sxs-lookup"><span data-stu-id="aed5c-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="aed5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aed5c-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aed5c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aed5c-105">DESCRIPTION</span></span>
<span data-ttu-id="aed5c-106">Das Set-AzSqlServerTransparentDataEncryptionProtector-Cmdlet legt die DSA-Beschützer für einen SQL Server fest.</span><span class="sxs-lookup"><span data-stu-id="aed5c-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="aed5c-107">Durch Ändern des DSA-Protector-Typs wird der Protector gedreht.</span><span class="sxs-lookup"><span data-stu-id="aed5c-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="aed5c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aed5c-108">EXAMPLES</span></span>

### <span data-ttu-id="aed5c-109">Beispiel 1: Einrichten des DSA-Protector-Typs (transparent Data Encryption) auf ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="aed5c-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="aed5c-110">Dieser Befehl aktualisiert den Typ des DSA-Beschützers des Servers auf Dienst verwaltet.</span><span class="sxs-lookup"><span data-stu-id="aed5c-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="aed5c-111">ResourceGroupName Servername Typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="aed5c-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="aed5c-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="aed5c-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="aed5c-113">Beispiel 2: Einrichten des transparenten Daten Verschlüsselungsschutz-Typs auf Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="aed5c-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="aed5c-114">Mit diesem Befehl wird ein Server aktualisiert, um den Serverschlüssel Vault-Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als DSA-Beschützer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="aed5c-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="aed5c-115">ResourceGroupName Servername Typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="aed5c-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="aed5c-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="aed5c-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="aed5c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="aed5c-117">PARAMETERS</span></span>

### <span data-ttu-id="aed5c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aed5c-118">-AsJob</span></span>
<span data-ttu-id="aed5c-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aed5c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aed5c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed5c-120">-DefaultProfile</span></span>
<span data-ttu-id="aed5c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="aed5c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aed5c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="aed5c-122">-Force</span></span>
<span data-ttu-id="aed5c-123">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="aed5c-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aed5c-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="aed5c-124">-KeyId</span></span>
<span data-ttu-id="aed5c-125">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="aed5c-125">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="aed5c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed5c-126">-ResourceGroupName</span></span>
<span data-ttu-id="aed5c-127">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aed5c-127">The name of the resource group</span></span>

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

### <span data-ttu-id="aed5c-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="aed5c-128">-ServerName</span></span>
<span data-ttu-id="aed5c-129">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="aed5c-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="aed5c-130">-Typ</span><span class="sxs-lookup"><span data-stu-id="aed5c-130">-Type</span></span>
<span data-ttu-id="aed5c-131">Der Azure SQL-Datenbank-Typ für DSA-Schutz.</span><span class="sxs-lookup"><span data-stu-id="aed5c-131">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="aed5c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aed5c-132">-Confirm</span></span>
<span data-ttu-id="aed5c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aed5c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aed5c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aed5c-134">-WhatIf</span></span>
<span data-ttu-id="aed5c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aed5c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aed5c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aed5c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aed5c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed5c-137">CommonParameters</span></span>
<span data-ttu-id="aed5c-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed5c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed5c-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aed5c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed5c-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aed5c-140">INPUTS</span></span>

### <span data-ttu-id="aed5c-141">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="aed5c-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="aed5c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="aed5c-142">System.String</span></span>

## <span data-ttu-id="aed5c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aed5c-143">OUTPUTS</span></span>

### <span data-ttu-id="aed5c-144">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="aed5c-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="aed5c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="aed5c-145">NOTES</span></span>

## <span data-ttu-id="aed5c-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aed5c-146">RELATED LINKS</span></span>

[<span data-ttu-id="aed5c-147">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="aed5c-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
