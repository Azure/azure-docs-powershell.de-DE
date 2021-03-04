---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0bdfa7ddf86beef3b9db26ff36a1953a1b574fd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949971"
---
# <span data-ttu-id="eafd4-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="eafd4-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="eafd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eafd4-102">SYNOPSIS</span></span>
<span data-ttu-id="eafd4-103">Ruft den Fortschritt einer TDE-Überprüfung einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="eafd4-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="eafd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eafd4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eafd4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eafd4-105">DESCRIPTION</span></span>
<span data-ttu-id="eafd4-106">Das **Get-AzSqlDatabaseTransparentDataEncryptionActivity-Cmdlet** ruft den Fortschritt einer Transparent Data Encryption (TDE)-Überprüfung einer Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="eafd4-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="eafd4-107">Wenn keine Verschlüsselungsspanne ausgeführt wird, gibt dieses Cmdlet eine leere Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="eafd4-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="eafd4-108">Weitere Informationen finden Sie unter Transparente Datenverschlüsselung mit Azure SQL -Datenbank https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (in der Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="eafd4-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="eafd4-109">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eafd4-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="eafd4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eafd4-110">EXAMPLES</span></span>

### <span data-ttu-id="eafd4-111">Beispiel 1: Get TDE activity for a database</span><span class="sxs-lookup"><span data-stu-id="eafd4-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="eafd4-112">Dieser Befehl ruft die TDE-Aktivität für die Datenbank mit dem Namen datenbank01 auf dem Server mit dem Namen server01 ab.</span><span class="sxs-lookup"><span data-stu-id="eafd4-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="eafd4-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eafd4-113">PARAMETERS</span></span>

### <span data-ttu-id="eafd4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eafd4-114">-DatabaseName</span></span>
<span data-ttu-id="eafd4-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet die TDE-Verschlüsselungsaktivität erhält.</span><span class="sxs-lookup"><span data-stu-id="eafd4-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="eafd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafd4-116">-DefaultProfile</span></span>
<span data-ttu-id="eafd4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="eafd4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eafd4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafd4-118">-ResourceGroupName</span></span>
<span data-ttu-id="eafd4-119">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="eafd4-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="eafd4-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="eafd4-120">-ServerName</span></span>
<span data-ttu-id="eafd4-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="eafd4-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="eafd4-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eafd4-122">-Confirm</span></span>
<span data-ttu-id="eafd4-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eafd4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eafd4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eafd4-124">-WhatIf</span></span>
<span data-ttu-id="eafd4-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eafd4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eafd4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eafd4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eafd4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafd4-127">CommonParameters</span></span>
<span data-ttu-id="eafd4-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafd4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafd4-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eafd4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafd4-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eafd4-130">INPUTS</span></span>

### <span data-ttu-id="eafd4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="eafd4-131">System.String</span></span>

## <span data-ttu-id="eafd4-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eafd4-132">OUTPUTS</span></span>

### <span data-ttu-id="eafd4-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="eafd4-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="eafd4-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eafd4-134">NOTES</span></span>

## <span data-ttu-id="eafd4-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eafd4-135">RELATED LINKS</span></span>

[<span data-ttu-id="eafd4-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="eafd4-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="eafd4-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="eafd4-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


