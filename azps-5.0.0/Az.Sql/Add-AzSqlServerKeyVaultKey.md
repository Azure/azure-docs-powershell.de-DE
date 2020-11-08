---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175411"
---
# <span data-ttu-id="c0c1e-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c0c1e-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="c0c1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c1e-103">Fügt einen schlüsseltresor-Schlüssel zu einem SQL Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="c0c1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0c1e-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0c1e-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c1e-106">Das Add-AzSqlServerKeyVaultKey-Cmdlet fügt dem bereitgestellten SQL Server einen schlüsseltresor Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="c0c1e-107">Der Server muss über die Berechtigungen "Get, wrapKey, unwrapKey" für den Tresor verfügen.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="c0c1e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0c1e-108">EXAMPLES</span></span>

### <span data-ttu-id="c0c1e-109">Beispiel 1: Hinzufügen von Key Vault-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="c0c1e-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="c0c1e-110">Dieser Befehl fügt dem https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 SQL Server mit dem Namen "ContosoServer" in der Ressourcengruppe "ContosoResourceGroup" den schlüsseltresor mit der ID "" hinzu.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="c0c1e-111">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="c0c1e-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="c0c1e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0c1e-112">PARAMETERS</span></span>

### <span data-ttu-id="c0c1e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0c1e-113">-AsJob</span></span>
<span data-ttu-id="c0c1e-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c0c1e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0c1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c1e-115">-DefaultProfile</span></span>
<span data-ttu-id="c0c1e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c0c1e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0c1e-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c0c1e-117">-KeyId</span></span>
<span data-ttu-id="c0c1e-118">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="c0c1e-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="c0c1e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c1e-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0c1e-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c0c1e-120">The name of the resource group</span></span>

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

### <span data-ttu-id="c0c1e-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="c0c1e-121">-ServerName</span></span>
<span data-ttu-id="c0c1e-122">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c0c1e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0c1e-123">-Confirm</span></span>
<span data-ttu-id="c0c1e-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c1e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c1e-125">-WhatIf</span></span>
<span data-ttu-id="c0c1e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c1e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c1e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c1e-128">CommonParameters</span></span>
<span data-ttu-id="c0c1e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c1e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c1e-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0c1e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c1e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0c1e-131">INPUTS</span></span>

### <span data-ttu-id="c0c1e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c0c1e-132">System.String</span></span>

## <span data-ttu-id="c0c1e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0c1e-133">OUTPUTS</span></span>

### <span data-ttu-id="c0c1e-134">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="c0c1e-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="c0c1e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0c1e-135">NOTES</span></span>

## <span data-ttu-id="c0c1e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0c1e-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0c1e-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c0c1e-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
