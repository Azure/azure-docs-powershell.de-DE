---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504713"
---
# <span data-ttu-id="1d202-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d202-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="1d202-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d202-102">SYNOPSIS</span></span>
<span data-ttu-id="1d202-103">Fügt einen schlüsseltresor-Schlüssel zu einem SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d202-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d202-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d202-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d202-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d202-105">DESCRIPTION</span></span>
<span data-ttu-id="1d202-106">Das Add-AzureRmSqlServerKeyVaultKey-Cmdlet fügt dem bereitgestellten SQL Server einen schlüsseltresor Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d202-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="1d202-107">Der Server muss über die Berechtigungen "Get, wrapKey, unwrapKey" für den Tresor verfügen.</span><span class="sxs-lookup"><span data-stu-id="1d202-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="1d202-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d202-108">EXAMPLES</span></span>

### <span data-ttu-id="1d202-109">--------------------------Beispiel 1: Hinzufügen von Key Vault-Schlüssel--------------------------</span><span class="sxs-lookup"><span data-stu-id="1d202-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="1d202-110">Dieser Befehl fügt dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 SQL Server mit dem Namen "ContosoServer" in der Ressourcengruppe "ContosoResourceGroup" den schlüsseltresor mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="1d202-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="1d202-111">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="1d202-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="1d202-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d202-112">PARAMETERS</span></span>

### <span data-ttu-id="1d202-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="1d202-113">-KeyId</span></span>
<span data-ttu-id="1d202-114">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="1d202-114">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="1d202-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d202-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d202-116">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1d202-116">The name of the resource group</span></span>

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

### <span data-ttu-id="1d202-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="1d202-117">-ServerName</span></span>
<span data-ttu-id="1d202-118">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="1d202-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1d202-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d202-119">-Confirm</span></span>
<span data-ttu-id="1d202-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d202-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d202-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d202-121">-WhatIf</span></span>
<span data-ttu-id="1d202-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d202-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d202-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d202-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d202-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d202-124">-DefaultProfile</span></span>
<span data-ttu-id="1d202-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d202-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d202-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d202-126">CommonParameters</span></span>
<span data-ttu-id="1d202-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d202-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d202-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d202-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d202-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d202-129">INPUTS</span></span>

### <span data-ttu-id="1d202-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1d202-130">System.String</span></span>

## <span data-ttu-id="1d202-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d202-131">OUTPUTS</span></span>

### <span data-ttu-id="1d202-132">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="1d202-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="1d202-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d202-133">NOTES</span></span>

## <span data-ttu-id="1d202-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d202-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d202-135">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1d202-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
