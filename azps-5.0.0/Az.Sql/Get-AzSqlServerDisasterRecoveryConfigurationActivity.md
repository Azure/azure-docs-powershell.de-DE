---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177720"
---
# <span data-ttu-id="b4cd5-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="b4cd5-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="b4cd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cd5-103">Ruft die Aktivität für eine Datenbankserver-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="b4cd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4cd5-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4cd5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="b4cd5-106">Das Cmdlet " **Get-AzSqlServerDisasterRecoveryConfigurationActivity** " Ruft die Aktivität für eine SQL Database Server-System Wiederherstellungskonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="b4cd5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4cd5-107">EXAMPLES</span></span>

## <span data-ttu-id="b4cd5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4cd5-108">PARAMETERS</span></span>

### <span data-ttu-id="b4cd5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cd5-109">-DefaultProfile</span></span>
<span data-ttu-id="b4cd5-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b4cd5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4cd5-111">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="b4cd5-111">-OperationId</span></span>
<span data-ttu-id="b4cd5-112">Gibt die Vorgangs-ID an.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4cd5-113">-ResourceGroupName</span></span>
<span data-ttu-id="b4cd5-114">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b4cd5-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b4cd5-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="b4cd5-116">Gibt den Namen der Server System-Wiederherstellungskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cd5-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="b4cd5-117">-ServerName</span></span>
<span data-ttu-id="b4cd5-118">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b4cd5-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4cd5-119">-Confirm</span></span>
<span data-ttu-id="b4cd5-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4cd5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4cd5-121">-WhatIf</span></span>
<span data-ttu-id="b4cd5-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4cd5-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4cd5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cd5-124">CommonParameters</span></span>
<span data-ttu-id="b4cd5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4cd5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cd5-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4cd5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cd5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4cd5-127">INPUTS</span></span>

### <span data-ttu-id="b4cd5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b4cd5-128">System.String</span></span>

### <span data-ttu-id="b4cd5-129">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b4cd5-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b4cd5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4cd5-130">OUTPUTS</span></span>

### <span data-ttu-id="b4cd5-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="b4cd5-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="b4cd5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4cd5-132">NOTES</span></span>

## <span data-ttu-id="b4cd5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4cd5-133">RELATED LINKS</span></span>

[<span data-ttu-id="b4cd5-134">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b4cd5-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
