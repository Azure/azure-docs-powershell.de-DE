---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: c1571dd5d03f82da13feec115fb9da123c6e3f69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825507"
---
# <span data-ttu-id="bdd2f-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bdd2f-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="bdd2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd2f-103">Ruft die transparente Datenverschlüsselung (DSA)-Beschützer ab</span><span class="sxs-lookup"><span data-stu-id="bdd2f-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="bdd2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdd2f-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdd2f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdd2f-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd2f-106">Das Get-AzSqlServerTransparentDataEncryptionProtector-Cmdlet ruft Informationen zur DSA-Beschützer ab.</span><span class="sxs-lookup"><span data-stu-id="bdd2f-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="bdd2f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdd2f-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd2f-108">Beispiel 1: Abrufen des DSA-Beschützers (transparent Data Encryption)</span><span class="sxs-lookup"><span data-stu-id="bdd2f-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="bdd2f-109">Dieser Befehl ruft die DSA-Beschützer für den Server mit dem Namen ContosoServer in der Ressourcengruppe mit dem Namen ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bdd2f-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="bdd2f-110">ResourceGroupName Servername Typ ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="bdd2f-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="bdd2f-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="bdd2f-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="bdd2f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdd2f-112">PARAMETERS</span></span>

### <span data-ttu-id="bdd2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd2f-113">-DefaultProfile</span></span>
<span data-ttu-id="bdd2f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bdd2f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdd2f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd2f-115">-ResourceGroupName</span></span>
<span data-ttu-id="bdd2f-116">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bdd2f-116">The name of the resource group</span></span>

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

### <span data-ttu-id="bdd2f-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="bdd2f-117">-ServerName</span></span>
<span data-ttu-id="bdd2f-118">Der Azure SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="bdd2f-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="bdd2f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bdd2f-119">-Confirm</span></span>
<span data-ttu-id="bdd2f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdd2f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd2f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd2f-121">-WhatIf</span></span>
<span data-ttu-id="bdd2f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdd2f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd2f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdd2f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd2f-124">CommonParameters</span></span>
<span data-ttu-id="bdd2f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd2f-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdd2f-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd2f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdd2f-127">INPUTS</span></span>

### <span data-ttu-id="bdd2f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bdd2f-128">System.String</span></span>

## <span data-ttu-id="bdd2f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdd2f-129">OUTPUTS</span></span>

### <span data-ttu-id="bdd2f-130">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="bdd2f-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="bdd2f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdd2f-131">NOTES</span></span>

## <span data-ttu-id="bdd2f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdd2f-132">RELATED LINKS</span></span>

[<span data-ttu-id="bdd2f-133">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="bdd2f-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
