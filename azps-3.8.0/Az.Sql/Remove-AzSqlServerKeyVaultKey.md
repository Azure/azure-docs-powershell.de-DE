---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003376"
---
# <span data-ttu-id="3eaff-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3eaff-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="3eaff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3eaff-102">SYNOPSIS</span></span>
<span data-ttu-id="3eaff-103">Entfernt einen Key Vault-Schlüssel aus einem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3eaff-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="3eaff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3eaff-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eaff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3eaff-105">DESCRIPTION</span></span>
<span data-ttu-id="3eaff-106">Das Remove-AzSqlServerKeyVaultKey-Cmdlet entfernt den schlüsseltresor Schlüssel aus dem angegebenen SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3eaff-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="3eaff-107">Beachten Sie, dass die SQL Server-Berechtigungen für den Tresor des Schlüssels nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3eaff-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="3eaff-108">Wenn Sie Berechtigungen ändern möchten, verwenden Sie die Einstellung-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="3eaff-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="3eaff-109">Beachten Sie, dass dieses Cmdlet keine Änderungen an Key Vault vornimmt.</span><span class="sxs-lookup"><span data-stu-id="3eaff-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="3eaff-110">Wenn Sie einen Schlüssel aus dem Schlüsselspeicher entfernen möchten, verwenden Sie Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="3eaff-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="3eaff-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3eaff-111">EXAMPLES</span></span>

### <span data-ttu-id="3eaff-112">Beispiel 1: Entfernen eines Key Vault-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3eaff-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="3eaff-113">Mit diesem Befehl wird der Key Vault-Schlüssel mit https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 der ID ' ' vom angegebenen Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="3eaff-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="3eaff-114">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="3eaff-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="3eaff-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3eaff-115">PARAMETERS</span></span>

### <span data-ttu-id="3eaff-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eaff-116">-AsJob</span></span>
<span data-ttu-id="3eaff-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3eaff-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eaff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eaff-118">-DefaultProfile</span></span>
<span data-ttu-id="3eaff-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3eaff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eaff-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="3eaff-120">-KeyId</span></span>
<span data-ttu-id="3eaff-121">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="3eaff-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="3eaff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eaff-122">-ResourceGroupName</span></span>
<span data-ttu-id="3eaff-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3eaff-123">The name of the resource group</span></span>

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

### <span data-ttu-id="3eaff-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="3eaff-124">-ServerName</span></span>
<span data-ttu-id="3eaff-125">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="3eaff-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3eaff-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3eaff-126">-Confirm</span></span>
<span data-ttu-id="3eaff-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3eaff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eaff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eaff-128">-WhatIf</span></span>
<span data-ttu-id="3eaff-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eaff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eaff-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3eaff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eaff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eaff-131">CommonParameters</span></span>
<span data-ttu-id="3eaff-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eaff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eaff-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3eaff-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eaff-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3eaff-134">INPUTS</span></span>

### <span data-ttu-id="3eaff-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3eaff-135">System.String</span></span>

## <span data-ttu-id="3eaff-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3eaff-136">OUTPUTS</span></span>

### <span data-ttu-id="3eaff-137">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="3eaff-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="3eaff-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="3eaff-138">NOTES</span></span>

## <span data-ttu-id="3eaff-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3eaff-139">RELATED LINKS</span></span>

[<span data-ttu-id="3eaff-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="3eaff-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
