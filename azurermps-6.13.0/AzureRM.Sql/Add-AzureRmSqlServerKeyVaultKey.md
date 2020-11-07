---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 96f6f6a2697117099a6710acec5be8018e492c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664320"
---
# <span data-ttu-id="41d01-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="41d01-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="41d01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41d01-102">SYNOPSIS</span></span>
<span data-ttu-id="41d01-103">Fügt einen schlüsseltresor-Schlüssel zu einem SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="41d01-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41d01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41d01-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d01-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41d01-105">DESCRIPTION</span></span>
<span data-ttu-id="41d01-106">Das Add-AzureRmSqlServerKeyVaultKey-Cmdlet fügt dem bereitgestellten SQL Server einen schlüsseltresor Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="41d01-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="41d01-107">Der Server muss über die Berechtigungen "Get, wrapKey, unwrapKey" für den Tresor verfügen.</span><span class="sxs-lookup"><span data-stu-id="41d01-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="41d01-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41d01-108">EXAMPLES</span></span>

### <span data-ttu-id="41d01-109">Beispiel 1: Hinzufügen von Key Vault-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="41d01-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="41d01-110">Dieser Befehl fügt dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 SQL Server mit dem Namen "ContosoServer" in der Ressourcengruppe "ContosoResourceGroup" den schlüsseltresor mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="41d01-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="41d01-111">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="41d01-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="41d01-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="41d01-112">PARAMETERS</span></span>

### <span data-ttu-id="41d01-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41d01-113">-AsJob</span></span>
<span data-ttu-id="41d01-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="41d01-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41d01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d01-115">-DefaultProfile</span></span>
<span data-ttu-id="41d01-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="41d01-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41d01-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="41d01-117">-KeyId</span></span>
<span data-ttu-id="41d01-118">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="41d01-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d01-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d01-119">-ResourceGroupName</span></span>
<span data-ttu-id="41d01-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="41d01-120">The name of the resource group</span></span>

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

### <span data-ttu-id="41d01-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="41d01-121">-ServerName</span></span>
<span data-ttu-id="41d01-122">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="41d01-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="41d01-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41d01-123">-Confirm</span></span>
<span data-ttu-id="41d01-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41d01-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d01-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d01-125">-WhatIf</span></span>
<span data-ttu-id="41d01-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41d01-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d01-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41d01-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d01-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d01-128">CommonParameters</span></span>
<span data-ttu-id="41d01-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d01-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d01-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d01-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d01-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41d01-131">INPUTS</span></span>

### <span data-ttu-id="41d01-132">System. String</span><span class="sxs-lookup"><span data-stu-id="41d01-132">System.String</span></span>

## <span data-ttu-id="41d01-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41d01-133">OUTPUTS</span></span>

### <span data-ttu-id="41d01-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="41d01-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="41d01-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="41d01-135">NOTES</span></span>

## <span data-ttu-id="41d01-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41d01-136">RELATED LINKS</span></span>

[<span data-ttu-id="41d01-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="41d01-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
