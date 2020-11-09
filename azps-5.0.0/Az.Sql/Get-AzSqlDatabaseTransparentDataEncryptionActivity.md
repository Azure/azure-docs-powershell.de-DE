---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296691"
---
# <span data-ttu-id="a0de7-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="a0de7-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="a0de7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0de7-102">SYNOPSIS</span></span>
<span data-ttu-id="a0de7-103">Ruft den Status eines DSA-Scans einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="a0de7-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="a0de7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0de7-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0de7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0de7-105">DESCRIPTION</span></span>
<span data-ttu-id="a0de7-106">Das Cmdlet " **Get-AzSqlDatabaseTransparentDataEncryptionActivity** " Ruft den Fortschritt eines DSA-Scans (transparent Data Encryption) einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="a0de7-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="a0de7-107">Wenn keine Verschlüsselungs Spanne ausgeführt wird, gibt dieses Cmdlet eine leere Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="a0de7-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="a0de7-108">Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.</span><span class="sxs-lookup"><span data-stu-id="a0de7-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="a0de7-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0de7-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0de7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0de7-110">EXAMPLES</span></span>

### <span data-ttu-id="a0de7-111">Beispiel 1: Abrufen der DSA-Aktivität für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a0de7-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="a0de7-112">Dieser Befehl ruft die DSA-Aktivität für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="a0de7-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="a0de7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0de7-113">PARAMETERS</span></span>

### <span data-ttu-id="a0de7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0de7-114">-DatabaseName</span></span>
<span data-ttu-id="a0de7-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet eine DSA-Verschlüsselungs Aktivität erhält.</span><span class="sxs-lookup"><span data-stu-id="a0de7-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="a0de7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0de7-116">-DefaultProfile</span></span>
<span data-ttu-id="a0de7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0de7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0de7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0de7-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0de7-119">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a0de7-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a0de7-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="a0de7-120">-ServerName</span></span>
<span data-ttu-id="a0de7-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="a0de7-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="a0de7-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0de7-122">-Confirm</span></span>
<span data-ttu-id="a0de7-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0de7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0de7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0de7-124">-WhatIf</span></span>
<span data-ttu-id="a0de7-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0de7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0de7-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0de7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0de7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0de7-127">CommonParameters</span></span>
<span data-ttu-id="a0de7-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0de7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0de7-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0de7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0de7-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0de7-130">INPUTS</span></span>

### <span data-ttu-id="a0de7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a0de7-131">System.String</span></span>

## <span data-ttu-id="a0de7-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0de7-132">OUTPUTS</span></span>

### <span data-ttu-id="a0de7-133">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="a0de7-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="a0de7-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0de7-134">NOTES</span></span>

## <span data-ttu-id="a0de7-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0de7-135">RELATED LINKS</span></span>

[<span data-ttu-id="a0de7-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a0de7-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="a0de7-137">Satz-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="a0de7-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


