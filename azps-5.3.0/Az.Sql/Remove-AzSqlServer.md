---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460600"
---
# <span data-ttu-id="dcf32-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dcf32-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="dcf32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf32-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf32-103">Entfernt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="dcf32-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="dcf32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcf32-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf32-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcf32-105">DESCRIPTION</span></span>
<span data-ttu-id="dcf32-106">Das **Cmdlet "Remove-AzSqlServer"** entfernt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="dcf32-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="dcf32-107">Der Löschvorgang ist asynchron und kann einige Zeit dauern. Überprüfen Sie daher, ob der Vorgang abgeschlossen ist, bevor Sie weitere Vorgänge ausführen, die vom vollständig gelöschten Server abhängen.</span><span class="sxs-lookup"><span data-stu-id="dcf32-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="dcf32-108">Sie müssen z. B. einen neuen Server mit demselben Namen erstellen.</span><span class="sxs-lookup"><span data-stu-id="dcf32-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="dcf32-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dcf32-109">EXAMPLES</span></span>

### <span data-ttu-id="dcf32-110">Beispiel 1: Entfernen eines Servers</span><span class="sxs-lookup"><span data-stu-id="dcf32-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="dcf32-111">Mit diesem Befehl wird der Azure SQL Datenbankserver namens Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="dcf32-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="dcf32-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcf32-112">PARAMETERS</span></span>

### <span data-ttu-id="dcf32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf32-113">-DefaultProfile</span></span>
<span data-ttu-id="dcf32-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dcf32-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcf32-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dcf32-115">-Force</span></span>
<span data-ttu-id="dcf32-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="dcf32-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcf32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf32-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcf32-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dcf32-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="dcf32-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dcf32-119">-ServerName</span></span>
<span data-ttu-id="dcf32-120">Gibt den Namen des zu entfernenden Servers an.</span><span class="sxs-lookup"><span data-stu-id="dcf32-120">Specifies the name of the server to remove.</span></span>

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

### <span data-ttu-id="dcf32-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcf32-121">-Confirm</span></span>
<span data-ttu-id="dcf32-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dcf32-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf32-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dcf32-123">-WhatIf</span></span>
<span data-ttu-id="dcf32-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dcf32-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf32-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dcf32-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf32-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf32-126">CommonParameters</span></span>
<span data-ttu-id="dcf32-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf32-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf32-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcf32-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf32-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dcf32-129">INPUTS</span></span>

### <span data-ttu-id="dcf32-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dcf32-130">System.String</span></span>

## <span data-ttu-id="dcf32-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dcf32-131">OUTPUTS</span></span>

### <span data-ttu-id="dcf32-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="dcf32-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="dcf32-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dcf32-133">NOTES</span></span>

## <span data-ttu-id="dcf32-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dcf32-134">RELATED LINKS</span></span>

[<span data-ttu-id="dcf32-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dcf32-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="dcf32-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dcf32-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="dcf32-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dcf32-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="dcf32-138">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="dcf32-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


