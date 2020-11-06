---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: bd5d8d2c63b10ecc4aaabd5e96ab1ce844602325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482693"
---
# <span data-ttu-id="b154b-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="b154b-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="b154b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b154b-102">SYNOPSIS</span></span>
<span data-ttu-id="b154b-103">Entfernt die Überwachung eines SQL-Servers.</span><span class="sxs-lookup"><span data-stu-id="b154b-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b154b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b154b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b154b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b154b-105">DESCRIPTION</span></span>
<span data-ttu-id="b154b-106">Das Cmdlet **Remove-AzureRmSqlServerAuditing** entfernt die Überwachung eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b154b-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="b154b-107">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* und Server *Name* an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b154b-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="b154b-108">Nachdem Sie dieses Cmdlet ausgeführt haben, wird die Überwachung der Datenbanken auf dem Azure SQL Server nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b154b-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="b154b-109">Wenn der Befehl erfolgreich ausgeführt wird und Sie den *passthru* -Parameter angeben, gibt das Cmdlet ein Objekt zurück, das die aktuelle Überwachungsrichtlinie und die Azure SQL Server-IDs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b154b-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="b154b-110">Server-IDs sind **ResourceGroupName** und Server **Name**.</span><span class="sxs-lookup"><span data-stu-id="b154b-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="b154b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b154b-111">EXAMPLES</span></span>

### <span data-ttu-id="b154b-112">Beispiel 1: Entfernen der Überwachung eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b154b-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="b154b-113">Mit diesem Befehl wird die Überwachung aller Datenbanken entfernt, die sich auf Server01 in der Ressourcengruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="b154b-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="b154b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b154b-114">PARAMETERS</span></span>

### <span data-ttu-id="b154b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b154b-115">-DefaultProfile</span></span>
<span data-ttu-id="b154b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b154b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b154b-117">-PassThru</span></span>
<span data-ttu-id="b154b-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b154b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b154b-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b154b-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b154b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b154b-121">Gibt den Namen der Ressourcengruppe an, der der Azure SQL Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b154b-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b154b-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="b154b-122">-ServerName</span></span>
<span data-ttu-id="b154b-123">Gibt den Namen des Azure SQL Server an.</span><span class="sxs-lookup"><span data-stu-id="b154b-123">Specifies the name of the Azure SQL server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b154b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b154b-124">-Confirm</span></span>
<span data-ttu-id="b154b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b154b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b154b-126">-WhatIf</span></span>
<span data-ttu-id="b154b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b154b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b154b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b154b-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b154b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b154b-129">CommonParameters</span></span>
<span data-ttu-id="b154b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b154b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b154b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b154b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b154b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b154b-132">INPUTS</span></span>

### <span data-ttu-id="b154b-133">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b154b-133">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="b154b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b154b-134">OUTPUTS</span></span>

### <span data-ttu-id="b154b-135">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b154b-135">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="b154b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b154b-136">NOTES</span></span>

## <span data-ttu-id="b154b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b154b-137">RELATED LINKS</span></span>

[<span data-ttu-id="b154b-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b154b-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="b154b-139">Satz-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="b154b-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="b154b-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b154b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


