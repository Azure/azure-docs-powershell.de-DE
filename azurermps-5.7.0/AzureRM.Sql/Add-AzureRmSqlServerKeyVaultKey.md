---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: bf82ca7804ecd3f382728217395be234155e9035
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482702"
---
# <span data-ttu-id="ba9c7-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ba9c7-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="ba9c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ba9c7-103">Fügt einen schlüsseltresor-Schlüssel zu einem SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba9c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba9c7-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba9c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba9c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ba9c7-106">Das Add-AzureRmSqlServerKeyVaultKey-Cmdlet fügt dem bereitgestellten SQL Server einen schlüsseltresor Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="ba9c7-107">Der Server muss über die Berechtigungen "Get, wrapKey, unwrapKey" für den Tresor verfügen.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="ba9c7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba9c7-108">EXAMPLES</span></span>

### <span data-ttu-id="ba9c7-109">Beispiel 1: Hinzufügen von Key Vault-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="ba9c7-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ba9c7-110">Dieser Befehl fügt dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 SQL Server mit dem Namen "ContosoServer" in der Ressourcengruppe "ContosoResourceGroup" den schlüsseltresor mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="ba9c7-111">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="ba9c7-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="ba9c7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba9c7-112">PARAMETERS</span></span>

### <span data-ttu-id="ba9c7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba9c7-113">-AsJob</span></span>
<span data-ttu-id="ba9c7-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ba9c7-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba9c7-115">-DefaultProfile</span></span>
<span data-ttu-id="ba9c7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ba9c7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c7-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ba9c7-117">-KeyId</span></span>
<span data-ttu-id="ba9c7-118">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="ba9c7-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba9c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba9c7-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ba9c7-120">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c7-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="ba9c7-121">-ServerName</span></span>
<span data-ttu-id="ba9c7-122">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-122">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c7-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba9c7-123">-Confirm</span></span>
<span data-ttu-id="ba9c7-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba9c7-125">-WhatIf</span></span>
<span data-ttu-id="ba9c7-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba9c7-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba9c7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba9c7-128">CommonParameters</span></span>
<span data-ttu-id="ba9c7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba9c7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba9c7-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba9c7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba9c7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba9c7-131">INPUTS</span></span>

### <span data-ttu-id="ba9c7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba9c7-132">System.String</span></span>

## <span data-ttu-id="ba9c7-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba9c7-133">OUTPUTS</span></span>

### <span data-ttu-id="ba9c7-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="ba9c7-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="ba9c7-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba9c7-135">NOTES</span></span>

## <span data-ttu-id="ba9c7-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba9c7-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba9c7-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ba9c7-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
