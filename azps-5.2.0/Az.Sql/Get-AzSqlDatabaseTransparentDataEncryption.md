---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371971"
---
# <span data-ttu-id="27b46-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="27b46-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="27b46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b46-102">SYNOPSIS</span></span>
<span data-ttu-id="27b46-103">Ruft den Status "TDE" für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="27b46-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="27b46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27b46-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27b46-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27b46-105">DESCRIPTION</span></span>
<span data-ttu-id="27b46-106">Das **Cmdlet "Get-AzSqlDatabaseTransparentDataEncryption"** ruft den Status der transparenten Datenverschlüsselung (Transparent Data Encryption, TDE) für eine Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="27b46-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="27b46-107">Weitere Informationen finden Sie unter "Transparente Datenverschlüsselung mit Azure SQL-Datenbank" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (in der Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="27b46-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="27b46-108">Dieses Cmdlet ruft den aktuellen Zustand von TDE ab, aber sowohl die Verschlüsselung als auch die Entschlüsselung können Vorgänge mit langer Dauer sein.</span><span class="sxs-lookup"><span data-stu-id="27b46-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="27b46-109">Um den Fortschritt des Verschlüsselungsscans zu sehen, führen Sie das Get-AzSqlDatabaseTransparentDataEncryptionActivity aus.</span><span class="sxs-lookup"><span data-stu-id="27b46-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="27b46-110">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27b46-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="27b46-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27b46-111">EXAMPLES</span></span>

### <span data-ttu-id="27b46-112">Beispiel 1: Erhalten des Status "TDE" für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="27b46-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="27b46-113">Dieser Befehl ruft den Status "TDE" für die Datenbank mit dem Namen "Database01" auf dem Server "server01" ab.</span><span class="sxs-lookup"><span data-stu-id="27b46-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="27b46-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b46-114">PARAMETERS</span></span>

### <span data-ttu-id="27b46-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27b46-115">-DatabaseName</span></span>
<span data-ttu-id="27b46-116">Gibt den Namen der Datenbank an, für die dieses Cmdlet den Status "TDE" erhält.</span><span class="sxs-lookup"><span data-stu-id="27b46-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="27b46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b46-117">-DefaultProfile</span></span>
<span data-ttu-id="27b46-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="27b46-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27b46-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b46-119">-ResourceGroupName</span></span>
<span data-ttu-id="27b46-120">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="27b46-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="27b46-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27b46-121">-ServerName</span></span>
<span data-ttu-id="27b46-122">Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet den STATUS "TDE" erhält.</span><span class="sxs-lookup"><span data-stu-id="27b46-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="27b46-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27b46-123">-Confirm</span></span>
<span data-ttu-id="27b46-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27b46-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b46-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="27b46-125">-WhatIf</span></span>
<span data-ttu-id="27b46-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27b46-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b46-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27b46-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b46-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b46-128">CommonParameters</span></span>
<span data-ttu-id="27b46-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b46-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b46-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27b46-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b46-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27b46-131">INPUTS</span></span>

### <span data-ttu-id="27b46-132">System.String</span><span class="sxs-lookup"><span data-stu-id="27b46-132">System.String</span></span>

## <span data-ttu-id="27b46-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27b46-133">OUTPUTS</span></span>

### <span data-ttu-id="27b46-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="27b46-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="27b46-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27b46-135">NOTES</span></span>

## <span data-ttu-id="27b46-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27b46-136">RELATED LINKS</span></span>

[<span data-ttu-id="27b46-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="27b46-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="27b46-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="27b46-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
