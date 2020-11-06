---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 0566396e3a32891b010b2bfa3cd71ba47d4a7e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479846"
---
# <span data-ttu-id="337ee-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="337ee-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="337ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="337ee-102">SYNOPSIS</span></span>
<span data-ttu-id="337ee-103">Ruft den Status "DSA" für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="337ee-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="337ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="337ee-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="337ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="337ee-105">DESCRIPTION</span></span>
<span data-ttu-id="337ee-106">Das Cmdlet " **Get-AzureRmSqlDatabaseTransparentDataEncryption** " Ruft den Zustand der transparenten Datenverschlüsselung (DSA) für eine Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="337ee-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="337ee-107">Weitere Informationen finden Sie unter transparente Datenverschlüsselung mit Azure SQL-Datenbank https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) in der Microsoft Developer-Netzwerkbibliothek.</span><span class="sxs-lookup"><span data-stu-id="337ee-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="337ee-108">Dieses Cmdlet ruft den aktuellen Status von "DSA" ab, aber sowohl die Verschlüsselung als auch die Entschlüsselung können Vorgänge mit langer Laufzeit sein.</span><span class="sxs-lookup"><span data-stu-id="337ee-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="337ee-109">Führen Sie das Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity-Cmdlet aus, um den Status des Verschlüsselungs Scans anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="337ee-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>

<span data-ttu-id="337ee-110">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="337ee-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="337ee-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="337ee-111">EXAMPLES</span></span>

### <span data-ttu-id="337ee-112">Beispiel 1: Abrufen des DSA-Status für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="337ee-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="337ee-113">Dieser Befehl ruft den Status von "DSA" für die Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" ab.</span><span class="sxs-lookup"><span data-stu-id="337ee-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="337ee-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="337ee-114">PARAMETERS</span></span>

### <span data-ttu-id="337ee-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="337ee-115">-DatabaseName</span></span>
<span data-ttu-id="337ee-116">Gibt den Namen der Datenbank an, für die dieses Cmdlet den DSA-Status erhält.</span><span class="sxs-lookup"><span data-stu-id="337ee-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="337ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="337ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="337ee-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="337ee-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="337ee-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="337ee-119">-ServerName</span></span>
<span data-ttu-id="337ee-120">Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet den DSA-Status erhält.</span><span class="sxs-lookup"><span data-stu-id="337ee-120">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="337ee-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="337ee-121">-Confirm</span></span>
<span data-ttu-id="337ee-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="337ee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="337ee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="337ee-123">-WhatIf</span></span>
<span data-ttu-id="337ee-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="337ee-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="337ee-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="337ee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="337ee-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337ee-126">-DefaultProfile</span></span>
<span data-ttu-id="337ee-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="337ee-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="337ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337ee-128">CommonParameters</span></span>
<span data-ttu-id="337ee-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337ee-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="337ee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337ee-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="337ee-131">INPUTS</span></span>

## <span data-ttu-id="337ee-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="337ee-132">OUTPUTS</span></span>

### <span data-ttu-id="337ee-133">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="337ee-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="337ee-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="337ee-134">NOTES</span></span>

## <span data-ttu-id="337ee-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="337ee-135">RELATED LINKS</span></span>

[<span data-ttu-id="337ee-136">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="337ee-136">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="337ee-137">Satz-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="337ee-137">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
