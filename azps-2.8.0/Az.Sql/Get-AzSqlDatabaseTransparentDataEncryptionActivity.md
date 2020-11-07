---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: bc072934fe8695cae0fd5f5762c1a31936997da9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825619"
---
# <span data-ttu-id="0574d-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="0574d-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="0574d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0574d-102">SYNOPSIS</span></span>
<span data-ttu-id="0574d-103">Ruft den Status eines DSA-Scans einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="0574d-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="0574d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0574d-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0574d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0574d-105">DESCRIPTION</span></span>
<span data-ttu-id="0574d-106">Das Cmdlet " **Get-AzSqlDatabaseTransparentDataEncryptionActivity** " Ruft den Fortschritt eines DSA-Scans (transparent Data Encryption) einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="0574d-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="0574d-107">Wenn keine Verschlüsselungs Spanne ausgeführt wird, gibt dieses Cmdlet eine leere Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="0574d-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="0574d-108">Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.</span><span class="sxs-lookup"><span data-stu-id="0574d-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="0574d-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0574d-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0574d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0574d-110">EXAMPLES</span></span>

### <span data-ttu-id="0574d-111">Beispiel 1: Abrufen der DSA-Aktivität für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="0574d-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="0574d-112">Dieser Befehl ruft die DSA-Aktivität für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="0574d-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="0574d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0574d-113">PARAMETERS</span></span>

### <span data-ttu-id="0574d-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0574d-114">-DatabaseName</span></span>
<span data-ttu-id="0574d-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet eine DSA-Verschlüsselungs Aktivität erhält.</span><span class="sxs-lookup"><span data-stu-id="0574d-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="0574d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0574d-116">-DefaultProfile</span></span>
<span data-ttu-id="0574d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0574d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0574d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0574d-118">-ResourceGroupName</span></span>
<span data-ttu-id="0574d-119">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0574d-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0574d-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="0574d-120">-ServerName</span></span>
<span data-ttu-id="0574d-121">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="0574d-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="0574d-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0574d-122">-Confirm</span></span>
<span data-ttu-id="0574d-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0574d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0574d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0574d-124">-WhatIf</span></span>
<span data-ttu-id="0574d-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0574d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0574d-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0574d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0574d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0574d-127">CommonParameters</span></span>
<span data-ttu-id="0574d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0574d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0574d-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0574d-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0574d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0574d-130">INPUTS</span></span>

### <span data-ttu-id="0574d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0574d-131">System.String</span></span>

## <span data-ttu-id="0574d-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0574d-132">OUTPUTS</span></span>

### <span data-ttu-id="0574d-133">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="0574d-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="0574d-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0574d-134">NOTES</span></span>

## <span data-ttu-id="0574d-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0574d-135">RELATED LINKS</span></span>

[<span data-ttu-id="0574d-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0574d-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="0574d-137">Satz-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0574d-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


