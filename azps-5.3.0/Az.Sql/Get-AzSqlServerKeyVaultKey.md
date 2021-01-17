---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376520"
---
# <span data-ttu-id="5567e-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5567e-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="5567e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5567e-102">SYNOPSIS</span></span>
<span data-ttu-id="5567e-103">Ruft die SQL des Schlüsseltresor eines Servers ab.</span><span class="sxs-lookup"><span data-stu-id="5567e-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="5567e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5567e-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5567e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5567e-105">DESCRIPTION</span></span>
<span data-ttu-id="5567e-106">Das Get-AzSqlServerKeyVaultKey cmdlet ruft Informationen zu den Schlüsseln des Tresors auf einem SQL ab.</span><span class="sxs-lookup"><span data-stu-id="5567e-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="5567e-107">Sie können alle Schlüssel auf einem Server oder einen bestimmten Schlüssel anzeigen, indem Sie die KeyId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5567e-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="5567e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5567e-108">EXAMPLES</span></span>

### <span data-ttu-id="5567e-109">Beispiel 1: Alle Schlüssel des Tresors erhalten</span><span class="sxs-lookup"><span data-stu-id="5567e-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5567e-110">Dieser Befehl ruft alle Schlüssel des Schlüsseltresor auf einem SQL ab.</span><span class="sxs-lookup"><span data-stu-id="5567e-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="5567e-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122334455667788990011223344556677889900 CreationDate: 01.01.2017 00:00:00GroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Type: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint : 00998877665544332211009877665544332211 CreationDate: 01.01.2017 00:00</span><span class="sxs-lookup"><span data-stu-id="5567e-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="5567e-112">Beispiel 2: Erhalten eines bestimmten Schlüsseltresorschlüssels</span><span class="sxs-lookup"><span data-stu-id="5567e-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="5567e-113">Dieser Befehl ruft den Schlüssel des Schlüsseltresor mit der ID ' ' ab und speichert ihn dann in der https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 $MyServerKeyVaultKey Variable.</span><span class="sxs-lookup"><span data-stu-id="5567e-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="5567e-114">Sie können die Eigenschaften von $MyServerKeyVaultKey, um Details zum Schlüsseltresor zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5567e-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="5567e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5567e-115">PARAMETERS</span></span>

### <span data-ttu-id="5567e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5567e-116">-DefaultProfile</span></span>
<span data-ttu-id="5567e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5567e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5567e-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="5567e-118">-KeyId</span></span>
<span data-ttu-id="5567e-119">Die KeyId des Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5567e-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5567e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5567e-120">-ResourceGroupName</span></span>
<span data-ttu-id="5567e-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5567e-121">The name of the resource group</span></span>

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

### <span data-ttu-id="5567e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5567e-122">-ServerName</span></span>
<span data-ttu-id="5567e-123">Der Azure Sql Server-Name.</span><span class="sxs-lookup"><span data-stu-id="5567e-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="5567e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5567e-124">-Confirm</span></span>
<span data-ttu-id="5567e-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5567e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5567e-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5567e-126">-WhatIf</span></span>
<span data-ttu-id="5567e-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5567e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5567e-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5567e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5567e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5567e-129">CommonParameters</span></span>
<span data-ttu-id="5567e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5567e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5567e-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5567e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5567e-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5567e-132">INPUTS</span></span>

### <span data-ttu-id="5567e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5567e-133">System.String</span></span>

## <span data-ttu-id="5567e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5567e-134">OUTPUTS</span></span>

### <span data-ttu-id="5567e-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="5567e-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="5567e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5567e-136">NOTES</span></span>

## <span data-ttu-id="5567e-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5567e-137">RELATED LINKS</span></span>

[<span data-ttu-id="5567e-138">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="5567e-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
