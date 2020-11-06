---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481477"
---
# <span data-ttu-id="f1ea2-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1ea2-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="f1ea2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ea2-103">Ruft eine Datenbank-langfristige Aufbewahrungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1ea2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1ea2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1ea2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1ea2-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ea2-106">Das Cmdlet " **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** " Ruft die langfristige Aufbewahrungsrichtlinie ab, die für diese Datenbank registriert ist.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="f1ea2-107">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="f1ea2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1ea2-108">EXAMPLES</span></span>

## <span data-ttu-id="f1ea2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1ea2-109">PARAMETERS</span></span>

### <span data-ttu-id="f1ea2-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f1ea2-110">-DatabaseName</span></span>
<span data-ttu-id="f1ea2-111">Gibt den Namen der SQL-Datenbank an, für die dieses Cmdlet eine Richtlinie erhält.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="f1ea2-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ea2-112">-ResourceGroupName</span></span>
<span data-ttu-id="f1ea2-113">Gibt den Namen der Ressourcengruppe an, die die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="f1ea2-114">-Servername</span><span class="sxs-lookup"><span data-stu-id="f1ea2-114">-ServerName</span></span>
<span data-ttu-id="f1ea2-115">Gibt den Server an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="f1ea2-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1ea2-116">-Confirm</span></span>
<span data-ttu-id="f1ea2-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ea2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ea2-118">-WhatIf</span></span>
<span data-ttu-id="f1ea2-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ea2-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ea2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ea2-121">-DefaultProfile</span></span>
<span data-ttu-id="f1ea2-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1ea2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ea2-123">CommonParameters</span></span>
<span data-ttu-id="f1ea2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ea2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ea2-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1ea2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ea2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1ea2-126">INPUTS</span></span>

## <span data-ttu-id="f1ea2-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1ea2-127">OUTPUTS</span></span>

## <span data-ttu-id="f1ea2-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1ea2-128">NOTES</span></span>

## <span data-ttu-id="f1ea2-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1ea2-129">RELATED LINKS</span></span>

[<span data-ttu-id="f1ea2-130">Satz-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f1ea2-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f1ea2-131">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f1ea2-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
