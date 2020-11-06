---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496809"
---
# <span data-ttu-id="b2f98-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2f98-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b2f98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2f98-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f98-103">Legt eine Server-langfristige Aufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="b2f98-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2f98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2f98-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2f98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2f98-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f98-106">Das Cmdlet " **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** " legt die für diese Datenbank registrierte langfristige Aufbewahrungsrichtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="b2f98-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="b2f98-107">Bei der Richtlinie handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2f98-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="b2f98-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2f98-108">EXAMPLES</span></span>

## <span data-ttu-id="b2f98-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2f98-109">PARAMETERS</span></span>

### <span data-ttu-id="b2f98-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b2f98-110">-DatabaseName</span></span>
<span data-ttu-id="b2f98-111">Gibt den Namen der SQL-Datenbank an, für die dieses Cmdlet eine Richtlinie festlegt.</span><span class="sxs-lookup"><span data-stu-id="b2f98-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="b2f98-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f98-112">-ResourceGroupName</span></span>
<span data-ttu-id="b2f98-113">Gibt den Namen der Ressourcengruppe an, die die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="b2f98-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="b2f98-114">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b2f98-114">-ResourceId</span></span>
<span data-ttu-id="b2f98-115">Gibt die ID einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="b2f98-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f98-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="b2f98-116">-ServerName</span></span>
<span data-ttu-id="b2f98-117">Gibt den Server an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="b2f98-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="b2f98-118">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="b2f98-118">-State</span></span>
<span data-ttu-id="b2f98-119">Gibt einen Zustand an.</span><span class="sxs-lookup"><span data-stu-id="b2f98-119">Specifies a state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f98-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2f98-120">-Confirm</span></span>
<span data-ttu-id="b2f98-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2f98-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2f98-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2f98-122">-WhatIf</span></span>
<span data-ttu-id="b2f98-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2f98-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2f98-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2f98-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2f98-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f98-125">-DefaultProfile</span></span>
<span data-ttu-id="b2f98-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2f98-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2f98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f98-127">CommonParameters</span></span>
<span data-ttu-id="b2f98-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f98-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f98-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f98-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2f98-130">INPUTS</span></span>

## <span data-ttu-id="b2f98-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2f98-131">OUTPUTS</span></span>

## <span data-ttu-id="b2f98-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2f98-132">NOTES</span></span>

## <span data-ttu-id="b2f98-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2f98-133">RELATED LINKS</span></span>

[<span data-ttu-id="b2f98-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b2f98-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b2f98-135">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b2f98-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
