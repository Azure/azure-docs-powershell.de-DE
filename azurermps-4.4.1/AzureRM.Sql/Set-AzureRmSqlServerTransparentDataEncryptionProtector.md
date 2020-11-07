---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665233"
---
# <span data-ttu-id="7f9a2-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7f9a2-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="7f9a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9a2-103">Legt die transparente Daten Verschlüsselungs-Beschützer für einen SQL Server fest.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f9a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f9a2-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f9a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f9a2-105">DESCRIPTION</span></span>
<span data-ttu-id="7f9a2-106">Das Set-AzureRmSqlServerTransparentDataEncryptionProtector-Cmdlet legt die DSA-Beschützer für einen SQL Server fest.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="7f9a2-107">Durch Ändern des DSA-Protector-Typs wird der Protector gedreht.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="7f9a2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f9a2-108">EXAMPLES</span></span>

### <span data-ttu-id="7f9a2-109">--------------------------Beispiel 1: setzen Sie den Typ der transparenten Datenverschlüsselung (DSA) auf ServiceManaged--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f9a2-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="7f9a2-110">Dieser Befehl aktualisiert den Typ des DSA-Beschützers des Servers auf Dienst verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="7f9a2-111">ResourceGroupName Servername Typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="7f9a2-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="7f9a2-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="7f9a2-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="7f9a2-113">--------------------------Beispiel 2: setzen Sie den transparenten Daten Verschlüsselungs Protector-Typ auf Azure Key Vault--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f9a2-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="7f9a2-114">Mit diesem Befehl wird ein Server aktualisiert, um den Serverschlüssel Vault-Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' als DSA-Beschützer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="7f9a2-115">ResourceGroupName Servername Typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="7f9a2-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="7f9a2-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="7f9a2-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="7f9a2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f9a2-117">PARAMETERS</span></span>

### <span data-ttu-id="7f9a2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7f9a2-118">-Force</span></span>
<span data-ttu-id="7f9a2-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="7f9a2-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7f9a2-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7f9a2-120">-KeyId</span></span>
<span data-ttu-id="7f9a2-121">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="7f9a2-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="7f9a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f9a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f9a2-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7f9a2-123">The name of the resource group</span></span>

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

### <span data-ttu-id="7f9a2-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="7f9a2-124">-ServerName</span></span>
<span data-ttu-id="7f9a2-125">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="7f9a2-126">-Typ</span><span class="sxs-lookup"><span data-stu-id="7f9a2-126">-Type</span></span>
<span data-ttu-id="7f9a2-127">Der Azure SQL-Datenbank-Typ für DSA-Schutz.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-127">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="7f9a2-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f9a2-128">-Confirm</span></span>
<span data-ttu-id="7f9a2-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f9a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f9a2-130">-WhatIf</span></span>
<span data-ttu-id="7f9a2-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f9a2-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f9a2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9a2-133">-DefaultProfile</span></span>
<span data-ttu-id="7f9a2-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9a2-135">CommonParameters</span></span>
<span data-ttu-id="7f9a2-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f9a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9a2-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f9a2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9a2-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f9a2-138">INPUTS</span></span>

### <span data-ttu-id="7f9a2-139">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="7f9a2-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="7f9a2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7f9a2-140">System.String</span></span>

## <span data-ttu-id="7f9a2-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f9a2-141">OUTPUTS</span></span>

### <span data-ttu-id="7f9a2-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="7f9a2-142">System.Object</span></span>

## <span data-ttu-id="7f9a2-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f9a2-143">NOTES</span></span>

## <span data-ttu-id="7f9a2-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f9a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="7f9a2-145">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7f9a2-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
