---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 4f26955db9d99871cb0c5ae127b5977deedacf08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476490"
---
# <span data-ttu-id="3d267-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3d267-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="3d267-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d267-102">SYNOPSIS</span></span>
<span data-ttu-id="3d267-103">Ruft die schlüsseltresor Schlüssel von SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="3d267-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d267-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d267-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d267-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d267-105">DESCRIPTION</span></span>
<span data-ttu-id="3d267-106">Das Get-AzureRmSqlServerKeyVaultKey-Cmdlet ruft Informationen zu den schlüsseltresor Schlüsseln auf einem SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="3d267-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="3d267-107">Sie können alle Schlüssel auf einem Server anzeigen oder einen bestimmten Schlüssel anzeigen, indem Sie den KeyId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3d267-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="3d267-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d267-108">EXAMPLES</span></span>

### <span data-ttu-id="3d267-109">Beispiel 1: Abrufen aller schlüsseltresor-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="3d267-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="3d267-110">Dieser Befehl ruft alle schlüsseltresor Schlüssel auf einem SQL Server ab.</span><span class="sxs-lookup"><span data-stu-id="3d267-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="3d267-111">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="3d267-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="3d267-112">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey2_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Fingerabdruck: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="3d267-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="3d267-113">Beispiel 2: Abrufen eines bestimmten Key Vault-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3d267-113">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="3d267-114">Dieser Befehl ruft den Schlüssel Vault-Schlüssel mit der ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ab und speichert ihn dann in der $MyServerKeyVaultKey-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3d267-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="3d267-115">Sie können die Eigenschaften von $MyServerKeyVaultKey überprüfen, um Details zum schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d267-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="3d267-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d267-116">PARAMETERS</span></span>

### <span data-ttu-id="3d267-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d267-117">-DefaultProfile</span></span>
<span data-ttu-id="3d267-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d267-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d267-119">-KeyId</span><span class="sxs-lookup"><span data-stu-id="3d267-119">-KeyId</span></span>
<span data-ttu-id="3d267-120">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="3d267-120">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d267-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d267-121">-ResourceGroupName</span></span>
<span data-ttu-id="3d267-122">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3d267-122">The name of the resource group</span></span>

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

### <span data-ttu-id="3d267-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="3d267-123">-ServerName</span></span>
<span data-ttu-id="3d267-124">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="3d267-124">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="3d267-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d267-125">-Confirm</span></span>
<span data-ttu-id="3d267-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d267-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d267-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d267-127">-WhatIf</span></span>
<span data-ttu-id="3d267-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d267-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d267-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d267-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d267-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d267-130">CommonParameters</span></span>
<span data-ttu-id="3d267-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d267-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d267-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d267-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d267-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d267-133">INPUTS</span></span>

### <span data-ttu-id="3d267-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3d267-134">System.String</span></span>

## <span data-ttu-id="3d267-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d267-135">OUTPUTS</span></span>

### <span data-ttu-id="3d267-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="3d267-136">System.Object</span></span>

## <span data-ttu-id="3d267-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d267-137">NOTES</span></span>

## <span data-ttu-id="3d267-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d267-138">RELATED LINKS</span></span>

[<span data-ttu-id="3d267-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="3d267-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
