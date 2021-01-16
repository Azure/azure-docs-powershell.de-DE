---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 696f7bd0334039691301f8a4399362b9383ab2db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289589"
---
# <span data-ttu-id="ffb03-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ffb03-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="ffb03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb03-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb03-103">Entfernt einen Schlüssel im Tresor von einem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ffb03-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="ffb03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffb03-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffb03-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffb03-105">DESCRIPTION</span></span>
<span data-ttu-id="ffb03-106">Das Remove-AzSqlServerKeyVaultKey cmdlet entfernt den Schlüssel des Tresorschlüssels vom angegebenen SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ffb03-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="ffb03-107">Beachten Sie, SQL die Berechtigungen des Servers für den Tresor des Schlüssels nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ffb03-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="ffb03-108">Verwenden Sie Set-AzKeyVaultAccessPolicy, um Berechtigungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ffb03-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="ffb03-109">Beachten Sie, dass dieses Cmdlet keine Änderungen am Schlüsseltresor vor nimmt.</span><span class="sxs-lookup"><span data-stu-id="ffb03-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="ffb03-110">Verwenden Sie "Remove-AzKeyVaultKey", um einen Schlüssel aus dem Schlüsseltresor zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ffb03-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="ffb03-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffb03-111">EXAMPLES</span></span>

### <span data-ttu-id="ffb03-112">Beispiel 1: Entfernen eines Schlüsseltresorschlüssels</span><span class="sxs-lookup"><span data-stu-id="ffb03-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ffb03-113">Mit diesem Befehl wird der Schlüssel "Schlüssel im Tresor" mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 vom angegebenen Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="ffb03-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="ffb03-114">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122334455667788990011223344556677889900 CreationDate: 01.01.2017 00:00:00</span><span class="sxs-lookup"><span data-stu-id="ffb03-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="ffb03-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffb03-115">PARAMETERS</span></span>

### <span data-ttu-id="ffb03-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffb03-116">-AsJob</span></span>
<span data-ttu-id="ffb03-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ffb03-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffb03-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb03-118">-DefaultProfile</span></span>
<span data-ttu-id="ffb03-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ffb03-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffb03-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ffb03-120">-KeyId</span></span>
<span data-ttu-id="ffb03-121">Die KeyId des Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ffb03-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="ffb03-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb03-122">-ResourceGroupName</span></span>
<span data-ttu-id="ffb03-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ffb03-123">The name of the resource group</span></span>

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

### <span data-ttu-id="ffb03-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ffb03-124">-ServerName</span></span>
<span data-ttu-id="ffb03-125">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="ffb03-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="ffb03-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffb03-126">-Confirm</span></span>
<span data-ttu-id="ffb03-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffb03-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb03-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ffb03-128">-WhatIf</span></span>
<span data-ttu-id="ffb03-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffb03-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb03-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffb03-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb03-131">CommonParameters</span></span>
<span data-ttu-id="ffb03-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb03-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffb03-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb03-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffb03-134">INPUTS</span></span>

### <span data-ttu-id="ffb03-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ffb03-135">System.String</span></span>

## <span data-ttu-id="ffb03-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffb03-136">OUTPUTS</span></span>

### <span data-ttu-id="ffb03-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="ffb03-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="ffb03-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ffb03-138">NOTES</span></span>

## <span data-ttu-id="ffb03-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ffb03-139">RELATED LINKS</span></span>

[<span data-ttu-id="ffb03-140">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="ffb03-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
