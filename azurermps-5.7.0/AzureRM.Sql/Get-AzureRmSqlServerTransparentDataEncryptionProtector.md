---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: ecb49271c49e441140a43f8cb8ae5d65be56cd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664158"
---
# <span data-ttu-id="b7b24-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b7b24-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="b7b24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7b24-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b24-103">Ruft die transparente Datenverschlüsselung (DSA)-Beschützer ab</span><span class="sxs-lookup"><span data-stu-id="b7b24-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7b24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b24-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7b24-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7b24-105">DESCRIPTION</span></span>
<span data-ttu-id="b7b24-106">Das Get-AzureRmSqlServerTransparentDataEncryptionProtector-Cmdlet ruft Informationen zur DSA-Beschützer ab.</span><span class="sxs-lookup"><span data-stu-id="b7b24-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="b7b24-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7b24-107">EXAMPLES</span></span>

### <span data-ttu-id="b7b24-108">Beispiel 1: Abrufen des DSA-Beschützers (transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="b7b24-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="b7b24-109">Dieser Befehl ruft die DSA-Beschützer für den Server mit dem Namen ContosoServer in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b7b24-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="b7b24-110">ResourceGroupName Servername Typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="b7b24-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="b7b24-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="b7b24-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="b7b24-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b24-112">PARAMETERS</span></span>

### <span data-ttu-id="b7b24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b24-113">-DefaultProfile</span></span>
<span data-ttu-id="b7b24-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b7b24-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7b24-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b24-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7b24-116">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b7b24-116">The name of the resource group</span></span>

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

### <span data-ttu-id="b7b24-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="b7b24-117">-ServerName</span></span>
<span data-ttu-id="b7b24-118">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="b7b24-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b7b24-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7b24-119">-Confirm</span></span>
<span data-ttu-id="b7b24-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7b24-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7b24-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7b24-121">-WhatIf</span></span>
<span data-ttu-id="b7b24-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7b24-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7b24-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7b24-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7b24-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b24-124">CommonParameters</span></span>
<span data-ttu-id="b7b24-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b24-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b24-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b24-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b24-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7b24-127">INPUTS</span></span>

### <span data-ttu-id="b7b24-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b24-128">System.String</span></span>

## <span data-ttu-id="b7b24-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7b24-129">OUTPUTS</span></span>

### <span data-ttu-id="b7b24-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="b7b24-130">System.Object</span></span>

## <span data-ttu-id="b7b24-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7b24-131">NOTES</span></span>

## <span data-ttu-id="b7b24-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7b24-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7b24-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b7b24-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
