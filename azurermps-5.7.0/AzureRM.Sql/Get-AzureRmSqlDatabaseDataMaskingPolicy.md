---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: bb6beb99171f376fb1ce6ba19b43a93b830457e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500381"
---
# <span data-ttu-id="c9536-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c9536-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="c9536-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9536-102">SYNOPSIS</span></span>
<span data-ttu-id="c9536-103">Ruft die Daten Maskierungs Richtlinie für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c9536-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9536-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9536-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9536-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9536-105">DESCRIPTION</span></span>
<span data-ttu-id="c9536-106">Das Cmdlet " **Get-AzureRmSqlDatabaseDataMaskingPolicy** " Ruft die Daten Maskierungs Richtlinie einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c9536-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="c9536-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c9536-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="c9536-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9536-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c9536-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9536-109">EXAMPLES</span></span>

### <span data-ttu-id="c9536-110">Beispiel 1: Abrufen der Daten Maskierungs Richtlinie für eine Azure SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="c9536-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="c9536-111">Dieser Befehl ruft die Daten Maskierungs Richtlinie aus dem Daten Bank database01 in der Ressourcengruppen-ResourceGroup01 auf dem Server SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="c9536-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="c9536-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9536-112">PARAMETERS</span></span>

### <span data-ttu-id="c9536-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9536-113">-DatabaseName</span></span>
<span data-ttu-id="c9536-114">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="c9536-114">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9536-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9536-115">-DefaultProfile</span></span>
<span data-ttu-id="c9536-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c9536-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9536-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9536-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9536-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c9536-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c9536-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="c9536-119">-ServerName</span></span>
<span data-ttu-id="c9536-120">Gibt den Namen des Servers an, auf dem sich die Datenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="c9536-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="c9536-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9536-121">-Confirm</span></span>
<span data-ttu-id="c9536-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9536-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9536-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9536-123">-WhatIf</span></span>
<span data-ttu-id="c9536-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9536-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9536-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9536-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9536-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9536-126">CommonParameters</span></span>
<span data-ttu-id="c9536-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9536-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9536-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9536-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9536-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9536-129">INPUTS</span></span>

### <span data-ttu-id="c9536-130">Keine</span><span class="sxs-lookup"><span data-stu-id="c9536-130">None</span></span>
<span data-ttu-id="c9536-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c9536-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9536-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9536-132">OUTPUTS</span></span>

### <span data-ttu-id="c9536-133">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c9536-133">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="c9536-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9536-134">NOTES</span></span>

## <span data-ttu-id="c9536-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9536-135">RELATED LINKS</span></span>

[<span data-ttu-id="c9536-136">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c9536-136">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c9536-137">Neu – AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c9536-137">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c9536-138">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c9536-138">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="c9536-139">Satz-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="c9536-139">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="c9536-140">Satz-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="c9536-140">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


