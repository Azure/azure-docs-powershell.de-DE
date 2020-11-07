---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0f858e2ad0260995b71ec6146a6ce7e64bd48c29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662475"
---
# <span data-ttu-id="7948f-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="7948f-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="7948f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7948f-102">SYNOPSIS</span></span>
<span data-ttu-id="7948f-103">Ruft den Status eines DSA-Scans einer Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="7948f-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7948f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7948f-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7948f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7948f-105">DESCRIPTION</span></span>
<span data-ttu-id="7948f-106">Das Cmdlet " **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** " Ruft den Fortschritt eines DSA-Scans (transparent Data Encryption) einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="7948f-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="7948f-107">Wenn keine Verschlüsselungs Spanne ausgeführt wird, gibt dieses Cmdlet eine leere Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="7948f-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="7948f-108">Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.</span><span class="sxs-lookup"><span data-stu-id="7948f-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="7948f-109">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7948f-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7948f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7948f-110">EXAMPLES</span></span>

### <span data-ttu-id="7948f-111">Beispiel 1: Abrufen der DSA-Aktivität für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="7948f-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="7948f-112">Dieser Befehl ruft die DSA-Aktivität für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="7948f-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="7948f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7948f-113">PARAMETERS</span></span>

### <span data-ttu-id="7948f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7948f-114">-DatabaseName</span></span>
<span data-ttu-id="7948f-115">Gibt den Namen der Datenbank an, für die dieses Cmdlet eine DSA-Verschlüsselungs Aktivität erhält.</span><span class="sxs-lookup"><span data-stu-id="7948f-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="7948f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7948f-116">-ResourceGroupName</span></span>
<span data-ttu-id="7948f-117">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7948f-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="7948f-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="7948f-118">-ServerName</span></span>
<span data-ttu-id="7948f-119">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="7948f-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7948f-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7948f-120">-Confirm</span></span>
<span data-ttu-id="7948f-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7948f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7948f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7948f-122">-WhatIf</span></span>
<span data-ttu-id="7948f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7948f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7948f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7948f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7948f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7948f-125">-DefaultProfile</span></span>
<span data-ttu-id="7948f-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7948f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7948f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7948f-127">CommonParameters</span></span>
<span data-ttu-id="7948f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7948f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7948f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7948f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7948f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7948f-130">INPUTS</span></span>

## <span data-ttu-id="7948f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7948f-131">OUTPUTS</span></span>

### <span data-ttu-id="7948f-132">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="7948f-132">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="7948f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7948f-133">NOTES</span></span>

## <span data-ttu-id="7948f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7948f-134">RELATED LINKS</span></span>

[<span data-ttu-id="7948f-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7948f-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="7948f-136">Satz-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="7948f-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


