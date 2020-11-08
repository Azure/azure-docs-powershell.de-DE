---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173429"
---
# <span data-ttu-id="519fa-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="519fa-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="519fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="519fa-102">SYNOPSIS</span></span>
<span data-ttu-id="519fa-103">Entfernt die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="519fa-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="519fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="519fa-104">SYNTAX</span></span>

### <span data-ttu-id="519fa-105">ServerParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="519fa-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="519fa-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="519fa-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="519fa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="519fa-107">DESCRIPTION</span></span>
<span data-ttu-id="519fa-108">Das Cmdlet **Remove-AzSqlServerAudit** entfernt die Überwachungseinstellungen eines Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="519fa-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="519fa-109">Geben Sie die Parameter *ResourceGroupName* und Server *Name* an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="519fa-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="519fa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="519fa-110">EXAMPLES</span></span>

### <span data-ttu-id="519fa-111">Beispiel 1: Entfernen der Überwachungseinstellungen eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="519fa-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="519fa-112">Beispiel 2: entfernen, durch Pipeline, die Überwachungseinstellungen eines Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="519fa-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="519fa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="519fa-113">PARAMETERS</span></span>

### <span data-ttu-id="519fa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="519fa-114">-AsJob</span></span>
<span data-ttu-id="519fa-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="519fa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="519fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519fa-116">-DefaultProfile</span></span>
<span data-ttu-id="519fa-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="519fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="519fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="519fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="519fa-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="519fa-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519fa-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="519fa-120">-ServerName</span></span>
<span data-ttu-id="519fa-121">SQL Server-Name.</span><span class="sxs-lookup"><span data-stu-id="519fa-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519fa-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="519fa-122">-ServerObject</span></span>
<span data-ttu-id="519fa-123">Das Serverobjekt, dessen Überwachungsrichtlinie verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="519fa-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="519fa-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="519fa-124">-Confirm</span></span>
<span data-ttu-id="519fa-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="519fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="519fa-126">-WhatIf</span></span>
<span data-ttu-id="519fa-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="519fa-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="519fa-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="519fa-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519fa-129">CommonParameters</span></span>
<span data-ttu-id="519fa-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="519fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519fa-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="519fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519fa-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="519fa-132">INPUTS</span></span>

### <span data-ttu-id="519fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="519fa-133">System.String</span></span>

### <span data-ttu-id="519fa-134">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="519fa-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="519fa-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="519fa-135">OUTPUTS</span></span>

### <span data-ttu-id="519fa-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="519fa-136">System.Boolean</span></span>

## <span data-ttu-id="519fa-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="519fa-137">NOTES</span></span>

## <span data-ttu-id="519fa-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="519fa-138">RELATED LINKS</span></span>
