---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996262"
---
# <span data-ttu-id="44345-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="44345-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="44345-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44345-102">SYNOPSIS</span></span>
<span data-ttu-id="44345-103">Ruft die Daten Maskierungs Richtlinie für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="44345-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="44345-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44345-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44345-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44345-105">DESCRIPTION</span></span>
<span data-ttu-id="44345-106">Das Cmdlet " **Get-AzSqlDatabaseDataMaskingPolicy** " Ruft die Daten Maskierungs Richtlinie einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="44345-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="44345-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="44345-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="44345-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44345-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="44345-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44345-109">EXAMPLES</span></span>

### <span data-ttu-id="44345-110">Beispiel 1: Abrufen der Daten Maskierungs Richtlinie für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="44345-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="44345-111">Dieser Befehl ruft die Daten Maskierungs Richtlinie aus dem Daten Bank database01 in der Ressourcengruppen-ResourceGroup01 auf dem Server SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="44345-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="44345-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="44345-112">PARAMETERS</span></span>

### <span data-ttu-id="44345-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="44345-113">-DatabaseName</span></span>
<span data-ttu-id="44345-114">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="44345-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="44345-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44345-115">-DefaultProfile</span></span>
<span data-ttu-id="44345-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="44345-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44345-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44345-117">-ResourceGroupName</span></span>
<span data-ttu-id="44345-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="44345-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="44345-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="44345-119">-ServerName</span></span>
<span data-ttu-id="44345-120">Gibt den Namen des Servers an, auf dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="44345-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="44345-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44345-121">-Confirm</span></span>
<span data-ttu-id="44345-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44345-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44345-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44345-123">-WhatIf</span></span>
<span data-ttu-id="44345-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44345-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44345-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44345-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44345-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44345-126">CommonParameters</span></span>
<span data-ttu-id="44345-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44345-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44345-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44345-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44345-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44345-129">INPUTS</span></span>

### <span data-ttu-id="44345-130">System. String</span><span class="sxs-lookup"><span data-stu-id="44345-130">System.String</span></span>

## <span data-ttu-id="44345-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44345-131">OUTPUTS</span></span>

### <span data-ttu-id="44345-132">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="44345-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="44345-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="44345-133">NOTES</span></span>

## <span data-ttu-id="44345-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44345-134">RELATED LINKS</span></span>

[<span data-ttu-id="44345-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="44345-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="44345-136">Neu – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="44345-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="44345-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="44345-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="44345-138">Satz-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="44345-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="44345-139">Satz-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="44345-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


