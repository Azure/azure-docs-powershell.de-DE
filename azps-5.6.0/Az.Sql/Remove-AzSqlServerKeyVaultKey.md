---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 5b394909df0469c37a0217b3eb861ce4a1146e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926288"
---
# <span data-ttu-id="100ec-101">Remove-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="100ec-101">Remove-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="100ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="100ec-102">SYNOPSIS</span></span>
<span data-ttu-id="100ec-103">Entfernt einen Schlüsseltresorschlüssel von einem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="100ec-103">Removes a Key Vault key from a SQL server.</span></span>

## <span data-ttu-id="100ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="100ec-104">SYNTAX</span></span>

```
Remove-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="100ec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="100ec-105">DESCRIPTION</span></span>
<span data-ttu-id="100ec-106">Das Remove-AzSqlServerKeyVaultKey cmdlet entfernt den Schlüsseltresorschlüssel aus dem angegebenen SQL Server.</span><span class="sxs-lookup"><span data-stu-id="100ec-106">The Remove-AzSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="100ec-107">Beachten Sie, SQL die Berechtigungen des Schlüsselservers für den Tresor des Schlüssels nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="100ec-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="100ec-108">Zum Ändern von Berechtigungen verwenden Sie Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="100ec-108">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="100ec-109">Beachten Sie, dass dieses Cmdlet keine Änderungen am Schlüsseltresor vor nimmt.</span><span class="sxs-lookup"><span data-stu-id="100ec-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="100ec-110">Wenn Sie einen Schlüssel aus dem Schlüsseltresor entfernen möchten, verwenden Sie Remove-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="100ec-110">To remove a key from Key Vault, use Remove-AzKeyVaultKey.</span></span>

## <span data-ttu-id="100ec-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="100ec-111">EXAMPLES</span></span>

### <span data-ttu-id="100ec-112">Beispiel 1: Entfernen eines Schlüsseltresorschlüssels</span><span class="sxs-lookup"><span data-stu-id="100ec-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="100ec-113">Mit diesem Befehl wird der Schlüsseltresorschlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' vom angegebenen Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="100ec-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="100ec-114">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445667789900111223345567789900 CreationDate : 01.01.2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="100ec-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="100ec-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="100ec-115">PARAMETERS</span></span>

### <span data-ttu-id="100ec-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="100ec-116">-AsJob</span></span>
<span data-ttu-id="100ec-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="100ec-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="100ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100ec-118">-DefaultProfile</span></span>
<span data-ttu-id="100ec-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="100ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="100ec-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="100ec-120">-KeyId</span></span>
<span data-ttu-id="100ec-121">Die Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="100ec-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="100ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="100ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="100ec-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="100ec-123">The name of the resource group</span></span>

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

### <span data-ttu-id="100ec-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="100ec-124">-ServerName</span></span>
<span data-ttu-id="100ec-125">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="100ec-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="100ec-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="100ec-126">-Confirm</span></span>
<span data-ttu-id="100ec-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="100ec-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="100ec-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="100ec-128">-WhatIf</span></span>
<span data-ttu-id="100ec-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="100ec-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="100ec-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="100ec-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="100ec-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100ec-131">CommonParameters</span></span>
<span data-ttu-id="100ec-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="100ec-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100ec-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="100ec-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100ec-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="100ec-134">INPUTS</span></span>

### <span data-ttu-id="100ec-135">System.String</span><span class="sxs-lookup"><span data-stu-id="100ec-135">System.String</span></span>

## <span data-ttu-id="100ec-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="100ec-136">OUTPUTS</span></span>

### <span data-ttu-id="100ec-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="100ec-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="100ec-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="100ec-138">NOTES</span></span>

## <span data-ttu-id="100ec-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="100ec-139">RELATED LINKS</span></span>

[<span data-ttu-id="100ec-140">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="100ec-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
