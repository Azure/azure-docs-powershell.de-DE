---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 13ab762b7f5ed8457bc8975687c3a45315be969b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664968"
---
# <span data-ttu-id="ae9eb-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9eb-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="ae9eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9eb-103">Ruft die Daten Maskierungs Richtlinie für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae9eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae9eb-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae9eb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae9eb-105">DESCRIPTION</span></span>
<span data-ttu-id="ae9eb-106">Das Cmdlet " **Get-AzureRmSqlDatabaseDataMaskingPolicy** " Ruft die Daten Maskierungs Richtlinie einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="ae9eb-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="ae9eb-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ae9eb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae9eb-109">EXAMPLES</span></span>

### <span data-ttu-id="ae9eb-110">Beispiel 1: Abrufen der Daten Maskierungs Richtlinie für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ae9eb-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="ae9eb-111">Dieser Befehl ruft die Daten Maskierungs Richtlinie aus dem Daten Bank database01 in der Ressourcengruppen-ResourceGroup01 auf dem Server SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="ae9eb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae9eb-112">PARAMETERS</span></span>

### <span data-ttu-id="ae9eb-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae9eb-113">-DatabaseName</span></span>
<span data-ttu-id="ae9eb-114">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ae9eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae9eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae9eb-116">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-116">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ae9eb-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="ae9eb-117">-ServerName</span></span>
<span data-ttu-id="ae9eb-118">Gibt den Namen des Servers an, auf dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-118">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="ae9eb-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae9eb-119">-Confirm</span></span>
<span data-ttu-id="ae9eb-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae9eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae9eb-121">-WhatIf</span></span>
<span data-ttu-id="ae9eb-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae9eb-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae9eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9eb-124">-DefaultProfile</span></span>
<span data-ttu-id="ae9eb-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae9eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9eb-126">CommonParameters</span></span>
<span data-ttu-id="ae9eb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9eb-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae9eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9eb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae9eb-129">INPUTS</span></span>

## <span data-ttu-id="ae9eb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae9eb-130">OUTPUTS</span></span>

### <span data-ttu-id="ae9eb-131">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ae9eb-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="ae9eb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae9eb-132">NOTES</span></span>

## <span data-ttu-id="ae9eb-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae9eb-133">RELATED LINKS</span></span>

[<span data-ttu-id="ae9eb-134">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae9eb-134">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae9eb-135">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae9eb-135">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae9eb-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae9eb-136">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae9eb-137">Satz-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae9eb-137">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="ae9eb-138">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae9eb-138">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


