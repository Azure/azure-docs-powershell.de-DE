---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 76b4e024f5a6d5979bbcd9aa860caee823ecc28e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482694"
---
# <span data-ttu-id="c3909-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c3909-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="c3909-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3909-102">SYNOPSIS</span></span>
<span data-ttu-id="c3909-103">Entfernt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="c3909-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3909-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3909-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3909-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3909-105">DESCRIPTION</span></span>
<span data-ttu-id="c3909-106">Das Cmdlet **Remove-AzureRmSqlServer** entfernt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="c3909-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="c3909-107">Der Löschvorgang ist asynchron und kann einige Zeit in Anspruch nehmen, also überprüfen Sie, ob der Vorgang fertig ist, bevor Sie weitere Vorgänge ausführen, die vom vollständigen Löschen des Servers abhängen.</span><span class="sxs-lookup"><span data-stu-id="c3909-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="c3909-108">Sie müssen beispielsweise einen neuen Server erstellen, der denselben Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3909-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="c3909-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3909-109">EXAMPLES</span></span>

### <span data-ttu-id="c3909-110">Beispiel 1: Entfernen eines Servers</span><span class="sxs-lookup"><span data-stu-id="c3909-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c3909-111">Mit diesem Befehl wird der Azure SQL-Datenbankserver mit dem Namen Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c3909-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="c3909-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3909-112">PARAMETERS</span></span>

### <span data-ttu-id="c3909-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3909-113">-DefaultProfile</span></span>
<span data-ttu-id="c3909-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c3909-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3909-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3909-115">-Force</span></span>
<span data-ttu-id="c3909-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c3909-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3909-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3909-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3909-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c3909-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c3909-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="c3909-119">-ServerName</span></span>
<span data-ttu-id="c3909-120">Gibt den Namen des Servers an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3909-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3909-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3909-121">-Confirm</span></span>
<span data-ttu-id="c3909-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3909-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3909-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3909-123">-WhatIf</span></span>
<span data-ttu-id="c3909-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3909-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3909-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3909-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3909-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3909-126">CommonParameters</span></span>
<span data-ttu-id="c3909-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3909-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3909-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3909-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3909-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3909-129">INPUTS</span></span>

### <span data-ttu-id="c3909-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c3909-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c3909-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3909-131">OUTPUTS</span></span>

### <span data-ttu-id="c3909-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c3909-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c3909-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3909-133">NOTES</span></span>

## <span data-ttu-id="c3909-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3909-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3909-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c3909-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="c3909-136">Neu – AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c3909-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="c3909-137">Satz-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c3909-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="c3909-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c3909-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


