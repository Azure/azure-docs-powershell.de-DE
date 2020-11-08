---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176737"
---
# <span data-ttu-id="f1041-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1041-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="f1041-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1041-102">SYNOPSIS</span></span>
<span data-ttu-id="f1041-103">Entfernt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="f1041-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="f1041-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1041-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1041-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1041-105">DESCRIPTION</span></span>
<span data-ttu-id="f1041-106">Das Cmdlet **Remove-AzSqlServer** entfernt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="f1041-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="f1041-107">Der Löschvorgang ist asynchron und kann einige Zeit in Anspruch nehmen, also überprüfen Sie, ob der Vorgang fertig ist, bevor Sie weitere Vorgänge ausführen, die vom vollständigen Löschen des Servers abhängen.</span><span class="sxs-lookup"><span data-stu-id="f1041-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="f1041-108">Sie müssen beispielsweise einen neuen Server erstellen, der denselben Namen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1041-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="f1041-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1041-109">EXAMPLES</span></span>

### <span data-ttu-id="f1041-110">Beispiel 1: Entfernen eines Servers</span><span class="sxs-lookup"><span data-stu-id="f1041-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="f1041-111">Mit diesem Befehl wird der Azure SQL-Datenbankserver mit dem Namen Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f1041-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="f1041-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1041-112">PARAMETERS</span></span>

### <span data-ttu-id="f1041-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1041-113">-DefaultProfile</span></span>
<span data-ttu-id="f1041-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f1041-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1041-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1041-115">-Force</span></span>
<span data-ttu-id="f1041-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f1041-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1041-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1041-117">-ResourceGroupName</span></span>
<span data-ttu-id="f1041-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f1041-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f1041-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="f1041-119">-ServerName</span></span>
<span data-ttu-id="f1041-120">Gibt den Namen des Servers an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1041-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1041-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1041-121">-Confirm</span></span>
<span data-ttu-id="f1041-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1041-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1041-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1041-123">-WhatIf</span></span>
<span data-ttu-id="f1041-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1041-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1041-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1041-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1041-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1041-126">CommonParameters</span></span>
<span data-ttu-id="f1041-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1041-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1041-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1041-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1041-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1041-129">INPUTS</span></span>

### <span data-ttu-id="f1041-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f1041-130">System.String</span></span>

## <span data-ttu-id="f1041-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1041-131">OUTPUTS</span></span>

### <span data-ttu-id="f1041-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="f1041-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="f1041-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1041-133">NOTES</span></span>

## <span data-ttu-id="f1041-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1041-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1041-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1041-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="f1041-136">Neu – AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1041-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="f1041-137">Satz-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f1041-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="f1041-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f1041-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


