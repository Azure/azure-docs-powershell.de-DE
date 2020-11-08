---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179632"
---
# <span data-ttu-id="fc629-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc629-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="fc629-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc629-102">SYNOPSIS</span></span>
<span data-ttu-id="fc629-103">Ruft die schlüsseltresor Schlüssel von SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="fc629-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="fc629-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc629-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc629-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc629-105">DESCRIPTION</span></span>
<span data-ttu-id="fc629-106">Das Get-AzSqlServerKeyVaultKey-Cmdlet ruft Informationen zu den schlüsseltresor Schlüsseln auf einem SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="fc629-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="fc629-107">Sie können alle Schlüssel auf einem Server anzeigen oder einen bestimmten Schlüssel anzeigen, indem Sie den KeyId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fc629-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="fc629-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc629-108">EXAMPLES</span></span>

### <span data-ttu-id="fc629-109">Beispiel 1: Abrufen aller schlüsseltresor-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="fc629-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="fc629-110">Dieser Befehl ruft alle schlüsseltresor Schlüssel auf einem SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="fc629-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="fc629-111">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Type: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Fingerabdruck: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="fc629-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="fc629-112">Beispiel 2: Abrufen eines bestimmten Key Vault-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="fc629-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="fc629-113">Dieser Befehl ruft den Schlüssel Vault-Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ab und speichert ihn dann in der $MyServerKeyVaultKey-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fc629-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="fc629-114">Sie können die Eigenschaften von $MyServerKeyVaultKey überprüfen, um Details zum schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fc629-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="fc629-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc629-115">PARAMETERS</span></span>

### <span data-ttu-id="fc629-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc629-116">-DefaultProfile</span></span>
<span data-ttu-id="fc629-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fc629-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc629-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="fc629-118">-KeyId</span></span>
<span data-ttu-id="fc629-119">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="fc629-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="fc629-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc629-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc629-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fc629-121">The name of the resource group</span></span>

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

### <span data-ttu-id="fc629-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="fc629-122">-ServerName</span></span>
<span data-ttu-id="fc629-123">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="fc629-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fc629-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc629-124">-Confirm</span></span>
<span data-ttu-id="fc629-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc629-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc629-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc629-126">-WhatIf</span></span>
<span data-ttu-id="fc629-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc629-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc629-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc629-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc629-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc629-129">CommonParameters</span></span>
<span data-ttu-id="fc629-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc629-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc629-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc629-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc629-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc629-132">INPUTS</span></span>

### <span data-ttu-id="fc629-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fc629-133">System.String</span></span>

## <span data-ttu-id="fc629-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc629-134">OUTPUTS</span></span>

### <span data-ttu-id="fc629-135">Microsoft. Azure. Commands. SQL. ServerKeyVaultKey. Model. AzureSqlServerKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="fc629-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="fc629-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc629-136">NOTES</span></span>

## <span data-ttu-id="fc629-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc629-137">RELATED LINKS</span></span>

[<span data-ttu-id="fc629-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="fc629-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
