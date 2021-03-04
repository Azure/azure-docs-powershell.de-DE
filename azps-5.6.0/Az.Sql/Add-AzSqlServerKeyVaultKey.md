---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f354fe8ad1876eb756cdf78378dbf7048e53932d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923352"
---
# <span data-ttu-id="299ac-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="299ac-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="299ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299ac-102">SYNOPSIS</span></span>
<span data-ttu-id="299ac-103">Fügt einem Server einen Schlüsseltresorschlüssel SQL hinzu.</span><span class="sxs-lookup"><span data-stu-id="299ac-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="299ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="299ac-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="299ac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="299ac-105">DESCRIPTION</span></span>
<span data-ttu-id="299ac-106">Das Add-AzSqlServerKeyVaultKey-Cmdlet fügt dem bereitgestellten Server einen Schlüsseltresorschlüssel SQL hinzu.</span><span class="sxs-lookup"><span data-stu-id="299ac-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="299ac-107">Der Server muss über die Berechtigungen "get, wrapKey, unwrapKey" für den Tresor verfügen.</span><span class="sxs-lookup"><span data-stu-id="299ac-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="299ac-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="299ac-108">EXAMPLES</span></span>

### <span data-ttu-id="299ac-109">Beispiel 1: Hinzufügen des Schlüsseltresorschlüssels</span><span class="sxs-lookup"><span data-stu-id="299ac-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="299ac-110">Mit diesem Befehl wird der Schlüsseltresorschlüssel mit der ID ' dem SQL https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 "ContosoServer" in der Ressourcengruppe "ContosoResourceGroup" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="299ac-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="299ac-111">ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445667789900111223345567789900 CreationDate : 01.01.2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="299ac-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="299ac-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="299ac-112">PARAMETERS</span></span>

### <span data-ttu-id="299ac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="299ac-113">-AsJob</span></span>
<span data-ttu-id="299ac-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="299ac-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="299ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299ac-115">-DefaultProfile</span></span>
<span data-ttu-id="299ac-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="299ac-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="299ac-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="299ac-117">-KeyId</span></span>
<span data-ttu-id="299ac-118">Die Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="299ac-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="299ac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299ac-119">-ResourceGroupName</span></span>
<span data-ttu-id="299ac-120">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="299ac-120">The name of the resource group</span></span>

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

### <span data-ttu-id="299ac-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="299ac-121">-ServerName</span></span>
<span data-ttu-id="299ac-122">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="299ac-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="299ac-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="299ac-123">-Confirm</span></span>
<span data-ttu-id="299ac-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="299ac-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="299ac-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="299ac-125">-WhatIf</span></span>
<span data-ttu-id="299ac-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="299ac-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="299ac-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="299ac-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="299ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299ac-128">CommonParameters</span></span>
<span data-ttu-id="299ac-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299ac-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="299ac-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299ac-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="299ac-131">INPUTS</span></span>

### <span data-ttu-id="299ac-132">System.String</span><span class="sxs-lookup"><span data-stu-id="299ac-132">System.String</span></span>

## <span data-ttu-id="299ac-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="299ac-133">OUTPUTS</span></span>

### <span data-ttu-id="299ac-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="299ac-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="299ac-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="299ac-135">NOTES</span></span>

## <span data-ttu-id="299ac-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="299ac-136">RELATED LINKS</span></span>

[<span data-ttu-id="299ac-137">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="299ac-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
