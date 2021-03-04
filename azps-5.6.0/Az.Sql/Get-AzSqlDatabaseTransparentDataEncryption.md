---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 1b045b97df1dbbc704f3288cf2075caa16f30bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949976"
---
# <span data-ttu-id="856c6-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="856c6-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="856c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="856c6-102">SYNOPSIS</span></span>
<span data-ttu-id="856c6-103">Ruft den TDE-Zustand für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="856c6-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="856c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="856c6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="856c6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="856c6-105">DESCRIPTION</span></span>
<span data-ttu-id="856c6-106">Das **Get-AzSqlDatabaseTransparentDataEncryption-Cmdlet** ruft den Zustand der Transparent Data Encryption (TDE) für eine Azure SQL ab.</span><span class="sxs-lookup"><span data-stu-id="856c6-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="856c6-107">Weitere Informationen finden Sie unter Transparente Datenverschlüsselung mit Azure SQL -Datenbank https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (in der Microsoft Developer Network Library).</span><span class="sxs-lookup"><span data-stu-id="856c6-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="856c6-108">Dieses Cmdlet ruft den aktuellen Zustand von TDE ab, aber sowohl Verschlüsselung als auch Entschlüsselung können vorgänge mit langer Ausführung sein.</span><span class="sxs-lookup"><span data-stu-id="856c6-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="856c6-109">Um den Fortschritt der Verschlüsselungsscans zu sehen, führen Sie das cmdlet Get-AzSqlDatabaseTransparentDataEncryptionActivity aus.</span><span class="sxs-lookup"><span data-stu-id="856c6-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="856c6-110">Dieses Cmdlet wird auch vom SQL Server Stretch Database Service in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="856c6-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="856c6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="856c6-111">EXAMPLES</span></span>

### <span data-ttu-id="856c6-112">Beispiel 1: Get TDE status for a database</span><span class="sxs-lookup"><span data-stu-id="856c6-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="856c6-113">Dieser Befehl ruft den Status von TDE für die Datenbank mit dem Namen Datenbank01 auf dem Server mit dem Namen server01 ab.</span><span class="sxs-lookup"><span data-stu-id="856c6-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="856c6-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="856c6-114">PARAMETERS</span></span>

### <span data-ttu-id="856c6-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="856c6-115">-DatabaseName</span></span>
<span data-ttu-id="856c6-116">Gibt den Namen der Datenbank an, für die dieses Cmdlet den TDE-Status erhält.</span><span class="sxs-lookup"><span data-stu-id="856c6-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="856c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856c6-117">-DefaultProfile</span></span>
<span data-ttu-id="856c6-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="856c6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="856c6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856c6-119">-ResourceGroupName</span></span>
<span data-ttu-id="856c6-120">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="856c6-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="856c6-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="856c6-121">-ServerName</span></span>
<span data-ttu-id="856c6-122">Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet den TDE-Status erhält.</span><span class="sxs-lookup"><span data-stu-id="856c6-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="856c6-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="856c6-123">-Confirm</span></span>
<span data-ttu-id="856c6-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="856c6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856c6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856c6-125">-WhatIf</span></span>
<span data-ttu-id="856c6-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="856c6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="856c6-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="856c6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856c6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856c6-128">CommonParameters</span></span>
<span data-ttu-id="856c6-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856c6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856c6-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="856c6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856c6-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="856c6-131">INPUTS</span></span>

### <span data-ttu-id="856c6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="856c6-132">System.String</span></span>

## <span data-ttu-id="856c6-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="856c6-133">OUTPUTS</span></span>

### <span data-ttu-id="856c6-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="856c6-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="856c6-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="856c6-135">NOTES</span></span>

## <span data-ttu-id="856c6-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="856c6-136">RELATED LINKS</span></span>

[<span data-ttu-id="856c6-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="856c6-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="856c6-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="856c6-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
