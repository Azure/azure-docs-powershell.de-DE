---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145745"
---
# <span data-ttu-id="3a7e9-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="3a7e9-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="3a7e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7e9-103">Ruft den Fortschritt einer TDE-Überprüfung einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="3a7e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a7e9-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a7e9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a7e9-105">DESCRIPTION</span></span>
<span data-ttu-id="3a7e9-106">Das **Cmdlet "Get-AzSqlDatabaseTransparentDataEncryptionActivity"** ruft den Fortschritt einer Transparent Data Encryption (TDE)-Überprüfung einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="3a7e9-107">Wenn kein Verschlüsselungsspanne ausgeführt wird, gibt dieses Cmdlet eine leere Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="3a7e9-108">Weitere Informationen finden Sie unter "Transparente Datenverschlüsselung mit Azure SQL-Datenbank" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (in der Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="3a7e9-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="3a7e9-109">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3a7e9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a7e9-110">EXAMPLES</span></span>

### <span data-ttu-id="3a7e9-111">Beispiel 1: Get TDE activity for a database</span><span class="sxs-lookup"><span data-stu-id="3a7e9-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="3a7e9-112">Dieser Befehl ruft die "TDE-Aktivität" für die Datenbank mit dem Namen "database01" auf dem Server "server01" ab.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="3a7e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a7e9-113">PARAMETERS</span></span>

### <span data-ttu-id="3a7e9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a7e9-114">-DatabaseName</span></span>
<span data-ttu-id="3a7e9-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet die TDE-Verschlüsselungsaktivität erhält.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="3a7e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7e9-116">-DefaultProfile</span></span>
<span data-ttu-id="3a7e9-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3a7e9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a7e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a7e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a7e9-119">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3a7e9-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3a7e9-120">-ServerName</span></span>
<span data-ttu-id="3a7e9-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3a7e9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a7e9-122">-Confirm</span></span>
<span data-ttu-id="3a7e9-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a7e9-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3a7e9-124">-WhatIf</span></span>
<span data-ttu-id="3a7e9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a7e9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a7e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7e9-127">CommonParameters</span></span>
<span data-ttu-id="3a7e9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a7e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7e9-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a7e9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7e9-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a7e9-130">INPUTS</span></span>

### <span data-ttu-id="3a7e9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3a7e9-131">System.String</span></span>

## <span data-ttu-id="3a7e9-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a7e9-132">OUTPUTS</span></span>

### <span data-ttu-id="3a7e9-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="3a7e9-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="3a7e9-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a7e9-134">NOTES</span></span>

## <span data-ttu-id="3a7e9-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a7e9-135">RELATED LINKS</span></span>

[<span data-ttu-id="3a7e9-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3a7e9-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="3a7e9-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3a7e9-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


