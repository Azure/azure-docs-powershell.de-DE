---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: dcb099a26fe46325b1c3869b5e507347c948f09f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659032"
---
# <span data-ttu-id="77e8e-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="77e8e-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="77e8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="77e8e-103">Entfernt einen Key Vault-Schlüssel aus einem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77e8e-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="77e8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77e8e-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77e8e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="77e8e-106">Das Remove-AzSqlServerKeyVaultKey-Cmdlet entfernt den schlüsseltresor Schlüssel aus dem angegebenen SQL Server.</span><span class="sxs-lookup"><span data-stu-id="77e8e-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="77e8e-107">Beachten Sie, dass die SQL Server-Berechtigungen für den Tresor des Schlüssels nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="77e8e-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="77e8e-108">Wenn Sie Berechtigungen ändern möchten, verwenden Sie die Einstellung-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="77e8e-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="77e8e-109">Beachten Sie, dass dieses Cmdlet keine Änderungen an Key Vault vornimmt.</span><span class="sxs-lookup"><span data-stu-id="77e8e-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="77e8e-110">Wenn Sie einen Schlüssel aus dem Schlüsselspeicher entfernen möchten, verwenden Sie Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="77e8e-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="77e8e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77e8e-111">EXAMPLES</span></span>

### <span data-ttu-id="77e8e-112">Beispiel 1: Entfernen eines Key Vault-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="77e8e-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="77e8e-113">Mit diesem Befehl wird der Key Vault-Schlüssel mit https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 der ID ' ' vom angegebenen Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="77e8e-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="77e8e-114">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="77e8e-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="77e8e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="77e8e-115">PARAMETERS</span></span>

### <span data-ttu-id="77e8e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77e8e-116">-AsJob</span></span>
<span data-ttu-id="77e8e-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="77e8e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77e8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e8e-118">-DefaultProfile</span></span>
<span data-ttu-id="77e8e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="77e8e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77e8e-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="77e8e-120">-KeyId</span></span>
<span data-ttu-id="77e8e-121">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="77e8e-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="77e8e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e8e-122">-ResourceGroupName</span></span>
<span data-ttu-id="77e8e-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="77e8e-123">The name of the resource group</span></span>

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

### <span data-ttu-id="77e8e-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="77e8e-124">-ServerName</span></span>
<span data-ttu-id="77e8e-125">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="77e8e-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="77e8e-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77e8e-126">-Confirm</span></span>
<span data-ttu-id="77e8e-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77e8e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e8e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e8e-128">-WhatIf</span></span>
<span data-ttu-id="77e8e-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77e8e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77e8e-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77e8e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e8e-131">CommonParameters</span></span>
<span data-ttu-id="77e8e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e8e-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77e8e-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e8e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77e8e-134">INPUTS</span></span>

### <span data-ttu-id="77e8e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="77e8e-135">System.String</span></span>

## <span data-ttu-id="77e8e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77e8e-136">OUTPUTS</span></span>

### <span data-ttu-id="77e8e-137">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="77e8e-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="77e8e-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="77e8e-138">NOTES</span></span>

## <span data-ttu-id="77e8e-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77e8e-139">RELATED LINKS</span></span>

[<span data-ttu-id="77e8e-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="77e8e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
