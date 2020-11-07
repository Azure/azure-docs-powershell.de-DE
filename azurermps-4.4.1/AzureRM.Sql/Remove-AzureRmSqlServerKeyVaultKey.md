---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: e8606f9eecfac63b68e9b8a26ecbebb89431e509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662391"
---
# <span data-ttu-id="663a5-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="663a5-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="663a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="663a5-102">SYNOPSIS</span></span>
<span data-ttu-id="663a5-103">Entfernt einen Key Vault-Schlüssel aus einem SQL Server.</span><span class="sxs-lookup"><span data-stu-id="663a5-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="663a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="663a5-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="663a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="663a5-105">DESCRIPTION</span></span>
<span data-ttu-id="663a5-106">Das Remove-AzureRmSqlServerKeyVaultKey-Cmdlet entfernt den schlüsseltresor Schlüssel aus dem angegebenen SQL Server.</span><span class="sxs-lookup"><span data-stu-id="663a5-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>

<span data-ttu-id="663a5-107">Beachten Sie, dass die SQL Server-Berechtigungen für den Tresor des Schlüssels nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="663a5-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="663a5-108">Wenn Sie Berechtigungen ändern möchten, verwenden Sie die Einstellung-AzureRmKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="663a5-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>

<span data-ttu-id="663a5-109">Beachten Sie, dass dieses Cmdlet keine Änderungen an Key Vault vornimmt.</span><span class="sxs-lookup"><span data-stu-id="663a5-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="663a5-110">Wenn Sie einen Schlüssel aus dem Schlüsselspeicher entfernen möchten, verwenden Sie Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="663a5-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="663a5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="663a5-111">EXAMPLES</span></span>

### <span data-ttu-id="663a5-112">--------------------------Beispiel 1: Entfernen eines Key Vault-Schlüssels--------------------------</span><span class="sxs-lookup"><span data-stu-id="663a5-112">--------------------------  Example 1: Remove a Key Vault key  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="663a5-113">Mit diesem Befehl wird der Key Vault-Schlüssel mit https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 der ID ' ' vom angegebenen Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="663a5-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>

<span data-ttu-id="663a5-114">ResourceGroupName: ContosoResourceGroup Servername: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault URI: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Fingerabdruck: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 am</span><span class="sxs-lookup"><span data-stu-id="663a5-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="663a5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="663a5-115">PARAMETERS</span></span>

### <span data-ttu-id="663a5-116">-KeyId</span><span class="sxs-lookup"><span data-stu-id="663a5-116">-KeyId</span></span>
<span data-ttu-id="663a5-117">Der Azure Key Vault-KeyId</span><span class="sxs-lookup"><span data-stu-id="663a5-117">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="663a5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663a5-118">-ResourceGroupName</span></span>
<span data-ttu-id="663a5-119">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="663a5-119">The name of the resource group</span></span>

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

### <span data-ttu-id="663a5-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="663a5-120">-ServerName</span></span>
<span data-ttu-id="663a5-121">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="663a5-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="663a5-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="663a5-122">-Confirm</span></span>
<span data-ttu-id="663a5-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="663a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="663a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="663a5-124">-WhatIf</span></span>
<span data-ttu-id="663a5-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="663a5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="663a5-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="663a5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="663a5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663a5-127">-DefaultProfile</span></span>
<span data-ttu-id="663a5-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="663a5-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663a5-129">CommonParameters</span></span>
<span data-ttu-id="663a5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="663a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663a5-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="663a5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663a5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="663a5-132">INPUTS</span></span>

### <span data-ttu-id="663a5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="663a5-133">System.String</span></span>

## <span data-ttu-id="663a5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="663a5-134">OUTPUTS</span></span>

### <span data-ttu-id="663a5-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="663a5-135">System.Object</span></span>

## <span data-ttu-id="663a5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="663a5-136">NOTES</span></span>

## <span data-ttu-id="663a5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="663a5-137">RELATED LINKS</span></span>

[<span data-ttu-id="663a5-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="663a5-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
