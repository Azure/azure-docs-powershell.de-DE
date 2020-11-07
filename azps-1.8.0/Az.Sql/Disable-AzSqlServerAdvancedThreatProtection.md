---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedThreatProtection.md
ms.openlocfilehash: d6a06c3f4c50e10522ed06e6b1cd4185c1ef6768
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659265"
---
# <span data-ttu-id="c886e-101">Disable-AzSqlServerAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c886e-101">Disable-AzSqlServerAdvancedThreatProtection</span></span>

## <span data-ttu-id="c886e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c886e-102">SYNOPSIS</span></span>
<span data-ttu-id="c886e-103">Deaktiviert den erweiterten Bedrohungsschutz auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="c886e-103">Disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="c886e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c886e-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedThreatProtection [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c886e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c886e-105">DESCRIPTION</span></span>
<span data-ttu-id="c886e-106">Das Cmdlet **Disable-AzSqlServerAdvancedThreatProtection** deaktiviert den erweiterten Bedrohungsschutz auf einem Server.</span><span class="sxs-lookup"><span data-stu-id="c886e-106">The **Disable-AzSqlServerAdvancedThreatProtection** cmdlet disables Advanced Threat Protection on a server.</span></span>

## <span data-ttu-id="c886e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c886e-107">EXAMPLES</span></span>

### <span data-ttu-id="c886e-108">Beispiel 1 – Schutz vor erweiterten Bedrohungen durch Server deaktivieren</span><span class="sxs-lookup"><span data-stu-id="c886e-108">Example 1 - Disable server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedThreatProtection `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="c886e-109">Beispiel 2 – deaktivieren Sie den erweiterten Schutz vor Bedrohungen durch Serverressourcen</span><span class="sxs-lookup"><span data-stu-id="c886e-109">Example 2 - Disable server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedThreatProtection

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="c886e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c886e-110">PARAMETERS</span></span>

### <span data-ttu-id="c886e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c886e-111">-DefaultProfile</span></span>
<span data-ttu-id="c886e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c886e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c886e-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c886e-113">-InputObject</span></span>
<span data-ttu-id="c886e-114">Das Serverobjekt, das mit der erweiterten Bedrohungsschutz Richtlinien Operation verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="c886e-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c886e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c886e-115">-ResourceGroupName</span></span>
<span data-ttu-id="c886e-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c886e-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="c886e-117">-Servername</span><span class="sxs-lookup"><span data-stu-id="c886e-117">-ServerName</span></span>
<span data-ttu-id="c886e-118">SQL-Datenbankservername</span><span class="sxs-lookup"><span data-stu-id="c886e-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="c886e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c886e-119">-Confirm</span></span>
<span data-ttu-id="c886e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c886e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c886e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c886e-121">-WhatIf</span></span>
<span data-ttu-id="c886e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c886e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c886e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c886e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c886e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c886e-124">CommonParameters</span></span>
<span data-ttu-id="c886e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c886e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c886e-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c886e-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c886e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c886e-127">INPUTS</span></span>

### <span data-ttu-id="c886e-128">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c886e-128">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="c886e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c886e-129">System.String</span></span>

## <span data-ttu-id="c886e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c886e-130">OUTPUTS</span></span>

### <span data-ttu-id="c886e-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c886e-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="c886e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c886e-132">NOTES</span></span>

## <span data-ttu-id="c886e-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c886e-133">RELATED LINKS</span></span>
